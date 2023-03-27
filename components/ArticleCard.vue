<template>
  <div class="card">
    <img v-if="article.imgUrl" :src="article.imgUrl" class="card__img" />
    <div class="card__content">
      <h2 class="card__content-title">
        {{ article?.title }}
      </h2>
      <div class="card__content-text">
        {{ article?.description }}
      </div>
      <footer class="card__content-footer">
        <div class="footer-wrapper">
          <div class="card__content-date">{{ article?.createdAt }}</div>
          <div class="card__content-marker"></div>
          <div class="card__content-subtitle">{{ article?.category }}</div>
        </div>
        <nuxt-link
          class="card__content-link"
          :to="`/article/${article.id}`"
          >читать</nuxt-link
        >
      </footer>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { IArticle } from "@/models/Article.interface";

const props = defineProps<{ article: IArticle }>();
</script>

<style lang="scss" scoped>
@import "assets/styles/_breakpoints.scss";

.card {
  background-color: #202020;
  box-shadow: 0px 15px 25px rgba(0, 0, 0, 0.35);
  border-radius: 5px;

  &__img {
    max-width: 600px;
    width: 100%;
    margin: 0 auto;
  }

  &__content {
    padding: 25px;
  }

  &__content-title {
    color: rgba(255, 255, 255, 1);
  }

  &__content-text {
    color: rgba(210, 210, 210, 1);
    padding: 15px 0 20px 0;
  }

  &__content-footer {
    color: rgba(130, 130, 130, 1);
    display: flex;
    justify-content: space-between;
  }

  &__content-marker {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background-color: #c4c4c4;
    margin: auto 15px auto 15px;
  }

  &__content-link {
    color: #107eff;
  }
}

@media screen and (max-width: $mobile-breakpoint-max) {
  .card {
    &__content {
      padding: 15px;
    }

    &__content-footer {
      flex-direction: column;
    }
  }
}

.footer-wrapper {
  display: flex;
}
</style>