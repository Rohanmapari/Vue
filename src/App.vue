<template>
  <div id="app" class="small-container">
    <h1>Welcome to Vue!</h1>
    <h2>Cube of number</h2>
	<hello-world :myvalue="myValue" />
	<hello-world @add:myvalue="addmyvalue" />

<input type="text" placeholder="Enter number..."  v-model="myValue"/>
<button type="button" v-on:click="addmyvalue(myValue)">Submit</button>
    <hello-world />
  </div>
</template>

<script>
  import HelloWorld from '@/components/HelloWorld.vue'


  export default {
    name: 'app',
    components: {
      HelloWorld,
	},
data(){
	return{
	name: 'User',
	myValue: ''
	}
	
},
methods: {
  addmyvalue(myvalue) {
    if(isNaN(myvalue)){
					alert("Please Enter Number");
				}else{
					alert("Cube of " + myvalue +" is " + myvalue * myvalue *myvalue );
				}
				
			}
  }
}

</script>

<style scoped>

h1{
  
  padding-top: 200px;
  padding-left: 560px;

}
h2{
padding-top: 10px;
  padding-left: 600px;
}
input[type=text]{
  padding: 12px; 
  font-size: 20px;
  border: 3px solid tomato;
  color: black;  
}

input{
  display: block;
  padding-top: 15px;
  margin: 30px auto;
}

button {
display: block;
margin: 20px auto;
background: tomato;
color: white;
border: none;
padding: 5px 10px; 
font-size: 16px;
border-radius: 4px;
cursor:pointer;
}

</style>