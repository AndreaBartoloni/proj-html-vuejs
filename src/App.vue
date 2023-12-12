<!-- app.vue -->

<script>
import navItem from './components/navItem.vue';
import hero from './components/hero.vue';
import AppBuildDream from './components/AppBuildDream.vue';
import AppCareer from './components/AppCareer.vue';

export default {
  components: {
    navItem,
    hero, 
    AppBuildDream,
    AppCareer
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

