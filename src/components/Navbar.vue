<template>
  <div class="navbar">
    <div>
      <img src="../assets/logo.png" class="navbar__logo"/>
    </div>

    <div class="navbar__menu">
        <q-list class="navbar__list">
          <q-item class="navbar__list__title">
            <q-item-section class="clickable">Produto</q-item-section>
          </q-item>
          <q-item class="navbar__list__title">
            <q-item-section class="clickable">Planos</q-item-section>
          </q-item>
          <q-separator />
          <q-item class="navbar__list__title">
            <q-item-section class="clickable">Premiações</q-item-section>
          </q-item>
          <q-item class="navbar__list__title">
            <q-item-section class="clickable">Cases</q-item-section>
          </q-item>
        </q-list>
    </div>
    <ButtonDefault textColor="grey-1" noCaps title="Começar Agora"/>
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import ButtonDefault from './Button.vue';

export default defineComponent({
  name: 'Navbar',
  components: {
    ButtonDefault,
  },
});
</script>

<style lang="scss" scoped>
.navbar {
  height: 120px;
  align-items: center;
  display: flex;
  justify-content: space-around;
  @media (max-width: 700px) {
    display: none;
  }
  &__logo {
    width:243px;
    height:45px;
    color: #fff;
  }
  &__menu {
    display: flex;
    width: 600px;
    color: #fff;
    justify-content: space-around;
  }
  &__list {
    display: flex;
    width: auto;
    &__title {
      font-family: Roboto;
      font-style: normal;
      font-weight: 500;
      font-size: 22px;
      line-height: 26px;
      color: #FFFFFF;
      margin: 0 30px;
    }
  }
}
.clickable {
  cursor: pointer;
  &:hover {
    text-decoration: underline;
    text-decoration-color: #FA00EF;
    text-underline-offset: 8px;
  }
}
</style>
