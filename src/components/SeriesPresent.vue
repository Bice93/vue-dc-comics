<template>
  <SeriesPresent>
    <div class="jumbotron"></div>

    <div class="rowSeries">
      <div class="container">
        <h2>Current Series</h2>
        <div class="container_products">
          <Product v-for="(product, index) in series" 
          :key="index"
          :UrlImage="product.thumb"
          :PriceProduct="product.price"
          :TitleProduct="product.series"
          :TypeProduct="product.type"
          />
        </div>
        <button>Load More</button>
        <!-- <div class="container_products">
          <div class="product" v-for="(product, index) in series" :key="index">
            <div class="box_image">
              <img :src="product.thumb" :alt="product.series">
            </div>
            <h6> {{ product.series }} </h6>
          </div>
        </div> -->
      </div>
    </div>

    <div class="content_menu">
      <div class="container">
        <ul class="menu">
          <li v-for="(product, index) in ProductsList" :key="index">
            <img :src="require(`../assets/images/${product.urlImage}`)" alt="" />
            <h5> {{ product.text }} </h5>
          </li>
        </ul>
      </div>
    </div>
  </SeriesPresent>
</template>

<script>
import Product from './Product.vue';


export default {
  name: 'Products',
  components: {
    Product,
  },

  data: function () {
    return {
      series: [
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],

      ProductsList:[
        {
          text:'Digital Comics',
          urlImage:'buy-comics-digital-comics.png',
        },
         {
          text:'Dc Merchandise',
          urlImage:'buy-comics-merchandise.png',
        },
        {
          text:'Subscription',
          urlImage:'buy-comics-subscriptions.png',
        },
        {
          text:'Comic Shop Locator',
          urlImage:'buy-comics-shop-locator.png',
        },
        {
          text:'Dc Power Visa',
          urlImage:'buy-dc-power-visa.svg',
        },

      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../styles/variables.scss";

.jumbotron{
  height: 300px;
  background-image: url("../assets/images/jumbotron.jpg");
  background-size: cover;
}

.rowSeries {
  background-color: black;
  color: white;
  padding: 30px 0;
}

.container{
  position: relative;
  text-align: center;

    h2{
      width: 20%;
      background-color: $colorActive;
      text-align: center;
      text-transform: uppercase;
      font-size: 1.3rem;
      padding: 5px;
      position: absolute;
      top: -50px;
    }

    button{
      background-color: $colorActive;
      color: white;
      text-align: center;
      text-transform: uppercase;
      font-size: .6rem;
      font-weight: bold;
      padding: 5px 25px;
    }
}

.container_products {
  display: flex;
  flex-wrap: wrap;
}

.content_menu {
  background-color: $colorActive;
  padding: 50px 0;
}

.menu {
  list-style: none;
  display: flex;
  justify-content: space-around;
  align-items: center;
  color: white;
  text-transform: uppercase;

  li {
    display: flex;
    align-items: center;
    font-size: 15px;
      h5{
        font-weight: 400;
      }
  }
  img {
    height: 2.5rem;
    margin-right: 10px;
  }
}
</style>