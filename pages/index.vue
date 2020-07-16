<template>
  <v-container>
   <div class="c-block c-block--modifier">
     <div class="c-block__element"></div>
   </div>
  </v-container>
</template>

<script>
export default {
}
</script>

<style lang="scss">
// @import '~sass-bem-utils/dist/sass-bem-utils';
@import '../assets/sass-bem-utils';

.block {
  background: green;
}

// откуда блять берётся .c-block?
@include block('block', 'component') {
  background: purple;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100px;
  height: 100px;

  @include element('element') {
    background: tomato;
    width: 50px;
    height: 50px;
  }
  @include modifier('modifier') {
    border-radius: 50%;
  }
}
</style>