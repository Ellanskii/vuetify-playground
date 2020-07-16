<template>
  <v-container class="block">
   <div class="block block_modifier">
     <div class="block-element"></div>
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