<template>
  <footer>
    <div class="container">
      <div class="footerLink">
        <div class="footerNav">
          <nav class="nav-footer comics">
            <h4>Dc Comics</h4>
            <ul>
              <li>Characters</li>
              <li>Comics</li>
              <li>Movies</li>
              <li>Tv</li>
              <li>Games</li>
              <li>Collectibles</li>
              <li>Videos</li>
            </ul>
          </nav>

          <nav class="nav-footer shop">
            <h4>Shop</h4>
            <ul>
              <li>Characters</li>
              <li>Comics</li>
            </ul>
          </nav>

          <nav class="nav-footer dc">
            <h4>Dc</h4>
            <ul>
              <li>Characters</li>
              <li>Comics</li>
              <li>Movies</li>
              <li>Tv</li>
              <li>Games</li>
              <li>Collectibles</li>
              <li>Videos</li>
              <li>Fans</li>
              <li>News</li>
              <li>Shop</li>
              <li>Shop</li>
            </ul>
          </nav>

          <nav class="nav-footer sites">
            <h4>Sites</h4>
            <ul>
              <li>Characters</li>
              <li>Movies</li>
              <li>Tv</li>
              <li>Games</li>
              <li>Collectibles</li>
            </ul>
          </nav>
        </div>
        <div class="footerLogo">
          <!-- <img src="../assets/images/dc-logo-bg.png" alt="" /> -->
        </div>
      </div>
    </div>
    <div class="footerFollow">
        <div class="container">
            <div class="btnFooter">
                <h5>Sign-Up Now!</h5>
            </div>
            
            <div class="iconFollow">
                <h3>Follow Us</h3>
                <img src="../assets/images/footer-facebook.png" alt="">
                <img src="../assets/images/footer-twitter.png" alt="">
                <img src="../assets/images/footer-youtube.png" alt="">
                <img src="../assets/images/footer-pinterest.png" alt="">
                <img src="../assets/images/footer-periscope.png" alt="">
            </div>
        </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../styles/variables.scss";

footer {
  background-image: url("../assets/images/footer-bg.jpg");
}

// link di navigazione del footer
.footerLink {
  display: flex;
  height: 350px;
  //height: calc(100vh - 400px - 80px);
}

.footerNav {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 30%;
  padding: 30px 0;

  .nav-footer {
    margin: 0 10px;

    h4 {
      color: white;
      text-transform: uppercase;
      font-size: 14px;
      margin-bottom: 8px;
    }
  }

  ul {
    list-style: none;
    font-size: 10px;
    color: $colorFooter;
    li {
      padding: 3px 0;
    }
  }
}

.footerLogo {
  width: 70%;
  background-image: url('../assets/images/dc-logo-bg.png');
  background-repeat: no-repeat;
  background-position: right;
}

//Follow del footer
.footerFollow {
  width: 100%;
  background-color: $bgFooterLight;
  color: white;
  text-transform: uppercase;

  .container{
        height: 80px;
        display: flex;
        justify-content: space-between;
        align-items: center;
  }

}

.btnFooter{
    border: 2px solid $colorActive;
    padding: 8px;
}

.iconFollow{
    display: flex;
    align-items: center;

    h3{
        color: $colorActive;
    }

    img{
        margin-left: 15px;
    }
}
</style>