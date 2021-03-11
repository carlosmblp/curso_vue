<template>
  <div>
     <LlamadaApi></LlamadaApi>
     <formulario></formulario>
  </div>
</template>
<script>
	import LlamadaApi from "./LlamadaApi.vue";
	import Formulario from "./Formulario.vue";
	
	
	export default {
		components: {
			LlamadaApi, 
			Formulario
		},
	};
</script>