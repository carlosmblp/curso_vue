<template>
	<div>
	<h2>esta api muestra por consola una url de una imagen de un perro</h2>
	<p>************************************************************************************</p>
	</div>
</template>
<script>
    import axios from "axios";

	export default {
		components: {},
		data(){
			return{
				perroUrl: null
			}
          
		},
		mounted(){
		const options={
			method: "GET", 
			url: "https://dog.ceo/api/breeds/image/random",
		}
        axios.request(options).then(
        function (response){
        let perroUrl = response.data;
			console.log(perroUrl);
          })
          .catch(function(error){
            console.log(error);
          });
		},
	};
</script>