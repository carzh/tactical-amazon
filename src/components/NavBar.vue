<template>
  <div class="bar" ref="navBar">
    <!-- logo -->
    <div class="card">
      <img
        src="@/assets/amazon_logo.png"
        @load="setHeight"
        :style="{ height: logoHeight + 'px' }"
      />
    </div>
    <!-- deliver -->
    <div class="card">
      <div class="locationtop">Deliver to Planet</div>
      <div class="locationbot">
        <img
          src="@/assets/location.png"
          style="vertical-align: text-bottom; margin-right: -5px"
        />
        <span style="vertical-align: text-bottom"> Earth </span>
      </div>
    </div>
    <!-- searchbar -->
    <div class="card">
      <div class="searchbar">
        <input type="text" />
        <button type="submit">🔍</button>
      </div>
    </div>
    <!-- hello customer -->
    <div class="card">
      <div class="top">Hello, Customer</div>
      <div class="locationbot">Account & Lists</div>
    </div>
    <!-- returns & orders -->
    <div class="card">
      <div class="top">Returns</div>
      <div class="locationbot">& Orders</div>
    </div>
    <!-- cart -->
    <div class="card">
      <img
        src="@/assets/cart.png"
        @load="setHeight"
        :style="{ height: logoHeight + 'px' }"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  data: function () {
    return {
      logoHeight: null,
    };
  },
  methods: {
    setHeight() {
      this.logoHeight = this.$refs.navBar.clientHeight - 10;
    },
  },
};
</script>

<style scoped>
.bar {
  height: 3.5rem;
  background-color: #131921;
  /* padding: 4px; */
  color: #fff;
  display: flex;
  width: 100%;
  font-weight: 300;
}
.card {
  vertical-align: middle;
  margin: auto 10px;
  display: inline-block;
  white-space: nowrap;
}
.locationtop {
  color: #9d9d9d;
  padding-left: 23px;
}
.locationbot {
  font-weight: 800;
}
.top {
  font-size: 0.8rem;
}
button {
  background-color: #febd69;
  border: none;
  height: 30px;
  width: 80px;
  border-radius: 0px 5px 5px 0px;
  font-size: 1.25rem;
}
input {
  border: none;
  border-radius: 5px 0px 0px 5px;
  height: 28px;
  width: 500px;
  font-size: 1.25rem;
}
</style>