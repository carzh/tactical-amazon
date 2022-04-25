<template>
  <div class="bar">
    Any department
    <div class="sub">
      <div
        class="cat"
        v-for="(category, index) in categories"
        :key="`category-${index}`"
      >
        {{ category }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LeftBar",
  data: function () {
    return {
      categories: [
        "Amazon Devices & Accessories",
        "Amazon Launchpad",
        "Appliances",
        "Apps & Games",
        "Arts, Crafts, & Sewing",
        "Audible Books & Originals",
        "Automotive",
        "Baby",
        "Beauty & Personal Care",
        "Books",
        "I got tired of typing out all",
        "the categories",
        "Amazon goes beyond",
        "a monopoly",
        "and has successfully invaded",
        "essentially all parts of ecommerce",
      ],
    };
  },
};
</script>

<style scoped>
.bar {
  border-right: 1px solid #ddd;
  font-weight: 800;
  width: 200px;
  padding: 10px 10px 0px 10px;
  font-size: 0.9rem;
}
.sub {
  font-weight: 300;
  padding-left: 20px;
}
.cat {
  padding-top: 3px;
}
</style>