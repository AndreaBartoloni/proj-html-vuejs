
<!-- NAVBAR -->

<script>
export default {
  name: 'navBar',
  props: {
    menu: Array
  },
  data() {
    return {
        logo: "/src/img/dark-logo.png", 
        cart: "/src/img/cart-shopping-solid.svg",
        user: "/src/img/circle-user-regular.svg",
        search: "/src/img/magnifying-glass-solid.svg"
    }
  },
};
</script>

<template>
    <div class="background-beige " >
        <div class="container-header container-big">
            <div class="container-logo">
                <img :src="logo">
            </div>
            <div class="container-item">
                <ul>
                    <li v-for="item in menu" :key="item">
                        <p>{{ item.label }}</p>
                    </li>
                </ul>
                <div class="container-icon">
                    <img :src="cart">
                </div>
                <div class="container-icon">
                    <img :src="user">
                </div>
                <div class="container-searchBar">
                    <input placeholder="Search...">
                    <img :src="search">
                </div>
            </div>
        </div>
        
    </div>
 
</template>

<style scoped>


.container-header{
    display: flex;
    align-items: center;

    padding: 8px 0px;
}
.container-logo{
    width:25%;
}
.container-logo > img{
    width: 55%;
}
.container-item{
    width: 75%;
    display: flex;
    align-items: center;
    text-align: end;
}
ul{
    width: 60%;
}
li{
    width:20%;
    list-style-type: none
}

ul{
    display: flex;
}
.container-icon{
    width: 4%;
}
.container-searchBar{
    width: 29% ;
    text-align: center;
}
.container-searchBar > input{
    width: 40% ;
    border: none;
    padding: 13px 20px;
    border-radius: 5px 0px 0px 5px;
}
.container-searchBar > img{
    vertical-align: middle;
    padding-left: 10px;
    background-color: white;
    padding: 13px 20px;
    border-radius: 0px 5px 5px 0px;
}

</style>

