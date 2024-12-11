<template>
  <div class="slider-container">
    <h1 class="slider-title">
      WHEN YOU MOVE WITH US,
      <br />IT'S ALMOST FUN
    </h1>
    <section class="zipcode">
      <div class="ancho">
        <div class="container-flex-zipcode">
          <div class="zipcode-fields">
            <h2>Get your estimate today!</h2>
          </div>
          <div class="zipcode-fields">
            <div class="field">
              <p>Moving From</p>
              <input type="number" class="number-input" />
            </div>
            <div class="field">
              <p>Moving To</p>
              <input type="number" class="number-input" />
            </div>
            <div class="field">
              <button class="go-button">GO!</button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <swiper
      ref="swiperRef"
      :modules="modules"
      :slides-per-view="1"
      :autoplay="{ delay: 3000, disableOnInteraction: false }"
      class="swiper-container"
      @swiper="onSwiperInit"
    >
      <swiper-slide>
        <img
          src="../assets/slide-1.jpg"
          alt="Slide 1"
          class="swiper-slide-image"
        />
      </swiper-slide>
      <swiper-slide>
        <img
          src="../assets/slide-2.jpg"
          alt="Slide 2"
          class="swiper-slide-image"
        />
      </swiper-slide>
      <swiper-slide>
        <img
          src="../assets/slide-3.jpg"
          alt="Slide 3"
          class="swiper-slide-image"
        />
      </swiper-slide>
    </swiper>


    <button class="custom-prev" @click="goToPrev">
      <i class="fa-solid fa-chevron-left"></i>
    </button>
    <button class="custom-next" @click="goToNext">
      <i class="fa-solid fa-chevron-right"></i>
    </button>
  </div>
 
  <section class="home-container">
    <div class="container-inner">
      <div class="flex-container">
        <div class="section-container">
          <div class="text-container">
            <h2>Our mission is to move you, <br />not just your boxes.</h2>
            <h3>
              We’re a professional local moving company created to move more
              than just your boxes. <br />We’ll move you with our hard work and
              genuine smiles.
            </h3>
          </div>
        </div>
        <div class="section-container">
          <div class="box-container">
            <div class="icon-container">
              <a href="">
                <i class="fa-solid fa-house"></i>
              </a>
            </div>
            <div class="text-box-container">
              <h2>Local Moving</h2>
              <h3>
                We offer a comprehensive menu of moving services to suit your
                needs, timescale and budget.
              </h3>
            </div>
          </div>
          <div class="box-container">
            <div class="icon-container">
              <a href="">
                <i class="fa-solid fa-location-dot"></i>
              </a>
            </div>
            <div class="text-box-container">
              <h2>Long Distance</h2>
              <h3>
                We provide with long distance and international moving to keep
                your property in safe.
              </h3>
            </div>
          </div>
          <div class="box-container">
            <div class="icon-container">
              <a href="">
                <i class="fa-solid fa-briefcase"></i>
              </a>
            </div>
            <div class="text-box-container">
              <h2>Moving Your Business</h2>
              <h3>
                We have expertise and resources to plan and implement an
                effective office removal to ensure business continuity for you.
              </h3>
            </div>
          </div>
          <div class="box-container">
            <div class="icon-container">
              <a href="">
                <i class="fa-solid fa-box"></i>
              </a>
            </div>
            <div class="text-box-container">
              <h2>Storage</h2>
              <h3>
                We are the largest provider of storage facilities in the US,
                providing safe and secure furniture storage.
              </h3>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="container-home2">
    <div class="ancho">
      <div class="container-section">
        <div class="container-texto">
          <h2>The ways we move you.</h2>
        </div>
      </div>
      <div class="container-section">
        <div class="container-full-cards">
          <div class="container-cards">
            <div class="container-img">
              <img src="../assets/home-1-2-300x225.jpg" />
            </div>
            <div class="container-cards-text">
              <h3>How we move</h3>
              <p>
                After you ordered the service and left all your requirements, we
                make an appointment at your convenience and make preparations
                for moving.
              </p>
            </div>
            <div class="container-cards-button">
              <button>GET MOVING</button>
            </div>
          </div>
          <div class="container-cards">
            <div class="container-img">
              <img src="../assets/home-1-2-300x225.jpg" />
            </div>
            <div class="container-cards-text">
              <h3>How we move</h3>
              <p>
                After you ordered the service and left all your requirements, we
                make an appointment at your convenience and make preparations
                for moving.
              </p>
            </div>
            <div class="container-cards-button">
              <button>GET MOVING</button>
            </div>
          </div>
          <div class="container-cards">
            <div class="container-img">
              <img src="../assets/home-1-2-300x225.jpg" />
            </div>
            <div class="container-cards-text">
              <h3>How we move</h3>
              <p>
                After you ordered the service and left all your requirements, we
                make an appointment at your convenience and make preparations
                for moving.
              </p>
            </div>
            <div class="container-cards-button">
              <button>GET MOVING</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="container-home2">
    <div class="ancho">
      <div class="container-section">
        <div class="container-full-video">
          <div class="container-video-text">
            <div>
              <h2>Discover why we're everyone's favorite local movers!</h2>
            </div>
            <div>
              We helped thousands of people to move! We worked either with
              businesses and individual households and gained our reputation.
            </div>
            <div>
              <p>
                This was the third time I had used JohnnyGo and I would use them
                again. The company responded to my initial inquiry very promptly
                and I thought the quote was fair. Their packing team arrived on
                time and were incredibly efficient. At all times I was kept
                informed and expectations were met throughout the process.
              </p>
            </div>
          </div>
          <div class="container-video-div">
            <div class="container-video">
              <iframe
                width="560"
                height="315"
                src="https://www.youtube.com/embed/BWixkyze7PA?si=9uHUorPrL12k6nOS"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin"
                allowfullscreen
              ></iframe>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
