<template>
  <button @click="onClick" :style="{background: color}" class="btn" type="submit">{{text}}</button>
</template>

<script>
export default {
   name : 'ButtonComponent',
   
   props: {
    color: String,
    text: String
   },

   methods: {
    onClick(){
        console.log("click");
    }
   }
}
</script>

<style scoped>

.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 4px;
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