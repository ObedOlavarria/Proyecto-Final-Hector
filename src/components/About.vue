<template>
  <section class="container-section">
    <div class="ancho">
      <div class="container-title-seccion">
        <h1>About</h1>
      </div>
    </div>
  </section>

  <section class="container-section">
    <div class="imag-fondo">
      <img src="../assets/slide-3.jpg" alt="Household help image" />
      <div class="ancho">
        <div class="container-text-fondo">
          <div class="container-text-div">
            <div class="text-item">
              <h1>
                Need some professional household <br />
                help?
              </h1>
            </div>
            <div class="text-item">
              Contact our Customer Service representative to make an appointment
              and to answer all your questions!
            </div>
            <div class="text-item">
              <button aria-label="Make an Appointment">
                Make an Appointment
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="container-section">
    <div class="ancho">
      <div class="container-acordeon-section">
        <div class="container-title-acordeon">
          <h1>WHY JohnnyGo!</h1>
        </div>
        <div class="container-acordeon-div">
          <div class="accordion-container">
            <div
              class="accordion-item"
              v-for="(item, index) in accordionItems"
              :key="index"
              :ref="'accordionItem' + index"
            >
              <button class="accordion-header" @click="toggleAccordion(index)">
                {{ item.title }}
                <i
                  :class="{
                    'fas fa-minus': isAccordionOpen[index],
                    'fas fa-plus': !isAccordionOpen[index],
                  }"
                ></i>
              </button>
              <div class="accordion-content">
                <p>{{ item.content }}</p>
              </div>
            </div>
          </div>
          <div class="container-acordeon">
            <div class="container-acordeon-div-cards">
              <div class="container-acordeon-cards">
                <div><i class="far fa-clock"></i></div>
                <div>
                  <h3>Always Available</h3>
                  <p>
                    We accept requests and phone calls 24/7 so you could resolve
                    any problem whenever you need. Our emergency team will be at
                    your place...
                  </p>
                </div>
              </div>
              <div class="container-acordeon-cards"></div>
              <div></div>
              <div>
                <h3></h3>
                <p></p>
              </div>
              <div class="container-acordeon-cards">
                <div><i class="far fa-clock"></i></div>
                <div>
                  <h3>Always Available</h3>
                  <p>
                    We accept requests and phone calls 24/7 so you could resolve
                    any problem whenever you need. Our emergency team will be at
                    your place...
                  </p>
                </div>
              </div>
              <div class="container-acordeon-cards">
                <div></div>
                <div>
                  <h3></h3>
                  <p></p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import $ from "jquery";

export default {
  data() {
    return {
      accordionItems: [
        {
          title: "About Company",
          content: "We are a company providing a wide range of maintenance and many other services needed to make your life comfortable and happy. Our high-class experts fix any malfunction and install any equipment in your house",
        },
        {
          title: "Our Mission",
          content: "We work to ensure people’s comfort at their home, and to provide the best and the fastest help at fair prices. We stand for quality, safety and credibility, so you could be sure about our work.",
        },
        {
          title: "Our Vision",
          content: "We have been working for years to improve our skills, to expand the spheres of our work and to use the latest tools, so you could receive better results. We strive to enhance our experts’ skills and use high-tech technology.",
        },
        {
          title: "Our Goal",
          content: "The main goal is to provide our clients with the most complete list of services. We aim to expand our team of experts as there are more and more spheres of maintenance that we want to work with.",
        },
      ],
      isAccordionOpen: [], // Arreglo para manejar el estado abierto/cerrado
    };
  },
  mounted() {
    // Inicializa todos los acordeones como cerrados
    this.isAccordionOpen = this.accordionItems.map(() => false);
  },
  methods: {
    toggleAccordion(index) {
      const accordionItem = this.$refs["accordionItem" + index];
      const $content = $(accordionItem).find(".accordion-content");
      const isActive = $content.is(":visible");

      // Cierra todas las secciones
      $(".accordion-content").slideUp();
      this.isAccordionOpen = this.isAccordionOpen.map(() => false);

      // Si la sección no estaba activa, la abre
      if (!isActive) {
        $content.slideDown();
        this.isAccordionOpen[index] = true;
      }
    },
  },
};
</script>

<style scoped>
/* Estilo global para las secciones */
.container-section {
  width: 100%;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-sizing: border-box;
}

.ancho {
  max-width: 1200px; /* Limita el ancho máximo a 1200px */
  width: 100%; /* Ocupa todo el ancho del contenedor padre */
  margin: 0 auto; /* Centra horizontalmente */
  box-sizing: border-box; /* Incluye padding en el cálculo del ancho */
}


.container-title-seccion {
  text-align: center; /* Centrar el texto */
  margin-bottom: 1.5rem; /* Espaciado debajo del título */
}

.container-title-seccion h1 {
  font-family: 'Gloock', sans-serif; /* Aplicar Gursa a los encabezados */
  font-size: 3rem; /* Tamaño grande para el título */
  font-weight: 600; /* Peso de la fuente para mayor énfasis */
  color: #333; /* Color oscuro para el título */
  text-transform: uppercase; /* Convertir el texto a mayúsculas */
  letter-spacing: 2px; /* Espaciado entre las letras */
  margin: 0; /* Eliminar márgenes predeterminados */
}

/* Añadir estilos de hover para mejorar la interacción */
.container-title-seccion h1:hover {
  color: #007bff; /* Cambiar el color al hacer hover */
  transition: color 0.3s ease; /* Suavizar el cambio de color */
}

/* Imagen de fondo */
.imag-fondo {
  position: relative;
  width: 100%;
  height: 762px;
  overflow: hidden;
}

.imag-fondo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
}

