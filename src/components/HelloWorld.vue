<template>
  <div id="hello-world">
    
  </div>
</template>

<script>
  export default {
    name: 'hello-world',
    props: {
    myvalue: Number,
  },
  methods: {
          alertme(){
              this.$emit('add:myvalue', this.myvalue)


          }


  }
			
			
			

  }

</script>

<style scoped></style>