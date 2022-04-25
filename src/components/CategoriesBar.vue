<template>
  <div class="bar" ref="catbar">
    <div class="left">
      <img
        src="@/assets/menu.png"
        @load="setHeight"
        :style="{ height: menuHeight + 'px' }"
      />
      <span style="padding-left: 5px; padding-top: 3px"> All </span>
    </div>
    <div class="right">
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
  name: "CategoriesBar",
  data: function () {
    return {
      categories: [
        "Prime Video",
        "Best Sellers",
        "Customer Service",
        "Buy Again",
        "Browsing History",
        "Books",
        "Pet Supplies",
        "Groceries",
        "Kindle Books",
      ],
      menuHeight: null,
    };
  },
  methods: {
    setHeight() {
        this.menuHeight = this.$refs.catbar.clientHeight - 10;
    },
  },
};
</script>

<style scoped>
.bar {
  background-color: #232f3e;
  height: 2rem;
  color: white;
  display: flex;
  width: 100%;
  font-size: 15px;
}
.left {
  font-weight: 800;
  display: flex;
  height: 100%;
  padding: 0px 20px 5px 20px;
  width: 50px;
}
.right {
  display: flex;
}
.cat {
  margin: auto;
  padding: 0px 10px;
  font-weight: 300;
  height: 100%;
}
</style>