/* Estilo para el contenedor de texto */
.container-text-fondo {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 762px;
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px;
  box-sizing: border-box;
  margin: 0;
  z-index: 3;
}

.text-item {
  margin-bottom: 20px;
  text-align: center;
  z-index: 300;
}

.text-item h1 {
  font-family: "Montserrat", sans-serif;
  font-size: 46px;
  font-weight: 600;
  margin-bottom: 10px;
}

.text-item p {
  font-family: "Roboto", sans-serif;
  font-size: 14px;
  margin-bottom: 20px;
}

/* Estilo del botón */
button {
  padding: 10px 20px;
  background-color: #00b0f0;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-family: "Montserrat", sans-serif;
  font-size: 13px;
}

button:hover {
  background-color: #febf01;
}

/* Estilos para la sección acordeón */

.accordion-container {
  width: 100%;
  max-width: 600px;
  margin: 0 auto;
}

.accordion-item {
  margin-bottom: 10px;
}
.container-acordeon .container-title-acordeon h1 {
  color: #f9fafb;
  font-family: 'Montserrat', sans-serif;
  font-size: 38px;
  font-weight: 600;
  margin: 0;
  padding: 10px;
}

.accordion-header {
  width: 100%;
  padding: 15px;
  text-align: left;
  background-color: #00b0f0; /* Color actualizado */
  color: #fff; /* Color actualizado */
  font-family: 'Montserrat', sans-serif; /* Tipografía Montserrat */
  font-weight: 600;
  font-size: 1.2rem;
  border: none;
  cursor: pointer;
  text-transform: uppercase;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.accordion-header i {
  margin-left: 10px;
  font-size: 1.2rem;
  transition: transform 0.3s; /* Animación suave para los íconos */
}

.accordion-header:hover {
  background-color: #ff6900;
}

.accordion-content {
  display: none;
  padding: 15px;
  background-color: #ff6900; /* Color actualizado */
  border-radius: 5px;
  font-family: 'Roboto', sans-serif; /* Tipografía Roboto */
  font-size: 1rem;
}

.accordion-content p {
  margin: 0;
}


.container-acordeon-div-cards {
  display: grid; /* Usamos grid para crear filas y columnas */
  grid-template-columns: repeat(2, 1fr); /* 2 columnas, cada una ocupa el 50% */
  gap: 10px; /* Espacio entre las tarjetas */
}

.container-acordeon-cards {
  background-color: #00b0f0;
  padding: 20px;
  border-radius: 5px;
  text-align: center;
  min-height: 150px; /* Altura mínima para las tarjetas */
  color: #fff;
}

/* Acomodar el accordion-container y container-acordeon horizontalmente */

.container-acordeon-div {
  display: flex; /* Usamos flexbox para poner los elementos uno al lado del otro */
  gap: 20px; /* Espacio entre los dos contenedores */
  flex-wrap: wrap; /* Permite que los elementos se envuelvan en pantallas pequeñas */
  justify-content: space-between; /* Distribuye el espacio entre los elementos */
}

.accordion-container,
.container-acordeon {
  flex: 1; /* Cada elemento ocupa el mismo espacio */
  max-width: 48%; /* Limita el ancho de cada contenedor al 48% */
}



@media (max-width: 1024px) {
  .container-title-seccion h1 {
    font-size: 2rem; /* Reducir tamaño del título */
  }

  .imag-fondo {
    height: 500px; /* Ajustar la altura de la imagen de fondo */
  }

  .container-text-fondo {
    height: 500px; /* Ajustar la altura del contenedor de texto */
  }

  .text-item h1 {
    font-size: 36px; /* Reducir tamaño del texto */
  }

  .text-item p {
    font-size: 16px; /* Aumentar ligeramente el tamaño del párrafo */
  }
  .container-acordeon-div {
    flex-direction: row; /* Se mantienen en fila */
    gap: 20px; /* Espacio entre los elementos */
  }

  .accordion-container,
  .container-acordeon {
    max-width: 48%; /* Mantiene el 48% de ancho para cada contenedor */
  }

  .container-acordeon-div-cards {
    display: grid; /* Utiliza grid para las tarjetas */
    grid-template-columns: repeat(2, 1fr); /* Dos columnas */
  }

  .container-acordeon-cards {
    width: 100%;
  }
}

/* Para dispositivos móviles (pantallas menores de 768px) */
/* Media Queries para dispositivos pequeños */
@media (max-width: 768px) {
  .container-title-seccion h1 {
    font-size: 1.5rem; /* Reducir más el tamaño del título */
  }

  .imag-fondo {
    height: 400px; /* Reducir la altura de la imagen de fondo */
  }

  .container-text-fondo {
    height: 400px; /* Reducir la altura del contenedor de texto */
    padding: 10px; /* Reducir el padding */
  }

  .text-item h1 {
    font-size: 28px; /* Reducir tamaño del texto */
  }

  .text-item p {
    font-size: 14px; /* Ajustar tamaño del párrafo */
  }

  .text-item button {
    padding: 10px 20px; /* Ajustar tamaño del botón */
    font-size: 14px; /* Ajustar tamaño de fuente del botón */
  }
  .container-acordeon-div {
    flex-direction: column; /* Los elementos se apilan verticalmente */
    align-items: center; /* Centra los elementos */
  }

  .accordion-container,
  .container-acordeon {
    max-width: 100%; /* Ocupan el 100% del ancho */
    margin-bottom: 20px; /* Espaciado entre los contenedores */
  }

  .container-acordeon-div-cards {
    display: block; /* Cambia de grid a bloque */
  }

  .container-acordeon-cards {
    width: 100%; /* Ocupa el 100% del ancho */
    margin-bottom: 15px; /* Espacio entre las tarjetas */
  }
}

</style>
