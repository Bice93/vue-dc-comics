<template>
  <header>
    <div class="container">
      <img src="../assets/images/dc-logo.png" alt="" />
      <nav>
        <ul>
          <li>Characters</li>
          <li class="activeElement">Comics</li>
          <li>Movies</li>
          <li>Tv</li>
          <li>Games</li>
          <li>Collectibles</li>
          <li>Videos</li>
          <li>Fans</li>
          <li>News</li>
          <li>Shop</li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../styles/variables.scss";

header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background-color: white;

  .container {
    width: 1000px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}

img {
  height: 60px;
}

ul {
  list-style: none;
  li {
    font-size: 10px;
    font-weight: bold;
    display: inline-block;
    padding: 40px 10px;
    text-transform: uppercase;

    &.activeElement{
        color: $colorActive;
        border-bottom: 4px solid $colorActive;
    }
  }
}
</style>