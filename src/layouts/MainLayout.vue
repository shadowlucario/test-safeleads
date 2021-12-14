<template>
  <q-layout view="lHh Lpr lFf">
    <q-drawer
        v-model="drawer"
        show-if-above
        :breakpoint="500"
        bordered
        class="bg-grey-3"
      >
        <q-scroll-area class="fit">
          <q-list class="list">
            <div style="padding: 30px 0;">
              <img src="../assets/logoroxo.png" style="width:243px; height:45px;"/>
            </div>
            <q-item class="list__title">
              <q-item-section class="clickable">Produto</q-item-section>
            </q-item>
            <q-item class="list__title">
              <q-item-section class="clickable">Planos</q-item-section>
            </q-item>
            <q-separator />
            <q-item class="list__title">
              <q-item-section class="clickable">Premiações</q-item-section>
            </q-item>
            <q-item class="list__title">
              <q-item-section class="clickable">Cases</q-item-section>
            </q-item>
          </q-list>
        </q-scroll-area>
      </q-drawer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'MainLayout',
  data() {
    return {
      drawer: true,
    };
  },
});
</script>
<style lang="scss" scoped>
.list {
  &__title {
    font-family: Roboto;
    font-style: normal;
    font-weight: 500;
    font-size: 22px;
    line-height: 26px;
    color: #FA00EF;
    margin: 0;
  }
}
</style>
