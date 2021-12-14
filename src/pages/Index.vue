<template>
  <q-page style="height: 100vh;">
    <div class="home">
      <Navbar/>
      <div class="home__container">
        <div class="home__content">
          <div class="home__content__title">
            A MAIOR SOLUÇÃO PARA ENERGIA SOLAR
            <span class="text-white">DA AMÉRICA LATINA</span>
          </div>
          <div class="home__content__description">
            Ter o controle de todos os processos, é a realidade
            de menos de 30% dos integradores de energia solar.
            <span style="color: #FA00EF;">Mude agora com SafeLeads!</span></div>
          <div class="home__content__actions">
            <ButtonDefault
              textColor="grey-1"
              noCaps title="Começar agora"
              style="margin-right: 30px;"/>
            <ButtonDefault
              dark
              textColor="grey-1"
              noCaps
              title="Consultar vendedor"/>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';
import Navbar from '../components/Navbar';
import ButtonDefault from '../components/Button';

export default defineComponent({
  name: 'PageIndex',
  components: {
    Navbar,
    ButtonDefault,
  },
});
</script>
<style lang="scss" scoped>
.home {
  background: linear-gradient(259.56deg, #3A004A 1.39%, #640080 100%);
  height: 90%;
  @media (max-width: 700px) {
    height: 100vh;
  }
  &__container {
    display: flex;
    justify-content: flex-start;
    padding-left: 140px;
    @media (max-width: 700px) {
      padding: 10px;
    }
  }
  &__content {
    padding: 100px 0;
    width: 40%;
    @media (max-width: 700px) {
      padding: 70px 0;
      width: 95%;
    }
    &__title {
      padding: 15px 0;
      font-family: Roboto;
      font-style: normal;
      font-weight: bold;
      font-size: 60px;
      line-height: 70px;
      color: #FA00EF;
      @media (max-width: 700px) {
        font-size: 40px;
        line-height: 40px;
      }
    }
    &__description {
      color: #fff;
      padding: 15px 0;
      font-family: Roboto;
      font-style: normal;
      font-weight: normal;
      font-size: 30px;
      line-height: 35px;
      @media (max-width: 700px) {
        font-size: 20px;
      }
    }
    &__actions {
      padding: 15px 0;
      display: flex;
    }
  }
}

</style>
