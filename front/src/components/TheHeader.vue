<template>
  <header class="header bg-gray-dark" id="header">
    <div class="container">
      <div class="header__content">
        <router-link to="/">
          <h1 class="header__title color-white"><span class="header__hash">#</span>SigaCorona</h1>
        </router-link>
        <!-- <a href class="header__link color-green">+ INFO</a> -->
      </div>
    </div>
  </header>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {}
})
export default class TheHeader extends Vue {}
</script>

<style lang="scss" scoped>
.header {
  box-shadow: 0px 8px 8px rgba(0, 0, 0, 0.15), 0px 4px 4px rgba(0, 0, 0, 0.15);
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 20;

  &__content {
    height: 64px;
    display: flex;
    align-self: center;
    justify-content: space-between;
    align-items: center;
  }

  &__hash {
    background: $grandient-vertical;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  &__link {
    @include fontRegular(18px);
  }

  &__title {
    @include fontHeavy(18px);

    @include media-breakpoint-up(lg) {
      @include fontHeavy(24px);
    }
  }
}
</style>
