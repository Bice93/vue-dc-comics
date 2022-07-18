<template>
  <header>
    <div class="container">
      <img src="../assets/images/dc-logo.png" alt="" />
      <nav>
        <ul>
          <li :class="{activeElement : index === activeIndex}" v-for="(link, index) in HeaderLinks" :key="index" >
            <a :href="link.url"> {{ link.text }} </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  data: function () {
    return {
      activeIndex: 3,
      HeaderLinks: [
        {
          text: "Characters",
          url: "#",
        },
        {
          text: "Comics",
          url: "#",
        },
        {
          text: "Movies",
          url: "#",
        },
        {
          text: "Tv",
          url: "#",
        },
        {
          text: "Games",
          url: "#",
        },
        {
          text: "Collectibles",
          url: "#",
        },
        {
          text: "Videos",
          url: "#",
        },
        {
          text: "Fans",
          url: "#",
        },
        {
          text: "News",
          url: "#",
        },
        {
          text: "Shop",
          url: "#",
        },
      ],
    };
  },


};
</script>

<style scoped lang="scss">
@import "../styles/variables.scss";

header {
  width: 100%;
  background-color: white;
  color: $colorNav;

    .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
}

img {
  height: 80px;
}

ul {
  list-style: none;
    li {
      font-size: 13px;
      font-weight: 600;
      display: inline-block;
      padding: 45px 10px;
      text-transform: uppercase;
        a{
          text-decoration: none;
          color: $colorNav;
        }

        &.activeElement {
          color: $colorActive;
          border-bottom: 4px solid $colorActive;
        }
    }
}
</style>