<br> <br>
  <section class="container-home2">
    <div class="container-img-f">
      <img src="../assets/home-cta-bg.png" />
      <div class="ancho">
        <div class="display-flex">
          <div class="container-secction">
            <div class="container-img-vacio"></div>
          </div>
          <div class="container-secction">
            <div class="container-img-texto">
              <h2>
                Call us today <br />
                <span>(719) 445-2808</span>
              </h2>
              <div>
                Monday to Saturday 8 a.m. to 10 p.m. and Sunday 9:30 a.m. to
                5:30 p.m. Eastern
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section><!---->
</template>

<script>
import { Autoplay } from "swiper/modules";
import { Swiper, SwiperSlide } from "swiper/vue";
import { ref } from "vue";
import "swiper/css";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const swiperRef = ref(null); // Referencia al swiper

    // Método para manejar el evento de inicialización de Swiper
    const onSwiperInit = (swiper) => {
      swiperRef.value = swiper; // Guardamos la instancia de Swiper en la referencia
    };

    // Método para avanzar a la siguiente diapositiva
    const goToNext = () => {
      if (swiperRef.value) {
        swiperRef.value.slideNext(); // Navegar al siguiente slide
      }
    };

    // Método para retroceder a la diapositiva anterior
    const goToPrev = () => {
      if (swiperRef.value) {
        swiperRef.value.slidePrev(); // Navegar al slide anterior
      }
    };

    return {
      modules: [Autoplay],
      swiperRef,
      onSwiperInit,
      goToNext,
      goToPrev,
    };
  },
};
</script>

<style scoped>
.ancho {
  max-width: 1200px; /* Limita el ancho máximo a 1200px */
  width: 100%; /* Ocupa todo el ancho del contenedor padre */
  margin: 0 auto; /* Centra horizontalmente */
  box-sizing: border-box; /* Incluye padding en el cálculo del ancho */
}

.ancho2 {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  justify-content: space-between;
}
/* Contenedor principal del slider */
.slider-container {
  width: 100%;
  margin: 0;
  overflow: hidden;
  position: relative; /* Para posicionar el título sobre el slider */
}

/* Título del slider */
.slider-title {
  font-size: 4rem;
  font-weight: 500;
  font-family: "system-ui";
  text-align: center;
  position: absolute; /* Para colocar el título sobre el slider */
  top: 50%; /* Centra el título verticalmente */
  left: 50%; /* Centra el título horizontalmente */
  transform: translate(
    -50%,
    -50%
  ); /* Ajusta la posición para el centro exacto */
  z-index: 1; /* Ajustamos el z-index para que esté por encima del slider */
  width: 70%; /* Permite que el título ocupe un 80% del ancho del contenedor */
  color: #fff; /* Asegura que el texto sea visible sobre las imágenes */
}

