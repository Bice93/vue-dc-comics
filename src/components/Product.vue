<template>
        <div class="product">
        <div class="box_image">
            <img :src="UrlImage" :alt="TitleProduct" />
        </div>
        <h6>{{ TitleProduct }}</h6>
        </div>

</template>

<script>
export default {
    props:{
        'UrlImage': String,
        'PriceProduct': Number,
        'TitleProduct': String,
        'TypeProduct': String,
    },
};
</script>

<style scoped lang="scss">
.product{
      width: calc(100% / 6 - 20px);
      margin: 20px 10px;
      text-transform: uppercase;
      text-align: left;

      .box_image{
        width: 100%;
        height: 10rem;
        margin-bottom: 10px;

        img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position:top;
      }
      }

      h6{
        font-weight: 400;
      }
}
</style>