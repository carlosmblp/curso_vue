<template>
	
 <div id="app">
  Mi nombre es <input v-model="name">
  Mi Apellido es <input v-model="apellido">

  <p>************************************************************************************</p>
</div>

</template>
<script>
   export default {
    data() {
    return {
    name:'',
    apellido:''}
    },
    mounted(){
      if (localStorage.name) {
      this.name = localStorage.name;
    }
    if (localStorage.apellido) {
      this.apellido = localStorage.apellido;
    }
    },
    watch:{
    apellido(newApellido) {
      localStorage.apellido = newApellido;
    },
    name(newName) {
      localStorage.name = newName;
    }
    },
  };
</script>