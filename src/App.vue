<!-- app.vue -->

<script>
import navItem from './components/navItem.vue';
import hero from './components/hero.vue';

export default {
  components: {
    navItem,
    hero
  },
  data() {
    return {
      menuItems: [
        { id: 1, 
          label: 'Home', 
          link: '#' 
        },

        { id: 2, 
          label: 'Pages', 
          link: '#' 
        },

        { id: 3, 
          label: 'Courses', 
          link: '#' 
        },

        { id: 4, 
          label: 'Features', 
          link: '#' 
        },

        { id: 5, 
          label: 'Blog', 
          link: '#' 
        },
        { id: 6, 
          label: 'Shop', 
          link: '#' 
        }
       
      ], 
      contentHero: [
        {
          title: "Complete Your Dreams in JavaS Programming",
          description: "Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistance and help.",
          iconDownload: "/src/img/download-solid.svg",
          buttonText: "Download free E-book"
        }
      ]
    };
  }
};
</script>

<template>
  
  <navItem :menu="menuItems"/>
  <hero :heroText="contentHero"/>
</template>

<style lang="scss">
  @use './styles/general.scss';
</style>

<style scoped>
  /* Stili specifici del tuo componente padre */
</style>

