
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
    <div class="background-beige" >
        <div class="container-header">
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
                    <input>
                    <img :src="search">
                </div>
            </div>
        </div>
        
    </div>
 
</template>

<style scoped>

.background-beige{
    background-color: #f5f1ed;
}
.container-header{
    display: flex;
    align-items: center;
    text-align: center;
   margin: auto;
    width: 90%;
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
    text-align: start;
}
.container-searchBar > input{
    width: 60% ;
}

</style>

