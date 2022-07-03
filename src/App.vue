<template>
  <div id="app">
    <div class="psudo-wrapper">
      <div class="content-wrapper">
        <div class="main-header">
          <h2 class="main-header__title">Todo list</h2>

          <AddButton />
        </div>

        <ul class="todo-list" data-simplebar>
          <li class="todo-list__item todo-list__item--1">
            <CheckboxCom class="checkbox-input" />

            <div class="info-item">
              <h3 class="info-item__title">delectus aut autem</h3>
              <p class="info-item__text">laboriosam mollitia et enim quasi adipisci quia provident illum</p>
            </div>
          </li>
          <li class="todo-list__item todo-list__item--2">
            <CheckboxCom class="checkbox-input" />

            <div class="info-item">
              <h3 class="info-item__title">quo laboriosam deleniti aut qui</h3>
            </div>
          </li>
          <li class="todo-list__item todo-list__item--3">
            <CheckboxCom />

            <div class="info-item">
              <h3 class="info-item__title">laboriosam mollitia et enim quasi adipisci quia provident illum</h3>
            </div>
          </li>
          <li class="todo-list__item todo-list__item--4">
            <CheckboxCom />

            <div class="info-item">
              <h3 class="info-item__title">laboriosam mollitia et enim quasi adipisci quia provident illum</h3>
              <p class="info-item__text">accusamus eos facilis sint et aut voluptatem</p>
            </div>
          </li>
          <li class="todo-list__item todo-list__item--5">
            <CheckboxCom />

            <div class="info-item">
              <h3 class="info-item__title">repellendus sunt dolores architecto voluptatum</h3>
              <p class="info-item__text">accusamus eos facilis sint et aut voluptatem</p>
            </div>
          </li>
          <li class="todo-list__item todo-list__item--6">
            <CheckboxCom />

            <div class="info-item">
              <h3 class="info-item__title">repellendus sunt dolores architecto voluptatum</h3>
              <p class="info-item__text">accusamus eos facilis sint et aut voluptatem</p>
            </div>
          </li>
          <li class="todo-list__item todo-list__item--7">
            <CheckboxCom />

            <div class="info-item">
              <h3 class="info-item__title">repellendus sunt dolores architecto voluptatum</h3>
              <p class="info-item__text">accusamus eos facilis sint et aut voluptatem</p>
            </div>
          </li>
          <li class="todo-list__item todo-list__item--8">
            <CheckboxCom />

            <div class="info-item">
              <h3 class="info-item__title">repellendus sunt dolores architecto voluptatum</h3>
              <p class="info-item__text">accusamus eos facilis sint et aut voluptatem</p>
            </div>
          </li>
        </ul>
      </div>
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
  position: relative;
  z-index: 10;
  height: 482px;
  margin-top: 155px;
  padding-top: 30px;
  padding-bottom: 30px;
  padding-left: 30px;
  padding-right: 30px;
  background: #252E42;
  box-shadow: 0px 14px 34px rgba(0, 0, 0, 0.25);
  border-radius: 20px 0px 40px;
  overflow: hidden;
}
.psudo-wrapper {
  position: relative;

  &::after {
    position: absolute;
    content: "";
    z-index: -2;
    top: 135px;
    left: 0;
    width: 396px;
    height: 68px;
    background: linear-gradient(180deg, #31394D 0%, #091739 100%);
    border-radius: 20px;
    transform: rotate(-2.32deg);
  }

  &::before {
    position: absolute;
    content: "";
    z-index: -4;
    top: 126px;
    left: 2px;
    width: 341px;
    height: 85px;
    background: linear-gradient(180deg, #4F5565 0%, #000000 53.65%);
    border-radius: 20px;
    transform: rotate(-4.48deg);
  }
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
.todo-list {
  position: relative;
  margin: 0;
  margin-top: 25px;
  padding: 0;
  list-style: none;

  &::before {
    position: absolute;
    content: "";
    top: -6px;
    right: -14px;
    width: 4px;
    height: 216px;
    background-color: #FF8469;
  }
}
.todo-list__item {
  display: grid;
  grid-template-columns: 6% 1fr;
  align-items: center;

  &:not(:last-child) {
    margin-bottom: 20px;
  }

  @media (max-width: 400px) {
    max-width: 336px;
  }
}
.todo-list__item--5,
.todo-list__item--6,
.todo-list__item--7,
.todo-list__item--8 {
  @media (max-width: 442px) {
    display: none;
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
  font-size: 12px;
  font-weight: 400;
  line-height: 1.2;
  color: #4F5565;
}
.checkbox-input:checked + .info-item .info-item__title {
  text-decoration: line-through;
  text-decoration-color: #4F5565;
  color: #4F5565;

  &:hover {
    text-decoration-color: #ffffff;
    color: #ffffff;
  }
}
.info-item:hover + .checkbox-input::after {
  background-color: #FF8469;
  opacity: 0.2;
}
.copyright {
  margin: 0;
  margin-top: 31px;
  font-size: 16px;
  font-weight: 500;
  line-height: 1.2;
  color: #414B62;
}
.simplebar-track.simplebar-vertical .simplebar-scrollbar:before {
  width: 4px;
  height: 216px;
  background-color: #FF8469;
}
</style>