/* Contenedor del slider */
.swiper-container {
  width: 100%;
  position: relative;
  z-index: 0; /* Slider estará detrás de la sección zipcode */
}

/* Imagen del slider */
.swiper-slide-image {
  width: 100%;
  height: 550px;
  object-fit: cover;
  transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
}

.custom-prev,
.custom-next {
  background-color: #fff;
  color: #000;
  font-size: 1.5rem;
  border: none;
  padding: 0; /* Elimina el padding para que el tamaño sea consistente */
  width: 50px; /* Tamaño del botón (ajustable según tu preferencia) */
  height: 50px; /* Asegura que el alto sea igual al ancho */
  border-radius: 50%; /* Hace que el botón sea completamente circular */
  cursor: pointer;
  z-index: 1000;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  display: inline-flex;
  align-items: center;
  justify-content: center;
}

.custom-prev {
  left: 20px;
}

.custom-next {
  right: 20px;
}

.custom-prev:hover,
.custom-next:hover {
  color: #00b0f0;
  border: none;
}

/* Estilo general de la sección */
.zipcode {
  display: flex;
  justify-content: center; /* Centra el contenido de la sección */
  width: 100%;
  padding: 40px 0;
  background-color: #000000a8;
  position: fixed;
  bottom: 0;
  left: 0;
  z-index: 1;
  position: absolute;
}

/* Contenedor para limitar el ancho a 1200px */
.zipcode-container {
  width: 100%;
  max-width: 1200px;
  padding: 0 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* Nuevo contenedor con display: flex para los campos */
.container-flex-zipcode {
  display: flex;
  justify-content: space-between; /* Espaciado entre los div de zipcode-fields */
  width: 100%;
  gap: 20px; /* Espacio entre los campos */
}

/* Estilo para los campos (zipcode-fields) */
.zipcode-fields {
  display: flex; /* Cambiado de columna a fila */
  justify-content: space-between; /* Distribuye el contenido horizontalmente */
  flex-direction: row; /* Cambia la dirección a fila */
  width: 48%; /* Ajustamos el tamaño para que quepan bien en el espacio */
}

/* Estilo para los campos (cada .field) */
.field {
  display: flex;
  flex-direction: column; /* Alinea el contenido en columna (p y input) */
  align-items: center;
  justify-content: center;
  width: 33.33%; /* Hace que cada campo ocupe el 33% del espacio disponible */
  box-sizing: border-box;
}

.field p {
  font-size: 16px;
  margin-bottom: 5px;
}

.number-input {
  font-size: 16px;
  padding: 5px;
  width: 70%; /* Hace que el input ocupe el 70% del espacio disponible */
  box-sizing: border-box;
  border: 1px solid #ccc;
  border-radius: 4px;
  background-color: #fff;
}

.go-button {
  background-color: #00b0f0;
  color: white;
  border: none;
  padding: 20px 30px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
  transition: background-color 0.3s;
  margin-top: 10px;
}

.go-button:hover {
  background-color: #febf01;
}

/* Contenedor principal */
.container-home2 {
  padding: 20px; /* Espaciado interno */
  color: black; /* Texto negro */
}

.container-secction {
  width: 100%; /* Asegura que cada sección ocupe todo el ancho del contenedor */
  margin: 0; /* Elimina márgenes que puedan afectar el diseño */
  padding: 0; /* Elimina padding adicional */
  display: flex;
  flex-direction: row; /* Organiza los elementos horizontalmente */
  justify-content: space-between; /* Ajusta la posición de los elementos hijos */
  box-sizing: border-box; /* Incluye padding en el cálculo del ancho */
}

/* Nueva clase para el contenedor principal */
.home-container {
  padding: 20px;
  width: 100%;
  background-color: #f4f4f4; /* Fondo claro para visibilidad */
}

/* Contenedor interno con ancho máximo */
.container-inner {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
  box-sizing: border-box;
}

/* Contenedor con disposición flex y centrado */
.flex-container {
  display: flex;
  flex-direction: row;
  gap: 20px;
  width: 100%;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Cada sección con diseño en fila */
.section-container {
  display: flex;
  flex-wrap: wrap; /* Permite que los elementos se acomoden si el espacio es pequeño */
  justify-content: space-between;
  width: 100%;
  box-sizing: border-box;
}

/* Contenedor de texto centrado dentro de .section-container */
.text-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  gap: 10px;
  padding: 20px;
  border-radius: 8px;
  color: black;
  width: 100%;
  box-sizing: border-box;
}

/* Estilo para los títulos */
.text-container h2 {
  font-size: 32px;
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  color: #00b0f0;
  margin: 0;
}

.text-container h3 {
  font-size: 16px;
  font-family: "Roboto", sans-serif;
  font-weight: 400;
  color: black;
  margin: 0;
}

/* Estilo para las cajas */
.box-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 15px;
  padding: 20px;
  border-radius: 8px;
  flex: 1;
  max-width: 48%;
  box-sizing: border-box;
  color: black;
}

