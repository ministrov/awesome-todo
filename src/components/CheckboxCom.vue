<template>
  <input class="checkbox-input" type="checkbox">
</template>

<script>
export default {

}
</script>

<style lang="scss">
.checkbox-input {
  position: relative;
  display: block;
  width: 20px;
  height: 20px;
  margin: 0;
  background-color: #4F5565;
  border-radius: 6px;
  appearance: none;
  -webkit-appearance: none;

  &::after {
    position: absolute;
    content: "";
    top: 50%;
    left: 50%;
    display: none;
    width: 12px;
    height: 12px;
    background-image: url("../assets/tick.svg");
    background-repeat: no-repeat;
    transform: translate(-50%, -50%);
  }

  &:hover {
    background-color: #FF8469;
    opacity: 0.2;
  }

  &:checked {
    background-color: #FF8469;
  }

  &:checked:after {
    display: block;
  }
}

</style>