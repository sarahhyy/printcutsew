<template>
  <div class="row">
    <div class="halfcol">
      <img class="squareImg" src="/src/assets/images/sewingMachine.jpg" />
    </div>
    <div class="halfcol">
      <div class="contactForm">
        <h1>Say Hello!</h1>
        <p>Write to us!</p>
        <p>Let us know of anything we can improve on or if we're doing things right.</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ContactPage',
  }
</script>

<style>
p {
  text-align: left;
  font-family: 'Alata', Verdana, Geneva, Tahoma, sans-serif;
  color: black;
  font-size: small;
}

div {
  margin:auto;
  width: auto;
}

contactForm {
  width: 200px;
  align-self: center;
}

#boxy {
  position: absolute;
  top: 50%;
  right: 15%;
  font-family: 'Inknut Antiqua', serif;
  font-size: 60px;
  color: white;
}

#fitted {
  position: absolute;
  top: 50%;
  left: 15%;
  font-family: 'Inknut Antiqua', serif;
  font-size: 60px;
  color: white;
}

.row {
  display: flex;
}

.halfcol {
  flex: 50%;
}

.squareImg {
  width: 100%;
  object-fit: contain;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
</style>