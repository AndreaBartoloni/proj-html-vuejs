<!-- app.vue -->

<script>
import NavBar from '/src/components/NavBar.vue';

export default {
  components: {
    NavBar
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
       
      ]
    };
  }
};
</script>

<template>
  <NavBar :menu="menuItems" />
</template>

<style lang="scss">
  @use './styles/general.scss';
</style>

<style scoped>
  /* Stili specifici del tuo componente padre */
</style>

