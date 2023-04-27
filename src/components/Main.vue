<script>


export default {
  name: 'Main',

}
</script>

<template>

  <main>
    <div class="container">
      <h3> CONTENT GOES HERE </h3>
    </div>
  </main>
  
</template>


<style lang="scss" scoped>
@use '../scss/general/general' as *;
@use '../scss/general/mixin' as *;
@use '../scss/general/variables' as *;

main{
  background-color: #1C1C1C;
  min-height: 150px;
  padding: 30px 0;
  //bordo da togliere
  border: 2px solid white;
}

</style>