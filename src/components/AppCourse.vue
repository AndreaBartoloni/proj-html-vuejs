<script>
export default {
  name: "AppCourse",
  props: {
    courseItems: Array,
  },
  data() {
    return {
        titleCourse: "Latest Featured Courses", 
        descriptionCourse: "chose whre you'd like to begin" 
    };
  },
};
</script>

<template>

    <div class="container-big mt-120">
        <div class="center">
            <p>{{ descriptionCourse }}</p>
            <h2>{{ titleCourse }}</h2>
        </div>
     
        <div class="flex flex-wrap">
           
            <div v-for="corso in courseItems" :key="corso" class="card-course">
                <div class="container-image">
                    <img :src="corso.image">
                    <p>{{ corso.widget }}</p>
                </div>
                <div class="container-course-info">
                    <div class="course-info">
                        <img :src="corso.imageThub">
                        <span>{{ corso.name }}</span>
                        <h3>{{ corso.description }}</h3>
                    </div>
                
                    <div class="flex">
                        <div>
                            <img :src="corso.iconLesson">
                            <span>{{ corso.numLesson }}</span>
                        </div>
                        <div>
                            <img :src="corso.iconStudent">
                            <span>{{ corso.numStudent }}</span>
                        </div>
                    </div>
                </div>
            </div>
          
            
        </div>
        <div class="center">
            <button >View all courses <img src="/src/img/arrow-right-long-solid.svg"></button>
        </div>
       

    </div>

</template>

<style scoped>
.center > p{
    line-height: 1.6em;
    margin-top: 14px;
    color: #696969;
    font-weight: 300;
    letter-spacing: 2px;
    text-transform: uppercase;
    
}
h2{
    padding: 0;
    margin: 0;
    color: #3f3a64;
    font-size: 48px;
    line-height: 1.17em;
    margin-bottom: 40px;
}
button > img {
    vertical-align: middle;
    margin-left:5px;
    filter: invert(1);
}
button{
    background-color: #20ad96;
    color: white;
    border: none;
    padding: 15px 40px 15px 40px;
    border-radius: 5px;
    font-size: 16px;
}
.card-course{
    width: 30%;
    margin: 15px;
}
.container-image > img{
    width: 100%;
    border-radius: 5px 5px 0px 0px;
}
.container-image{
    position: relative;
}
.container-image > p{
    position: absolute;
    top: 0;
    right: 10px;
    background-color: #20AD96;
    padding: 10px 20px;
    border-radius: 0px 5px 0px 5px;
    color: white;
    margin: 0;
}
.course-info > img{
    width: 30px;
    vertical-align: middle;
    border-radius: 50px;
}

.course-info > span{

    color: #696969;
    font-size: 15px;
    font-weight: 200;
    margin-left: 10px;
}
.course-info >  h3{
    font-size: 20px ;
    color: #333333;
    line-height: 1.6;
}

.container-course-info{
    padding: 30px;
}
</style>