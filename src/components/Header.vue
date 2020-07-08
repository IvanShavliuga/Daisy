<template>
  <section class="header">
    <div class="header__topline">
      <div class="header__topline-logo">
        <div>D</div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.header {
  &__topline {
    &-logo {
      .hexogonlogo(#fc635e, #0c252d, 59px, 68px);
    }
  }
}
</style>
