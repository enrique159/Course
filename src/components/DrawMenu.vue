<template>
  <div class="container">
    <div class="logo">
      <span>logo</span>
    </div>
    <div class="menu">
      <ul>
        <li>Opcion</li>
        <li>Opcion</li>
        <li>Opcion</li>
        <li>Opcion</li>
      </ul>
    </div>
    <div class="option">
      <h2>opciones</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "DrawMenu",
};
</script>

<style lang="scss" scoped>
.container {
  box-sizing: border-box;
  height: 100%;
  width: 20%;
  padding: 24px 48px;

  .logo, .menu, .option {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .logo {
    background-color: rgb(189, 139, 236);
    height: 20%;
  }

  .menu {
    background-color: rgb(43, 226, 217);
    height: 60%;
  }

  .option {
    background-color: blueviolet;
    height: 20%;
  }
}
</style>