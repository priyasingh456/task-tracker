<template>
  <div :class="[task.reminder ? 'reminder' : '', 'task']">
    <h5>{{ task.text }}
    <i class="fas fa-times"></i>
    </h5>
    <p>{{ task.day }}</p>
  </div>
</template>


<script>
export default {
    name: 'TaskComp',

    props: {
        task: Object
    }

}
</script>



<style scoped>

.fas {
  color: red;
  left: 0;
}
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}
.task.reminder {
  border-left: 5px solid green;
}
.task h5 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
p{
    opacity: .9;
}

</style>