<template>
  <div class="sidebar">
    <img
      src="@/public/background.svg"
      alt=""
      class="sidebar__images-background"
    />

    <div class="sidebar__info">
      <img src="@/public/avatar.jpg" alt="" class="sidebar__images-avatar" />
      <h2 class="sidebar__info-title">Дмитрий Валiк</h2>
      <h3 class="sidebar__info-subtitle">блог front-end разработчика</h3>
      <ul class="sidebar__info-links">
        <nuxt-link class="sidebar__info-link" to="https://vk.com/val_wel"
          ><img src="@/public/inst.svg" alt=""
        /></nuxt-link>
        <nuxt-link class="sidebar__info-link" to="https://vk.com/val_wel"
          ><img src="@/public/vk.svg" alt=""
        /></nuxt-link>
        <nuxt-link class="sidebar__info-link" to="https://vk.com/val_wel"
          ><img src="@/public/pint.svg" alt=""
        /></nuxt-link>
      </ul>
      <div class="sidebar__description">
        Front-end разработчик. Практик верстки сайтов. Созданием сайтов
        занимаюсь с 2012 года. Работал в нескольких ИТ компаниях и наработал
        более 10 000 часов в создании сайтов различной сложности.
      </div>
      <div class="sidebar__buttons">
        <button class="button">Мои работы</button>
        <button class="button">Написать мне</button>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import 'assets/styles/colors';

.sidebar {
  &__images {
    position: relative;
    max-height: 180px;
  }
  &__images-background {
  }

  &__images-avatar {
    width: 100px;
    height: 100px;
    object-fit: cover;
    border-radius: 50%;
    border: 2px solid #ffffff;
    box-shadow: 0px 7px 20px rgba(0, 0, 0, 0.25);
  }

  &__info {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    top: -50px;
    padding: 0 20px;
  }

  &__info-title {
    font-weight: 400;
    font-size: 18px;
    line-height: 21px;
    text-align: center;
    margin-top: 20px;
  }

  &__info-subtitle {
    padding-top: 3px;
    font-weight: 300;
    font-size: 14px;
    line-height: 16px;
    text-align: center;
    color: #dedede;
  }

  &__info-links {
    padding: 18px 0 30px 0;
  }

  &__info-link {
    &:nth-child(n + 2) {
      margin-left: 15px;
    }

    img {
      width: 25px;
      height: 25px;
    }
  }

  &__description {
    padding: 30px 0;
    font-weight: 400;
    font-size: 12px;
    line-height: 18px;
    text-align: center;
    border-top: 1px solid $sidebar-description-border-color;
    border-bottom: 1px solid $sidebar-description-border-color;
  }

  &__buttons {
    margin-top: 30px;
  }
}
</style>