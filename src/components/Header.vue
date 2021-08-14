<template>
  <div class="header">
      <div class="header__logo">
          <img src="../assets/bmuse_logo.png" alt="logo">
      </div>
      <div class="header__search">
          <img src="../assets/search.png" class="header__search--box" alt="logo">
      </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style scoped lang="scss">
    .header {
        display: flex;
        justify-content: space-between;
        padding: 10px 15px;
        background-color: transparent;
        align-content: center;
        margin-bottom: 30px;
        .header__search {
            .header__search--box {
                background-color: #000;
                border-radius: 50%;
                padding: 10px;
            }
        }
    }
</style>
