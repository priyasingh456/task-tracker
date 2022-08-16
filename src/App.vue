<template>
  <div class="container">
    <HeaderPage title="Task Tracker" />
    <TasksComp :tasks="tasks" />
  </div>
</template>

<script>
import HeaderPage from './components/HeaderPage.vue';
import TasksComp from './components/TasksComp.vue';


export default {
  name: 'App',

  components: {
    HeaderPage,
    TasksComp
  },

  data() {
    return {
       tasks: []
    }
  },

  created(){
    this.tasks = [
      {
        id: 1,
        text: 'Vegetable shopping',
        day: '20 August at 5:00 PM',
        reminder: true
      },
      {
        id: 2,
        text: 'Internship Meeting',
        day: '18 August at 12:00 PM',
        reminder: true
      },
      {
        id: 3,
        text: 'Regular checkup',
        day: '20 August at 3:00 PM',
        reminder: true
      },
      {
        id: 4,
        text: 'Visit friend house',
        day: '19 August at 4:00 PM',
        reminder: false
      },
      {
        id: 5,
        text: 'Go to  the Bank',
        day: '20 August at 10:00 AM',
        reminder: true
      },
      {
        id: 6,
        text: 'Food shopping',
        day: '20 August at 8:00 PM',
        reminder: false
      }
    ]
  }
}
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
}
.container {
  width: 65%;
  margin: 30px auto;
  overflow: auto;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 2px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;
}

</style>
