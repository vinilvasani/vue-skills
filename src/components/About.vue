<template>
  <div class="about">
    <h1>Hello {{url_name}}, This is an about page</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna ali...</p>
  </div>
</template>

<script>
export default {
    name: 'About',
    data() {
        return {
            url_name: this.$route.params.name
        }
    },
    watch: {
       '$route.params.name' (nVal, cVal){
           console.log(nVal, cVal);
           this.url_name = nVal;
        }
    }
}
</script>