/* Contenedor del ícono */
.icon-container {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 2rem;
  color: white;
  background-color: #00b0f0;
  width: 80px;
  height: 80px;
  border-radius: 50%;
}
/* Cambiar el color de los íconos a blanco */
.icon-container i {
  color: white; /* Color blanco para los íconos */
}

/* Contenedor de texto dentro de las cajas */
.text-box-container {
  text-align: center;
}

/* Estilo del título h2 dentro de .text-box-container */
.text-box-container h2 {
  font-family: "Montserrat", sans-serif;
  font-size: 18px;
  font-weight: 400;
  margin-bottom: 5px;
}

/* Estilo del subtítulo h3 dentro de .text-box-container */
.text-box-container h3 {
  font-family: "Roboto", sans-serif;
  font-size: 14px;
  color: #666;
}

/* Contenedor para alinear las cards horizontalmente */
.container-full-cards {
  display: flex; /* Flexbox para organizar horizontalmente */
  gap: 10px; /* Espacio reducido entre las cards */
  justify-content: space-between; /* Distribuye las cards uniformemente */
  flex-wrap: nowrap; /* Evita que las cards se envuelvan */
  overflow-x: auto; /* Permite scroll horizontal si no caben */
  padding: 10px 0; /* Espaciado superior e inferior */
}

/* Estilo de las cards individuales */
.container-cards {
  flex: 0 0 30%; /* Cada card ocupa el 30% del contenedor */
  max-width: 30%; /* Limita el ancho al 30% */
  padding: 15px; /* Espaciado interno */
  box-sizing: border-box; /* Incluye el padding en el ancho total */
  transition: transform 0.3s ease; /* Efecto hover */
}

.container-cards:hover {
  transform: translateY(-5px); /* Animación al pasar el mouse */
}

/* Estilo de las imágenes dentro de las cards */
.container-img {
  width: 100%; /* Ocupa el ancho completo del contenedor */
  height: auto; /* Mantiene la proporción de la imagen */
  margin-bottom: 10px; /* Espaciado inferior entre la imagen y el texto */
  display: flex; /* Asegura que la imagen esté centrada */
  justify-content: center;
  align-items: center;
}

.container-img img {
  width: 300px; /* Ancho fijo de la imagen */
  height: 225px; /* Alto fijo de la imagen */
  object-fit: cover; /* Recorta la imagen para que encaje en las dimensiones */
}






/* Texto dentro de las cards */
.container-cards-text h3 {
  font-family: "Montserrat", sans-serif;
  font-size: 18px;
  font-weight: 600; /* Letra delgada */
  color: #333;
  margin-bottom: 10px;
}

.container-cards-text p {
  font-family: "Roboto", sans-serif;
  font-size: 14px;
  font-weight: 300; /* Letra delgada */
  color: #666;
  margin-bottom: 15px;
  line-height: 1.5;
}

