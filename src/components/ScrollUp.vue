<template>
    <div>
      <button 
        v-if="isVisible" 
        @click="scrollToTop" 
        class="scroll-up-btn">
        ↑ Scroll Up
      </button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isVisible: false,  // Estado para controlar la visibilidad del botón
      };
    },
    mounted() {
      // Agregar el evento de scroll cuando el componente se monta
      window.addEventListener("scroll", this.checkScrollPosition);
    },
    destroyed() {
      // Limpiar el evento cuando el componente se destruye
      window.removeEventListener("scroll", this.checkScrollPosition);
    },
    methods: {
      // Función para comprobar si se ha llegado al final de la página
      checkScrollPosition() {
        // Si el scroll está cerca del final de la página, mostrar el botón
        if (window.scrollY + window.innerHeight >= document.documentElement.scrollHeight - 100) {
          this.isVisible = true;
        } else {
          this.isVisible = false;
        }
      },
      // Función para hacer scroll hacia arriba
      scrollToTop() {
        window.scrollTo({
          top: 0,
          behavior: "smooth",  // Animación suave para el scroll
        });
      },
    },
  };
  </script>
  
  <style scoped>
.scroll-up-btn {
  position: fixed;
  bottom: 20px;
  right: 20px;
  background-color: blue;
  color: white;
  border: none;
  padding: 10px;
  border-radius: 50%;
  cursor: pointer;
  font-size: 1.5rem;
  display: none; /* Se oculta por defecto */
  z-index: 1000; /* Asegura que esté por encima de otros elementos */
}

.scroll-up-btn.show {
  display: block; 
}

  
  .scroll-up-btn:hover {
    background-color: #0056b3;
  }
  
  .scroll-up-btn[v-cloak] {
    display: block;
  }
  </style>
  