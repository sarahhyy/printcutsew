<template>
  <div>
    <p>{{blurbText[pageIndex]}}</p>
  </div>
</template>

<script>
  export default {
    name: 'Blurb',
    props: {
      pageIndex: Number
    },

    data () {
      return {
        blurbText: [
          "Free downloadable t-shirt sewing patterns. \nEasy DIY tees. \nStart customizing your tee below!", 
          "Switch up your design, toggle different parts to get your perfect tee. \nWhen you’re done, scroll down to stitch it together.",
          "Does your new design fit you to a T? ;D \nSelect a size, download your pdf pattern and get sewing!"
        ]
      }
    }
    
  }



</script>

<style>
p {
  text-align: center;
  font-family: 'Alata', Verdana, Geneva, Tahoma, sans-serif;
  color: black;
  font-size: small;
}

div {
  margin:auto;
  width: auto;
}

</style>