/* Botón dentro de las cards */
.container-cards-button button {
  font-family: "Montserrat", sans-serif;
  font-size: 13px;
  font-weight: 300; /* Letra delgada */
  color: #fff;
  background-color: #007bff;
  padding: 10px 15px;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.container-cards-button button:hover {
  background-color: #0056b3; /* Color más oscuro al pasar el mouse */
}

.container-full-video {
  display: flex;
  justify-content: space-between; /* Distribuye el espacio entre los elementos */
  align-items: center; /* Centra verticalmente los elementos */
  gap: 2rem; /* Espacio entre los elementos */
  width: 100%;
  padding: 2rem; /* Añadimos padding alrededor para más espacio */
}

.container-video-text {
  display: flex;
  flex-direction: column;
  gap: 0; /* Elimina el espacio entre los elementos */
  width: 50%; /* Ocupa la mitad del contenedor */
}

.container-video-text h2 {
  font-family: "Montserrat", sans-serif;
  font-weight: 700; /* Negrita */
  font-size: 32px;
  text-align: left;
  margin-bottom: 0; /* Elimina el margen debajo */
  color: #00aeef;
}
/* Estilo para el primer div que sigue al h2 */
.container-video-text > div:nth-child(2) {
  font-family: "Montserrat", sans-serif;
  font-weight: 300; /* Ligera */
  font-size: 16px;
  text-align: left;
  margin-top: 0; /* Elimina el margen encima */
  margin-bottom: 0; /* Elimina el margen debajo */
}

/* Estilo para el div con el p adentro */
.container-video-text p {
  font-family: "Roboto", sans-serif;
  font-weight: 300; /* Ligera */
  font-size: 14px;
  text-align: left;
  margin-top: 0; /* Elimina el margen encima */
  margin-bottom: 0; /* Elimina el margen debajo */
  color: #79787f;
}
.container-video-text div {
  padding: 1rem;
}

.container-video-div {
  display: flex;
  justify-content: center; /* Centra horizontalmente */
  align-items: center; /* Centra verticalmente */
  height: 400px; /* Ajusta la altura a lo que necesites */
  width: 50%; /* Ocupa la mitad del contenedor */
}

.container-video {
  position: relative; /* Para asegurarnos de que el iframe se ajuste dentro del contenedor */
  width: 100%;
  height: 100%;
}

.container-video iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: none;
  object-fit: cover; /* Hace que el video ocupe todo el espacio sin márgenes */
}

.container-img-f {
  position: relative;
  width: 100%;
}

.container-img-f img {
  width: 100%; /* Hace que la imagen ocupe todo el ancho */
  object-fit: cover; /* Asegura que la imagen se ajuste correctamente */
  height: auto; /* Mantiene la relación de aspecto */
  transform: scale(1.5); /* Aumenta el tamaño de la imagen un 20% */
}

