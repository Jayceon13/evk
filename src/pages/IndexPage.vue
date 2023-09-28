<template>
  <q-page class="flex flex-center">
    <div class="main-block">
      <div class="first-block">
        <p>Photographer EVGENY KORNEYCHUK</p>
        <q-btn outline rounded color="white" id="btn" label="Whats App" @click="goToWa"/>
        <q-btn outline rounded color="white" id="btn" label="Instagram" @click="goToInst"/>
        <q-btn outline rounded color="white" id="btn" label="Portfolio" @click="goToPort"/>
      </div>
      <div class="second-block">
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage',
  methods: {
    goToWa() {
      window.location.href = 'https://wa.me/+15513502104'
    },
    goToInst() {
      window.location.href = 'https://instagram.com/evk.ph'
    },
    goToPort() {
      window.location.href = 'https://evgeniy-photo.netlify.app'
    },
  }
})
</script>

<style>
.main-block{
  color: white;
  font-family: Jomolhari;
  display: flex;
}
.first-block{
  width: 50vw;
  height: 100vh;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  gap: 30px;
}
.second-block{
  width: 50vw;
  max-height: 100vh;
  background-image: url("/img/mainbg.jpg");
  background-size: cover;
  background-position: top;
}
#btn{
  text-transform: capitalize;
  width: 150px;

}
@media screen and (max-width: 800px){
  .main-block{
    flex-flow: column-reverse;
    justify-content: center;
    background-image: url("/img/mainbg.jpg");
    background-size: cover;
    background-position: top;
    width: 100vw;
  }
  .second-block{
    background-image: none;
    height: 50vh;
    width: 100vw;
  }
  .first-block{
    height: 50vh;
    width: 100vw;
  }
}

</style>
