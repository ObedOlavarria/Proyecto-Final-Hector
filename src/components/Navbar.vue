<template>
  <nav class="navbar">
    <section class="logo-container">
      <div class="ancho-logo">
        <div>
          <a href="#" class="logo">
            <img src="../assets/logo.png" alt="AccuMOVE Logo" />
          </a>
        </div>
        <div class="contact-info">
          <div class="contact-item">
            <i class="fas fa-clock"></i>
            <p>
              Mon-Fri: 10AM-7PM, <br />
              Sat-Sun: 10AM-3PM
            </p>
          </div>
          <div class="contact-item">
            <i class="fas fa-map-marker-alt"></i>
            <p>
              4578 Marmora Road, <br />
              Glasgow
            </p>
          </div>
          <div class="contact-item">
            <i class="fas fa-phone"></i>
            <p>
              Call Us: <br />
              (719) 445-2808
            </p>
          </div>
        </div>
        <div>
          <button class="make-appointment">
            <i class="fa-regular fa-bookmark"></i> Make an Appointment
          </button>
        </div>
      </div>
      <div class="contact-info-tableta">
        <div class="contact-item">
          <i class="fas fa-clock"></i>
          <p>
            Mon-Fri: 10AM-7PM, <br />
            Sat-Sun: 10AM-3PM
          </p>
        </div>
        <div class="contact-item">
          <i class="fas fa-map-marker-alt"></i>
          <p>
            4578 Marmora Road, <br />
            Glasgow
          </p>
        </div>
        <div class="contact-item">
          <i class="fas fa-phone"></i>
          <p>
            Call Us: <br />
            (719) 445-2808
          </p>
        </div>
      </div>
    </section>
    
    <section class="menu-container">
      <div class="ancho-menu">
        <!-- El Menú siempre está primero, en desktop y móvil -->
        <ul class="nav-menu" :class="{ active: isMenuOpen }">
          <br><br><br><br><br>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Services</a></li>
          <li><a href="#">Projects</a></li>
          <li><a href="#">Team</a></li>
          <li><a href="#">Prices</a></li>
          <li><a href="#">Blog</a></li>
          <li><a href="#">Contacts</a></li>
        </ul>

        <!-- Icono de búsqueda (visible siempre en móvil cuando no se ha abierto el menú) -->
        <div v-if="!isMenuOpen" class="search-container">
          <button class="search-icon" @click="toggleMenu">
            <i class="fas fa-search"></i>
          </button>
        </div>

        <!-- Icono de menú (visible cuando el menú no está abierto) -->
        <button
          class="menu-toggle"
          :class="{ hidden: isMenuOpen }"
          @click="toggleMenu"
        >
          <i class="fas fa-bars"></i>
        </button>

        <!-- Icono de cierre de menú (solo visible cuando el menú está abierto) -->
        <button
          class="close-menu"
          :class="{ hidden: !isMenuOpen }"
          @click="toggleMenu"
        >
          <i class="fas fa-times"></i>
        </button>
      </div>
    </section>
  </nav>
</template>

<script>
import $ from "jquery";

export default {
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
      if (this.isMenuOpen) {
        $(".menu-container").addClass("active");
      } else {
        $(".menu-container").removeClass("active");
      }
    },
  },
};
</script>

<style scoped>

* {
  box-sizing: border-box; /* Asegura que padding y border se incluyan en el ancho total */
}

body, html {
  overflow-x: hidden; /* Desactiva el scroll horizontal globalmente */
  margin: 0;
  padding: 0;
}
.ancho-logo {
  display: flex;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  justify-content: space-between;
}

.ancho-menu {
  display: flex;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  justify-content: space-between;
}

.navbar {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0;
  margin: 0;
  top: 0;
  left: 0;
  position: relative;
  width: 100%;
  z-index: 1000;
}

.logo-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  background-color: #fff;
  color: #000000;
  padding: 1rem 2rem;
  flex-wrap: wrap;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
  color: #ff0000;
}

