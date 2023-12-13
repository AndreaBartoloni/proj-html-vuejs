<!-- app.vue -->

<script>
import navItem from './components/navItem.vue';
import hero from './components/hero.vue';
import AppBuildDream from './components/AppBuildDream.vue';
import AppCareer from './components/AppCareer.vue';
import AppCounter from './components/AppCounter.vue';
import AppCourse from './components/AppCourse.vue';
import AppLeftRight from './components/AppLeftRight.vue';


export default {
  components: {
    navItem,
    hero, 
    AppBuildDream,
    AppCareer, 
    AppCounter,
    AppCourse,
    AppLeftRight
  },
  data() {
    return {

      // Section header 
      menuItems: [
        { 
          id: 1, 
          label: 'Home', 
          link: '#' 
        },

        { 
          id: 2, 
          label: 'Pages', 
          link: '#' 
        },

        { 
          id: 3, 
          label: 'Courses', 
          link: '#' 
        },

        { 
          id: 4, 
          label: 'Features', 
          link: '#' 
        },

        { 
          id: 5, 
          label: 'Blog', 
          link: '#' 
        },

        { 
          id: 6, 
          label: 'Shop', 
          link: '#' 
        }
       
      ], 

      // Section main
      contentHero: [
        {
          title: "Complete Your Dreams in JavaS Programming",
          description: "Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistance and help.",
          iconDownload: "/src/img/download-solid.svg",
          buttonText: "Download free E-book"
        }
      ],

      // Section main
      sectionDream: [
        {
          image: "/src/img/home-5-image-box-01.png",
          title: "Idea Discussion",
          description: "Get teamed up with the specialists who work and teach coding for years at famous universities.",
          buttonText: "Start Now",
          arrow: "/src/img/arrow-right-long-solid.svg",
          link: "#"
        },
        {
          image: "/src/img/home-5-image-box-02.png",
          title: "Web Development",
          description: "Learn to start building a webpage from scratch. You decide your own pace, course and speed.		",
          buttonText: "Start Now",
          arrow: "/src/img/arrow-right-long-solid.svg",
          link: "#"
        },
        {
          image: "/src/img/home-5-image-box-03.png",
          title: "System Administration",
          description: "Learners are encouraged to study the mechanism and structure of system administration.",
          buttonText: "Start Now",
          arrow: "/src/img/arrow-right-long-solid.svg",
          link: "#"
        },
        {
          image: "/src/img/home-5-image-box-04.png",
          title: "Graphic Design",
          description: "Have a passion for graphics and arts? Show your talents with confidence and self-assertiveness.",
          buttonText: "Start Now",
          arrow: "/src/img/arrow-right-long-solid.svg",
          link: "#"
        }

      ], 

      //Section Main
      sectionCareer: [
        {
          plus: "/src/img/circle-plus-solid.svg",
          minus: "/src/img/circle-minus-solid.svg",
          title: "Multiple Platforms Supported for Teaching & Studying",
          description: "MaxCoach supports the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren’t supposed to be devoured in a short time, you can always access our knowledge base from any device.",
          isOpen: false
        },
        {
          plus: "/src/img/circle-plus-solid.svg",
          minus: "/src/img/circle-minus-solid.svg",
          title: "Multiple Course Participation at the Same Time",
          description: "Study for a number of courses at the same time is possible as long as you can afford the fee and time for completing them in the proper time. Learn at your own desired timeline and timetable. Maximum up to 5 course at a time for a learner at MaxCoach.",
          isOpen: false
        },
        {
          plus: "/src/img/circle-plus-solid.svg",
          minus: "/src/img/circle-minus-solid.svg",
          title: "Track Study Progress & Deliver Prompt Feedback",
          description: "It’s not just a normal thing to be able to build such a solid online educational system like MaxCoach where your progress is easily tracked and feedback is properly delivered. We promise to keep improving our system for better stability and flexibility.",
          isOpen: false
        },
      ],
      countersNum: [
        { 
          targetNumber: "1926", 
          text:"Finished Sessions",
          duration: 3000, 
          startNumber: 0 
        },
        { 
          targetNumber: "3092+", 
          text:"enrolled learners",
          duration: 3000, 
          startNumber: 0 
        },
        { 
          targetNumber: "200", 
          text:"online instructor",
          duration: 3000, 
          startNumber: 0 
        },
        { 
          targetNumber: "100%", 
          text:"satisfaction rate",
          duration: 3000, 
          startNumber: 0 
        },
      ],
      // Section course Main
      courseList: [
        {
          image: "/src/img/finance-course-thumbnail-04-480x298.jpg",
          imageThub: "/src/img/1c2c9a0fac3cd923d80b4ea64a0806ce.jpg",
          name: "Owen Christ",
          description: "Personal Finance: Financial Security Thinking & Principles",
          iconLesson: "/src/img/file-regular.svg",
          numLesson: "2 Lessons",
          iconStudent: "/src/img/user-regular.svg",
          numStudent: "2 Students",
          widget: "Free"
          
        },
        {
          image: "/src/img/finance-course-thumbnail-04-480x298.jpg",
          imageThub: "/src/img/1c2c9a0fac3cd923d80b4ea64a0806ce.jpg",
          name: "Owen Christ",
          description: "Personal Finance: Financial Security Thinking & Principles",
          iconLesson: "/src/img/file-regular.svg",
          numLesson: "2 Lessons",
          iconStudent: "/src/img/user-regular.svg",
          numStudent: "2 Students",
          widget: "$40.00"
          
        },
        {
          image: "/src/img/finance-course-thumbnail-04-480x298.jpg",
          imageThub: "/src/img/1c2c9a0fac3cd923d80b4ea64a0806ce.jpg",
          name: "Owen Christ",
          description: "Personal Finance: Financial Security Thinking & Principles",
          iconLesson: "/src/img/file-regular.svg",
          numLesson: "2 Lessons",
          iconStudent: "/src/img/user-regular.svg",
          numStudent: "2 Students",
          widget: "Free"
          
        },
        {
          image: "/src/img/finance-course-thumbnail-04-480x298.jpg",
          imageThub: "/src/img/1c2c9a0fac3cd923d80b4ea64a0806ce.jpg",
          name: "Owen Christ",
          description: "Personal Finance: Financial Security Thinking & Principles",
          iconLesson: "/src/img/file-regular.svg",
          numLesson: "2 Lessons",
          iconStudent: "/src/img/user-regular.svg",
          numStudent: "2 Students",
          widget: "$19.00"
          
        },
        {
          image: "/src/img/finance-course-thumbnail-04-480x298.jpg",
          imageThub: "/src/img/1c2c9a0fac3cd923d80b4ea64a0806ce.jpg",
          name: "Owen Christ",
          description: "Personal Finance: Financial Security Thinking & Principles",
          iconLesson: "/src/img/file-regular.svg",
          numLesson: "2 Lessons",
          iconStudent: "/src/img/user-regular.svg",
          numStudent: "2 Students",
          widget: "$26.00"
          
        },
        {
          image: "/src/img/finance-course-thumbnail-04-480x298.jpg",
          imageThub: "/src/img/1c2c9a0fac3cd923d80b4ea64a0806ce.jpg",
          name: "Owen Christ",
          description: "Personal Finance: Financial Security Thinking & Principles",
          iconLesson: "/src/img/file-regular.svg",
          numLesson: "2 Lessons",
          iconStudent: "/src/img/user-regular.svg",
          numStudent: "2 Students",
          widget: "$39.00"
          
        },
      ],
      contentLeftRight: [
        {
          contentRight: [
            {
              check: "/src/img/check-solid.svg",
              description: "Select & customize courses to your preferences",
     
            },
            {
              check: "/src/img/check-solid.svg",
              description: "Change the tutor and make arrangements",
     
            },
            {
              check: "/src/img/check-solid.svg",
              description: "Participate in events to join others",
     
            },
            {
              check: "/src/img/check-solid.svg",
              description: "Get the desired certificate delivered at house"
     
            }
          ]
        }
     
        
      ]

      
              
              
    };
  }
};

</script>

<template>
  <header>
    <navItem :menu="menuItems"/>
  </header>

  <main>
    <hero :heroText="contentHero"/>
    <AppBuildDream :dream="sectionDream"/>
    <AppCareer :career="sectionCareer"/>
    <AppCounter :counters="countersNum"/>
    <AppCourse :courseItems="courseList"/>
    <AppLeftRight :items="contentLeftRight"/>
  </main>

  <footer>

  </footer>
  
</template>

<style lang="scss">
  @use './styles/general.scss';
</style>

<style scoped>
  /* Stili specifici del tuo componente padre */
</style>

