<template>
  <a
    href="https://github.com/mehmetsagir/vue-countries-cities"
    target="_blank"
    class="repo"
  >
    <icon name="github" color="white" size="42px" />
  </a>
</template>

<style lang="scss" scoped>
.repo {
  position: fixed;
  right: -160px;
  top: -110px;
  width: 300px;
  height: 200px;
  background: rgba(black, 0.5);
  transform: rotate(45deg);
  display: flex;
  align-items: flex-end;
  justify-content: center;
  transition: 300ms;
  svg {
    margin-bottom: 15px;
    transition: 300ms;
  }
  &:hover {
    right: -150px;
    top: -100px;
    background: black;
    svg {
      transform: rotate(-45deg);
    }
  }
}
</style>
