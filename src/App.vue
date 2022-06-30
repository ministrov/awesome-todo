<template>
  <div id="app">
    <div class="content-wrapper">
      <div class="main-header">
        <h2 class="main-header__title">Todo List</h2>

        <AddButton />
      </div>


    </div>

    <p class="copyright">© 2022. Zhilin Anton</p>
  </div>
</template>

<script>
import AddButton from './components/AddButton.vue'
export default {
  name: 'App',
  components: {
    AddButton
  }
}
</script>

<style lang="scss">
body {
  max-width: 1940px;
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  color: #ffffff;
  background-color: #252E42;
}
#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.content-wrapper {
  max-width: 420px;
  height: 570px;
  margin-top: 120px;
  padding-top: 30px;
  padding-bottom: 30px;
  padding-left: 30px;
  padding-right: 30px;
  background: #252E42;
  box-shadow: 0px 14px 34px rgba(0, 0, 0, 0.25);
  border-radius: 20px 0px 40px;
  Offset: 0px, 14px
  rgba(0, 0, 0, 0.25);
}
.main-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  min-width: 337px;
  max-width: 360px;

  &__title {
    margin: 0;
    font-size: 28px;
    font-weight: 700;
    line-height: 1.2;
  }
}
.copyright {
  margin: 0;
  margin-top: 31px;
  font-size: 16px;
  font-weight: 500;
  line-height: 1.2;
  color: #414B62;
}
</style>
