<template>
    <NavBar />
    <categories-bar />
    <div class="heading">
    <h1>
        Amazon Best Sellers
    </h1>
    <div class="subtext">Our most popular products based on sales. Updated hourly.</div>
    <br>
    <div class="content">
        <div class="left">
            <left-bar />
        </div>
        <div class="right">
            <listings-grid />
        </div>
    </div>
</div>
</template>

<script>
import NavBar from './NavBar.vue'
import CategoriesBar from './CategoriesBar.vue'
import LeftBar from './LeftBar.vue'
import ListingsGrid from './ListingsGrid.vue'

export default {
    name: 'HomePage',
    components: {
        NavBar, CategoriesBar, LeftBar, ListingsGrid
    }
}
</script>

<style scoped>
body {
    width: 100%;
}
h1 {
    font-family: 'Source Sans Pro Black';
    margin: 10px 0px 0px 0px;
    padding: 0px;
    font-weight: 300;
}
.subtext {
    color: #666;
    font-size: 12px;
}
.heading {
    padding-left: 15px;;
}
.content {
    display: flex;
}
</style>