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
            subtitle: "Dream with Maxcoach"
        }
    },
    methods: {
        clickAccordion(){
            
        }
    },
}

</script>

<template>
    <div class="container-big">
        <div class="flex align-center mt-120">
            <div class="container-image-left">
                <img :src="bgImgCareer" class="absolute">
                <div class="relative">
                    <img :src="imgCareer">
                </div>
                
            </div>
            <div class="container-accordion ">
                <div v-for="accordion in career" :key="accordion" class=" ">
                    <div class="flex justify-content-between accordion">
                        <h6>{{ accordion.title }}</h6>
                        <img :src="accordion.plus">
                    </div>
                    
                    <p class="accordion-description">{{ accordion.description }}</p>
                </div>

            </div>
        
        </div>
    </div>

 
    
</template>


<style scoped>
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

}
.accordion{
    box-shadow: 0 15px 50px rgba(51, 51, 51, 0.1);
    padding: 10px 20px;
    margin-bottom: 15px;
    border-radius: 5px;
}
h6{
    font-size: 18px;
    color: #696969;
    font-weight: 600;
    margin: 0;
    padding: 0;
}

</style>
