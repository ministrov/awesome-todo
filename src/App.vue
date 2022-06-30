<template>
  <div id="app">
    <div class="content-wrapper">
      <div class="main-header">
        <h2 class="main-header__title">Todo List</h2>

        <AddButton />
      </div>

      <ul class="todo-list">
        <li class="todo-list__item">
          <CheckboxCom />

          <div class="info-item">
            <h3 class="info-item__title">delectus aut autem</h3>
            <p class="info-item__text">laboriosam mollitia et enim quasi adipisci quia provident illum</p>
          </div>
        </li>
        <li class="todo-list__item">
          <CheckboxCom />

          <div class="info-item">
            <h3 class="info-item__title">quo laboriosam deleniti aut qui</h3>
          </div>
        </li>
        <li class="todo-list__item">
          <CheckboxCom />

          <div class="info-item">
            <h3 class="info-item__title">laboriosam mollitia et enim quasi adipisci quia provident illum</h3>
          </div>
        </li>
        <li class="todo-list__item">
          <CheckboxCom />

          <div class="info-item">
            <h3 class="info-item__title">laboriosam mollitia et enim quasi adipisci quia provident illum</h3>
            <p class="info-item__text">accusamus eos facilis sint et aut voluptatem</p>
          </div>
        </li>
        <li class="todo-list__item">
          <CheckboxCom />

          <div class="info-item">
            <h3 class="info-item__title">repellendus sunt dolores architecto voluptatum</h3>
            <p class="info-item__text">accusamus eos facilis sint et aut voluptatem</p>
          </div>
        </li>
        <li class="todo-list__item">
          <CheckboxCom />

          <div class="info-item">
            <h3 class="info-item__title">repellendus sunt dolores architecto voluptatum</h3>
            <p class="info-item__text">accusamus eos facilis sint et aut voluptatem</p>
          </div>
        </li>
        <li class="todo-list__item">
          <CheckboxCom />

          <div class="info-item">
            <h3 class="info-item__title">repellendus sunt dolores architecto voluptatum</h3>
            <p class="info-item__text">accusamus eos facilis sint et aut voluptatem</p>
          </div>
        </li>
        <li class="todo-list__item">
          <CheckboxCom />

          <div class="info-item">
            <h3 class="info-item__title">repellendus sunt dolores architecto voluptatum</h3>
            <p class="info-item__text">accusamus eos facilis sint et aut voluptatem</p>
          </div>
        </li>
      </ul>
    </div>

    <p class="copyright">© 2022. Zhilin Anton</p>
  </div>
</template>

<script>
import AddButton from './components/AddButton.vue'
import CheckboxCom from './components/CheckboxCom.vue'
export default {
  name: 'App',
  components: {
    AddButton,
    CheckboxCom
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
  min-width: 360px;
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
  overflow: hidden;
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

.todo-list {
  margin: 0;
  margin-top: 30px;
  padding: 0;
  list-style: none;
}
.todo-list__item {
  display: flex;
  align-items: center;
  max-width: 360px;

  &:not(:last-child) {
    margin-bottom: 15px;
  }
}
.info-item {
  max-width: 325px;
  margin-left: 15px;
}

.info-item__title {
  margin: 0;
  font-size: 16px;
  font-weight: 500;
  line-height: 1.2;

  &:hover {
    color: #FF8469;
  }
}
.info-item__text {
  margin: 0;
  margin-top: 5px;
  font-size: 12px;
  font-weight: 400;
  line-height: 1.2;
  color: #4F5565;
}
</style>
