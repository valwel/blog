<script lang="ts" setup>
</script>

<template>
  <div id="ui-kit-colors">
    <h1>Клик на название копирует в буфер обмена</h1>
    <ul class="colors-list">
      <li class="colors-item">
        <div class="color-box blue"></div>
        <a @click.prevent="copyToClipboard('#3137C9')" href="" class="copy-link">blue</a>
      </li>

      <li class="colors-item">
        <div class="color-box orange"></div>
        <a @click.prevent="copyToClipboard('#ED3024')" href="" class="copy-link">orange</a>
      </li>

      <li class="colors-item">
        <div class="color-box gray"></div>
        <a @click.prevent="copyToClipboard('#202020')" href="" class="copy-link">gray</a>
      </li>

      <li class="colors-item">
        <div class="color-box light-gray"></div>
        <a @click.prevent="copyToClipboard('#828282')" href="" class="copy-link">light-gray</a>
      </li>

      <li class="colors-item">
        <div class="color-box dark-gray"></div>
        <a @click.prevent="copyToClipboard('#121212')" href="" class="copy-link">dark-gray</a>
      </li>
    </ul>
  </div>
</template>

<script lang="ts" setup>
function copyToClipboard(color: string): void {
  navigator.clipboard.writeText(color);
}
</script>


<style lang="scss" scoped>
.colors-list {
  list-style: none;
}

.copy-link {
  text-decoration: none;
  color: $dark-gray;
  transition: color .3s;

  &:hover {
    color: $light-gray;
  }
}

.colors-item {
  display: flex;
  align-items: center;
  color: $dark-gray;
  margin-bottom: 12px;

  .orange {
    background-color: $orange;
  }

  .blue {
    background-color: $blue;
  }

  .gray {
    background-color: $gray;
  }

  .light-gray {
    background-color: $light-gray;
  }

  .dark-gray {
    background-color: $dark-gray;
  }
}

.color-box {
  margin-right: 8px;
  width: 20px;
  height: 20px;
}
</style>