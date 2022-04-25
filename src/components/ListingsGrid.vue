<template>
  <div class="listings">
    <div class="listing" v-for="item in items" :key="item.name">
      <img :src="imagePath(item.image)" />
      <h1>
      {{ item.name }}
      </h1>
      <div class="price">
          <div class="cents">
             $ 
          </div>

           {{ item.price }}
          <div class="cents">
              .{{item.cents}}
          </div>
      </div>
      <span> {{item.units}}</span>
      <br>
      <button>Add to Cart</button>

    </div>
  </div>
</template>

<script>
export default {
  name: "ListingsGrid",
  data: function () {
    return {
      items: [
        {
          name: "Amazon's Enterpise-wide Carbon Footprint",
          price: 60,
          cents: "64",
          units: "million metric tons of CO₂",
          source:
            "https://sustainability.aboutamazon.com/environment/sustainable-operations/carbon-footprint",
          image: "1.jpeg",
        },
        {
          name: "The world's annual internet usage",
          price: 97,
          cents: "00",
          units: "million metric tons of CO₂",
          source:
            "https://sustainability.aboutamazon.com/environment/sustainable-operations/carbon-footprinthttps://news.mongabay.com/2021/07/the-true-environmental-cost-of-the-internet-commentary/",
          image: "2.jpg",
          imageSource: "https://www.bbc.com/news/world-latin-america-53893161",
        },
        {
          name: "One hour of video streaming",
          price: 1000,
          cents: "00",
          units: "grams of CO₂",
          source:
            "https://sustainability.aboutamazon.com/environment/sustainable-operations/carbon-footprinthttps://news.mongabay.com/2021/07/the-true-environmental-cost-of-the-internet-commentary/https://www.pathzero.com/blog/the-internet-covid-19-and-the-environmental-impact-we-dont-think-about",
          image: "3.jpeg",
          imageSource:
            "https://www.ecohealthalliance.org/2019/08/the-amazon-is-burning",
        },
        {
          name: "Data centers & cloud services every year",
          price: 100,
          cents: "00",
          units: "megatonnes of CO₂",
          source:
            "https://sustainability.aboutamazon.com/environment/sustainable-operations/carbon-footprinthttps://news.mongabay.com/2021/07/the-true-environmental-cost-of-the-internet-commentary/https://www.pathzero.com/blog/the-internet-covid-19-and-the-environmental-impact-we-dont-think-abouthttps://www.advancedsciencenews.com/measuring-computers-carbon-footprint-with-green-algorithms/",
          image: "4.jpg",
          imageSource:
            "https://theprint.in/environment/the-amazon-is-still-burning-only-now-the-world-isnt-watching/437980/",
        },
      ],
    };
  },
  methods: {
    imagePath(file) {
      var images = require.context("@/assets/burning/", true, /\.(jpe?g)$/);
      return images("./" + file);
    },
  },
};
</script>

<style scoped>
.listings {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
}
.listing {
  padding: 0px 10px;
  width: 225px;
  white-space: nowrap;
}
img {
    height: 225px;
    width: 100%;
    object-fit: cover;
}
h1 {
    font-size: 1.25rem;
    padding: 0;
    margin: 0;
    white-space: normal;
}
.price {
    font-size: 2rem;
    display: flex;
}
.cents {
    font-size: 1rem;
}
button {
    margin: 10px 0px;
}
</style>