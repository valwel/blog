<template>
  <div class="layout">
    <div class="layout__sidebar">Sidebar</div>

     <div class="layout__content-wraper">
       <div class="header layout__header">Header</div>
        <div class="layout__content">
        <slot />
      </div>
     </div>
  </div>
</template>

<style lang="scss" scoped>
@import "assets/styles/colors";

.layout {
  display: flex;
  align-items: stretch;
  justify-content: stretch;
  color: #fff;
  min-height: 100vh;
  min-width: 100%;

  &__sidebar {
    box-shadow: 5px 0px 15px rgba(5, 5, 5, 0.1);
    width: 300px;
    background-color: $gray;
    height: 100vh;
  }

  &__content-wraper {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
  }
}

@media screen and (max-width: 767px) {
  .layout {
    &__sidebar {
      display: none;
    }
  }
}
</style>