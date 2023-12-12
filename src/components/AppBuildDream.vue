<script>
export default{
    name: "AppBuildDream",
    props: {
        dream: Array
    },
    data() {
        return {
            subtitle: "start leartning coding languages",
            text: "Build Your Dream TODAY"
        }
    },
}

</script>

<template>
    <div class="container-content-dream">
        <p>{{ subtitle }}</p>
        <h2>{{ text }}</h2>
    </div>
    <div class="flex container-big">
        <div v-for="itemDream in dream" :key="itemDream" class="container-card">
            <img :src="itemDream.image">
                <h3>{{ itemDream.title }}</h3>
                <p>{{ itemDream.description }}</p>
                <button :href="itemDream.link">{{ itemDream.buttonText }} <img :src="itemDream.arrow"></button>
            <div >
          
            </div>
        </div>
    </div>

    
</template>

<style scoped>
    .container-content-dream{
        text-align: center;
        margin-top: 70px;
    }
    .container-card{
        width: 25%;
        text-align: center;
        margin-top: 100px;
    }
    .container-card > p{
        line-height: 1.6em;
        margin-top: 14px;
        color: #696969;
        font-weight: 300;
    }
    h2{
        padding: 0;
        margin: 0;
        color: #3f3a64;
        font-size: 48px;
        line-height: 1.17em;
    }
    .container-content-dream > p{
        font-size: 15px;
        text-transform: uppercase;
        color: #696969;
        letter-spacing: 1px;
    }
    button{
        background-color: white;
        border: none;
        color: #8C89A2;
        font-weight: 600;
    }
    button > img{
        vertical-align: middle;
        margin-left: 5px;
        fill: #8C89A2;
        width: 12px;
    }

</style>