<template>
  <footer>
    <div class="container">
      <div class="footerLink">
        <div class="footerNav">
          <nav
            class="nav-footer comics"
            v-for="(element, index) in FooterLinks"
            :key="index"
          >
            <h4>{{ element.title }}</h4>
            <ul>
              <li v-for="(link, indexLink) in element.content" :key="indexLink">
                <a :href="link.url"> {{ link.name }} </a>
              </li>
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
          <img src="../assets/images/footer-facebook.png" alt="" />
          <img src="../assets/images/footer-twitter.png" alt="" />
          <img src="../assets/images/footer-youtube.png" alt="" />
          <img src="../assets/images/footer-pinterest.png" alt="" />
          <img src="../assets/images/footer-periscope.png" alt="" />
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data: function () {
    return {
      FooterLinks: [
        {
          title: "Dc Comics",
          content: [
            {
              name: "Characters",
              url: "#",
            },
            {
              name: "Comics",
              url: "#",
            },
            {
              name: "Movies",
              url: "#",
            },
            {
              name: "Tv",
              url: "#",
            },
            {
              name: "Games",
              url: "#",
            },
            {
              name: "Videos",
              url: "#",
            },
            {
              name: "News",
              url: "#",
            },
          ],
        },

        {
          title: "Shop",
          content: [
            {
              name: "Shop DC",
              url: "#",
            },
            {
              name: "Shop DC Collectibles",
              url: "#",
            },
          ],
        },

        {
          title: "DC",
          content: [
            {
              name: "Therm Of Use",
              url: "#",
            },
            {
              name: "Privacy Policy (New)",
              url: "#",
            },
            {
              name: "Ad Choices",
              url: "#",
            },
            {
              name: "Advertising",
              url: "#",
            },
            {
              name: "Jobs",
              url: "#",
            },
            {
              name: "Subscriptions",
              url: "#",
            },
            {
              name: "Talent Workshops",
              url: "#",
            },
            {
              name: "CPSC Certificates",
              url: "#",
            },
            {
              name: "Talent Ratings",
              url: "#",
            },
            {
              name: "Shop Help",
              url: "#",
            },
            {
              name: "Contact Us",
              url: "#",
            },
          ],
        },

        {
          title: "Sites",
          content: [
            {
              name: "DC",
              url: "#",
            },
            {
              name: "MAD Magazine",
              url: "#",
            },
            {
              name: "DC Kids",
              url: "#",
            },
            {
              name: "DC Universe",
              url: "#",
            },
            {
              name: "DC Power Visa",
              url: "#",
            },
          ],
        },
      ],
    };
  },
};
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
}

.footerNav {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 30%;
  padding: 30px 0;

  .nav-footer {
    margin-right: 30px;

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

    li {
      padding: 4px 0;

      a {
        color: $colorFooter;
        text-decoration: none;
      }
    }
  }
}

.footerLogo {
  width: 70%;
  background-image: url("../assets/images/dc-logo-bg.png");
  background-repeat: no-repeat;
  background-position: right;
}

//Follow del footer
.footerFollow {
  width: 100%;
  background-color: $bgFooterLight;
  color: white;
  text-transform: uppercase;

  .container {
    height: 80px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}

.btnFooter {
  border: 2px solid $colorActive;
  padding: 8px;
}

.iconFollow {
  display: flex;
  align-items: center;

  h3 {
    color: $colorActive;
  }

  img {
    margin-left: 15px;
  }
}
</style>