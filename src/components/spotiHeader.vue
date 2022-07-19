<template>
  <header>
    <div class="container-fluid">
        <img  class="ms_header-logo" src="../assets/logo-small.svg" alt="Logo">
    </div>
  </header>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

div.container-fluid{
    height: 70px;
    background-color: $cardColorBg;

    img{
        height: 100%;
        padding: 15px;
    }
}




</style>