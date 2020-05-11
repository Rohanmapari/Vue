<template>
  <div id="app" class="small-container">
    <h1></h1>
	<hello-world :myvalue="myValue" />
	<hello-world @add:myvalue="addmyvalue" />

<input type="text" v-model="myValue"/>
<p><button type="button" v-on:click="alertMe(myValue)">Submit</button></p>
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
					alert("Cube of  " + myvalue +"  is " + myvalue * myvalue *myvalue );
				}
				
			}
  }
}

</script>