<template>
  <div id="app">
    <div class="content-wrapper">
      <div class="main-header">
        <h2 class="main-header__title">Todo List</h2>

        <AddButton />
      </div>


    </div>
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
  justify-content: center;
  align-items: center;
}
.content-wrapper {
  max-width: 420px;
  height: 570px;
  background-color: #4F5565;
}
.main-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