.display-flex {
  display: flex;
  position: absolute; /* Hace que se posicione encima de la imagen */
  top: -20%; /* Ajusta la posición hacia arriba en un 10% */
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

.container-secction {
  width: 50%; /* Hace que cada sección ocupe el 50% */
}

.container-img-vacio {
  background-color: transparent; /* Mantén la caja vacía transparente */
  height: 100%; /* Ocupará la altura del contenedor */
}

.container-img-texto {
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center; /* Centra los elementos verticalmente si es necesario */
  text-align: right; /* Alinea todo el texto dentro de este contenedor a la derecha */
}

.container-img-texto h2 {
  font-family: "Montserrat", sans-serif;
  font-size: 32px;
  color: #fff; /* Color negro para el texto */
}

.container-img-texto h2 span {
  font-family: "Montserrat", sans-serif;
  color: #ffffff;
  font-size: 46px;
}

.container-img-texto div {
  font-family: "Roboto", sans-serif;
  margin-top: 10px;
  font-size: 14px;
  color: #fff; /* Color negro para el texto */
}







  /* Cambiar la disposición de los contenedores de las secciones para dispositivos móviles */
  .flex-container {
    flex-direction: column; /* Asegura que los contenedores se apilen verticalmente */
  }

  /* Cambiar la disposición de los box-container para que se apilen verticalmente */
  .box-container {
    max-width: 100%; /* Cada box-container ocupará el 100% del ancho */
    margin-bottom: 20px; /* Agrega espacio entre las cajas */
  }

  /* Asegura que el texto dentro de .text-container tenga un buen espaciado en pantallas pequeñas */
  .text-container {
    padding: 20px; /* Asegura suficiente espacio alrededor del texto */
  }

  /* Estilo de los iconos para pantallas pequeñas */
  .icon-container {
    width: 70px; /* Reducir el tamaño del ícono */
    height: 70px; /* Reducir el tamaño del ícono */
    font-size: 1.5rem; /* Reducir el tamaño del ícono */
  }








/* Generalmente, no se necesitan cambios hasta los tamaños pequeños */

@media (min-width: 768px) and (max-width: 1124px) { /* Tabletas */
  /* Ajustar el título en el slider */
  .slider-title {
    font-size: 3rem; /* Reducir el tamaño del texto */
    width: 80%; /* Reducir el ancho del título */
  }

  /* Ajustar el contenedor de las imágenes en el slider */
  .swiper-slide-image {
    height: 400px; /* Ajustar la altura para pantallas más pequeñas */
  }

  /* Ocultar las flechas del slider en tabletas */
  .custom-prev,
  .custom-next {
    display: none; /* Ocultar las flechas */
  }

  /* Desactivar el scroll horizontal */
  .swiper-container {
    overflow-x: hidden; /* Elimina el scroll horizontal */
  }

  /* Hacer que el contenedor de las tarjetas se adapte a la pantalla */
  .container-full-cards {
    flex-wrap: wrap; /* Permitir que las cards se acomoden en varias filas */
    justify-content: center; /* Centrar las cards */
  }

  .container-cards {
    flex: 0 0 45%; /* Hacer que las tarjetas ocupen el 45% del ancho */
    max-width: 45%;
    margin-bottom: 20px; /* Espacio entre las tarjetas */
  }

  /* Ajustar el tamaño de las imágenes dentro de las cards */
  .container-img {
    height: 250px; /* Reducir la altura de las imágenes */
  }

  /* Ajustes para el contenedor del zipcode */
  .zipcode {
    padding: 20px 0; /* Ajustar padding */
    display: none; /* Ocultar la sección de zipcode */
  }

  .container-flex-zipcode {
    flex-direction: column; /* Colocar los campos de zipcode en columna */
    gap: 20px; /* Añadir espacio entre los campos */
  }

  .zipcode-fields {
    width: 100%; /* Ajustar los campos para que ocupen el 100% */
  }

  .go-button {
    padding: 15px 25px; /* Reducir el tamaño del botón */
    font-size: 14px; /* Reducir tamaño de la fuente */
  }

    /* Cambiar la disposición de los contenedores de las secciones para dispositivos móviles */
    .flex-container {
    flex-direction: column; /* Asegura que los contenedores se apilen verticalmente */
  }

  /* Cambiar la disposición de los box-container para que se apilen verticalmente */
  .box-container {
    max-width: 100%; /* Cada box-container ocupará el 100% del ancho */
    margin-bottom: 20px; /* Agrega espacio entre las cajas */
  }

  /* Asegura que el texto dentro de .text-container tenga un buen espaciado en pantallas pequeñas */
  .text-container {
    padding: 20px; /* Asegura suficiente espacio alrededor del texto */
  }

  /* Estilo de los iconos para pantallas pequeñas */
  .icon-container {
    width: 70px; /* Reducir el tamaño del ícono */
    height: 70px; /* Reducir el tamaño del ícono */
    font-size: 1.5rem; /* Reducir el tamaño del ícono */
  }

  /* Ajustar el tamaño del texto en pantallas pequeñas */
  .text-container h2 {
    font-size: 28px; /* Reducir tamaño del título principal */
  }

  .text-container h3 {
    font-size: 14px; /* Reducir tamaño del subtítulo */
  }

  .text-box-container h2 {
    font-size: 16px; /* Reducir tamaño del título dentro de las cajas */
  }

  .text-box-container h3 {
    font-size: 12px; /* Reducir tamaño del subtítulo dentro de las cajas */
  }


  .container-cards-text h3 {
    font-size: 17px;
  }

  .container-cards-text p {
    font-size: 13px;
  }

  .container-cards-button button {
    font-size: 12px;
    padding: 8px 12px;
  }

  /* Ajustar el tamaño de la imagen */
  .container-img img {
    width: 100%;
    height: auto;
  }

  .container-full-cards {
    display: flex;
    flex-wrap: wrap; /* Asegurar que las tarjetas se distribuyan correctamente */
    gap: 2rem; /* Espacio entre las tarjetas */
  }

  .container-cards {
    width: 45%; /* Las tarjetas ocupan el 45% del ancho */
  }
}


@media (max-width: 768px) { /* Móviles */
  /* Ajustes para el título en el slider */
  .slider-title {
    font-size: 2.5rem; /* Reducir aún más el tamaño del título */
    width: 90%; /* Hacer el título más pequeño en móvil */
  }

  /* Ajustar la altura de las imágenes del slider */
  .swiper-slide-image {
    height: 300px; /* Asegurar que las imágenes no sean tan grandes */
  }

  /* Ocultar las flechas del slider en móviles */
  .custom-prev,
  .custom-next {
    display: none; /* Ocultar las flechas */
  }

  /* Desactivar el scroll horizontal */
  .swiper-container {
    overflow-x: hidden; /* Elimina el scroll horizontal */
  }

  /* Las tarjetas en móvil ocupan el 100% del ancho */
  .container-cards {
    flex: 0 0 100%; /* Las tarjetas ocupan el 100% en pantallas pequeñas */
    max-width: 100%;
    margin-bottom: 20px; /* Añadir espacio entre las tarjetas */
  }

  /* Ajustar la altura de las imágenes dentro de las cards */
  .container-img {
    height: 250px; /* Reducir la altura de las imágenes */
  }

  /* Ajustes para el contenedor del zipcode */
  .zipcode {
    padding: 10px 0; /* Ajustar padding */
    display: none; /* Ocultar la sección de zipcode */
  }

  .container-flex-zipcode {
    flex-direction: column; /* Colocar los campos de zipcode en columna */
    gap: 20px; /* Añadir espacio entre los campos */
  }

  .zipcode-fields {
    width: 100%; /* Ajustar los campos para que ocupen el 100% */
  }

  .go-button {
    padding: 10px 20px; /* Reducir el tamaño del botón */
    font-size: 12px; /* Reducir tamaño de la fuente */
  }


  .flex-container {
    flex-direction: column; /* Los elementos se apilan verticalmente */
  }

  .section-container {
    flex-direction: column; /* Los box-container se apilan verticalmente */
    align-items: center; /* Centra los elementos dentro de la sección */
  }

  .box-container {
    max-width: 100%; /* Los box-container ocupan el 100% del ancho en pantallas pequeñas */
    margin-bottom: 20px; /* Espacio entre las cajas */
  }

  .icon-container {
    width: 70px; /* Reducir el tamaño del ícono */
    height: 70px; /* Reducir el tamaño del ícono */
    font-size: 1.5rem; /* Reducir el tamaño del ícono */
  }

  .text-container h2 {
    font-size: 36px; /* Reducir tamaño del título principal */
  }

  .text-container h3 {
    font-size: 20px; /* Reducir tamaño del subtítulo */
  }

  .text-box-container h2 {
    font-size: 26px; /* Reducir tamaño del título dentro de las cajas */
  }

  .text-box-container h3 {
    font-size: 22px; /* Reducir tamaño del subtítulo dentro de las cajas */
  }



  .container-cards-text h3 {
    font-size: 18px;
  }

  .container-cards-text p {
    font-size: 14px;
  }

  .container-cards-button button {
    font-size: 13px;
    padding: 10px 15px;
  }

  .container-img img {
    width: 100%;
    height: auto;
  }

  .container-full-cards {
    display: flex;
    gap: 2rem; /* Espacio entre las tarjetas */
  }

  .container-cards {
    width: 30%; /* Las tarjetas ocupan el 30% del ancho */
  }

  .container-full-video {
    flex-direction: column; /* Cambia la dirección a columna */
    gap: 1.5rem; /* Añade más espacio entre los elementos */
  }

  .container-video-text,
  .container-video-div {
    width: 100%; /* Ocupa el 100% del ancho */
  }

  .container-video-div {
    height: 250px; /* Reduce la altura del video */
  }

  .container-video-text h2 {
    font-size: 24px; /* Reduce el tamaño del título */
  }

  .container-video-text > div:nth-child(2) {
    font-size: 14px; /* Reduce el tamaño de la descripción */
  }

  .container-video-text p {
    font-size: 12px; /* Reduce el tamaño del párrafo */
  }
  .container-video-text h2 {
    font-size: 20px; /* Reduce aún más el tamaño del título */
  }

  .container-video-text > div:nth-child(2) {
    font-size: 12px; /* Reduce aún más el tamaño de la descripción */
  }

  .container-video-text p {
    font-size: 10px; /* Reduce aún más el tamaño del párrafo */
  }

  .display-flex {
    top: 0; /* Ajusta la posición */
    flex-direction: column; /* Organiza los elementos en columna */
  }

  .container-secction {
    width: 100%; /* En móviles, las secciones ocupan el 100% */
    margin-bottom: 20px; /* Espacio entre secciones */
  }

  .container-img-f {
    display: none; /* Oculta toda la sección en móviles */
  }
}

</style>