.contact-info-tableta {
  display: none;
}

.contact-info {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.contact-item i {
  font-size: 2rem;
  color: #00b0f0;
  margin-right: 0.5rem;
}

.contact-item p {
  margin: 0;
}

.make-appointment {
  background-color: #00b0f0;
  color: #fff;
  padding: 0.6rem 1.5rem;
  border: none;
  border-radius: 0;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 1.2rem;
  line-height: 1.5;
}

.make-appointment i {
  font-size: 1.4rem;
}

.make-appointment:hover {
  background-color: #0056b3;
}

.menu-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  background-color: #1e1d24;
  padding: 0.1rem 2rem;
  position: relative;
  height: 70px;
}

.nav-menu {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
  flex-direction: row;
  gap: 1rem;
  align-items: center;
}

.nav-menu li {
  margin: 0;
}

.nav-menu a {
  text-decoration: none;
  color: #fff;
}

.nav-menu.active {
  display: flex;
  background-color: #fff;
  color: #000;
  width: 75%;
  top: 0;
  left: 0;
  height: 100%;
  flex-direction: column;
  justify-content: flex-start;
  transform: translateX(0);
  transition: transform 0.3s ease-in-out;
  position: fixed; /* Cambiar a fixed para que se fije en la pantalla */
}

.nav-menu.active li a {
  color: #000;
}

.menu-toggle {
  display: none;
  cursor: pointer;
  font-size: 1.5rem;
  color: #fff;
}

.search-container {
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

.search-icon {
  background: none;
  border: none;
  cursor: pointer;
  font-size: 1.5rem;
  color: #fff;
}

.close-menu {
  display: none;
  cursor: pointer;
  font-size: 1.5rem;
  color: #000000;
  background: none;
  border: none;
  position: absolute;
  top: -100px;
  right: 150px;
  z-index: 1100;
}

/* Media Queries */
@media (min-width: 768px) and (max-width: 1124px) {

  .contact-info-tableta {
    padding-top: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 2rem;
    margin: 0;
    width: 100%;
  }

  .ancho-logo {
    width: 80%;
  }

  .logo-container {
    padding: 2rem 2rem;
    flex-direction: row;
    gap: 0.5rem;
    align-items: center;
    margin-left: 1rem;
  }

  .make-appointment {
    margin-top: 0;
    text-align: left;
    order: 1;
    flex-grow: 1;
    margin-right: 1rem;
  }

  .contact-info {
    display: none;
  }

  .logo {
    font-size: 2rem;
    text-align: left;
  }

  .nav-menu {
    margin-left: 1rem;
  }

  .search-container {
    order: 3;
  }
}

@media (max-width: 768px) {
  .ancho-logo {
    flex-direction: column;
    align-items: center;
    width: 100%;
  }

  .logo-container {
    flex-direction: column;
    gap: 1rem;
  }

  .contact-info {
    display: none;
  }

  .make-appointment {
    margin-top: 1rem;
    width: 100%;
    text-align: center;
  }

  .logo {
    font-size: 2rem;
    text-align: center;
  }

  .menu-container {
    width: 100%;
  }

  .nav-menu {
    display: none;
    flex-direction: column;
    width: 100%;
    align-items: center;
    justify-content: flex-start; /* Alinea los elementos del menú a la izquierda */
    position: absolute; /* Asegura que el menú se posicione en la pantalla */
    background-color: #fff;
    top: 0;
    left: 0;
    z-index: 999;
  }
  
  .nav-menu li {
    margin: 1rem 0;
    
  }

  .search-container {
    order: 1;
  }

  .menu-toggle {
    order: 2;
    display: block;
    font-size: 1.5rem;
    color: #fff;
  }

  .close-menu {
    display: none;
  }

  .menu-container.active .close-menu {
    display: block;
  }

  .menu-container.active .menu-toggle {
    display: none;
  }
}
</style>
