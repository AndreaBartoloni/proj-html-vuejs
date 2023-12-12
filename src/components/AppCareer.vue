<script>

export default{
    name: "AppCareer",
    props: {
        career: Array
    },
    data() {
        return {
            imgCareer: "/src/img/about-us-03-image-01.png", 
            bgImgCareer: "/src/img/underlay-shape-lilla.svg",
            title: "Construct A Stunning Career Perspective",
            subtitle: "Dream with Maxcoach", 
            showAccordion: false,
            counter: 0
        }
    },
    methods: {
        clickAccordion(){
            this.showAccordion = !this.showAccordion
        }
    }
}

</script>

<template>
    <div class="container-big">
        <div class="flex mt-120">
            <div class="container-image-left">
                <img :src="bgImgCareer" class="absolute">
                <div class="relative">
                    <img :src="imgCareer">
                </div>
                
            </div>
            <div class="container-accordion ">
                <p>{{ subtitle }}</p>
                <h2>{{ title }}</h2>
                <div v-for="accordion in career" :key="accordion" class="mb-20">
                    <div @click="clickAccordion()" class="flex justify-content-between accordion">
                        <h6>{{ accordion.title }}</h6>
                        <img :src="accordion.plus">
                    </div>
                    
                    <p v-if="showAccordion" class="accordion-description">{{ accordion.description }}</p>
                </div>

            </div>
        
        </div>
    </div>

 
    
</template>


<style scoped>
  h2{
    padding: 0;
    margin: 0;
    color: #3f3a64;
    font-size: 48px;
    margin-right: 100px;
    line-height: 1.17em;
    margin-bottom:40px;
    margin-top: 25px;
  }
  .container-accordion > p{
        font-size: 15px;
        text-transform: uppercase;
        color: #696969;
        letter-spacing: 1px;
    }
.container-image-left{
    width: 50%;
    display: flex;
    align-items: center;
    text-align: center;
    margin-top: 120px;
}
.relative > img{
    width: 70%;
}
.relative{
    position: relative;
    width: 100%;
}
.absolute{
    position: absolute;
    width: 30%;
}
.container-accordion{
    width: 50%;
    margin-top: 120px;
}

.accordion{
    box-shadow: 0 15px 50px rgba(51, 51, 51, 0.1);
    padding: 20px 30px;
    border-radius: 5px;
}
.accordion-description{
    box-shadow: 0 15px 50px rgba(51, 51, 51, 0.1);
    padding: 20px 30px;
    border-radius: 5px;
    margin: 0;
}

h6{
    font-size: 18px;
    color: #696969;
    font-weight: 600;
    margin: 0;
    padding: 0;
}

</style>
