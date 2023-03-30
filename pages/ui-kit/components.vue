<template>
  <div class="container">
    <article-card :article="cardsList[0]" />
  </div>
</template>

<script lang="ts" setup>
import { IArticle } from "@/models/Article.interface";

const cardsList: Array<IArticle> = [{
  id: 0,
  title: 'Как писать код быстро и безболезненно?',
  description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Elementum volutpat orci turpis urna. Et vestibulum, posuere tortor lacinia sit. Sagittis porttitor orci auctor in at tincidunt arcu egestas. Fusce arcu sodales lacinia eu auctor nunc nam id. Diam sit sed volutpat massa. Egestas ornare vel volutpat.',
  category: 'Создание сайтов',
  createdAt: '11.11.2011',
  imgUrl: '/ui-kit/card.svg'
}];
</script>

<style lang="scss" scoped>
.container {
  width: 600px;
  color: #fff;
}
</style>