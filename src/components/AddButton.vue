<template>
  <button class="add-button">Add</button>
</template>

<script>
export default {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.add-button {
  display: block;
  width: 53px;
  height: 26px;
  font-size: 14px;
  font-weight: 500;
  text-transform: uppercase;
  color: #FFFFFF;
  background-color: #FF8469;
  outline: none;
  border: none;
  border-radius: 6px;

  &:hover {
    background-color: #D95133;
  }
}
</style>
