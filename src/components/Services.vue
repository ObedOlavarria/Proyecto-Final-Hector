<template>
  <section class="container-section">
    <div class="ancho">
      <div class="container-title-seccion">
        <h1>Services</h1>
      </div>
    </div>
  </section>

  <section class="container-section">
    <div class="ancho">
      <div class="container-services">
        <div class="container-services-title">
          <h2>Our Services</h2>
        </div>
        <div div class="container-services-p">
          We provide services in all kinds of household work: from minor repairs
          to welding and landscaping
        </div>
        <div div class="container-services-img-div">
          <div class="container-services-img-div-div">
            <div class="container-services-img">
              <img src="../assets/Depo1.jpg" />
              <div class="container-services-img-buton">
                <button>
                  <i class="fa-solid fa-house"></i>
                  Local Moving
                </button>
              </div>
            </div>
          </div>
          <div class="container-services-img-div-div">
            <div class="container-services-img">
              <img src="../assets/Depos2.jpg" />
              <div class="container-services-img-buton">
                <button>
                  <i class="fa-solid fa-house"></i>
                  Local Moving
                </button>
              </div>
            </div>
          </div>
          <div class="container-services-img-div-div">
            <div class="container-services-img">
              <img src="../assets/Depos2.jpg" />
              <div class="container-services-img-buton">
                <button>
                  <i class="fa-solid fa-house"></i>
                  Local Moving
                </button>
              </div>
            </div>
          </div>
          <div class="container-services-img-div-div">
            <div class="container-services-img">
              <img src="../assets/Depos2.jpg" />
              <div class="container-services-img-buton">
                <button>
                  <i class="fa-solid fa-house"></i>
                  Local Moving
                </button>
              </div>
            </div>
          </div>
          <div class="container-services-img-div-div">
            <div class="container-services-img">
              <img src="../assets/Depos2.jpg" />
              <div class="container-services-img-buton">
                <button>
                  <i class="fa-solid fa-house"></i>
                  Local Moving
                </button>
              </div>
            </div>
          </div>
          <div class="container-services-img-div-div">
            <div class="container-services-img">
              <img src="../assets/Depos2.jpg" />
              <div class="container-services-img-buton">
                <button>
                  <i class="fa-solid fa-house"></i>
                  Local Moving
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

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
  font-family: "Gloock", sans-serif; /* Aplicar Gursa a los encabezados */
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
* {
  box-sizing: border-box; /* Esto asegura que el padding y el borde no afecten el ancho total */
}



/* Estilos para la sección de servicios */
.container-services {
  width: 100%;
  background-color: #f9fafb; /* Fondo claro para la sección de servicios */
  padding: 2rem 1rem; /* Padding alrededor de la sección */
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.container-services-title {
  text-align: center; /* Centra el título */
  margin-bottom: 1.5rem; /* Espaciado debajo del título */
}

.container-services-title h2 {
  font-size: 2.5rem;
  font-weight: 600;
  color: #333;
}

.container-services-p {
  text-align: center;
  margin-bottom: 2rem;
}

.container-services-p p {
  font-size: 1.2rem;
  color: #555;
}

.container-services-img-div {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 columnas */
  grid-template-rows: repeat(2, auto); /* 2 filas */
  gap: 20px; /* Espacio entre los elementos */
}

.container-services-img-div-div {
  display: flex;
  justify-content: center;
  align-items: center;
}

.container-services-img {
  width: 100%; /* Hace que el contenedor ocupe solo el 30% del ancho original */
  height: auto; /* Ajusta la altura automáticamente para mantener las proporciones */
  position: relative;
  overflow: hidden;
}

.container-services-img img {
  width: 100%; /* La imagen ocupa el 100% del tamaño del contenedor */
  height: 100%;
  object-fit: cover;
}

.container-services-img-buton {
  position: absolute; /* Permite posicionar el botón sobre la imagen */
  top: 50%; /* Posiciona el botón verticalmente en el centro */
  left: 50%; /* Posiciona el botón horizontalmente en el centro */
  transform: translate(
    -50%,
    -50%
  ); /* Ajusta el botón al 50% de su tamaño para centrarlo */
}

.container-services-img-buton button {
  background-color: #00b0f0;
  color: #fff;
  display: flex;
  flex-direction: column; /* Coloca el icono arriba y el texto abajo */
  justify-content: center; /* Centra el contenido verticalmente */
  align-items: center; /* Centra horizontalmente */
  font-family: "Montserrat", sans-serif; /* Usa la fuente Montserrat */
  font-size: 16px; /* Tamaño de la fuente */
  padding: 3rem 6rem; /* Ajuste de padding para que el botón sea adecuado */
  border: none; /* Sin borde */
  border-radius: 5px; /* Bordes redondeados */
  cursor: pointer; /* Cursor de mano */
  text-align: center; /* Asegura que el texto esté centrado */
  opacity: 0.8; /* Opacidad del botón */
  transition: opacity 0.3s ease; /* Transición suave al pasar el mouse */
}

.container-services-img-buton button:hover {
  background-color: #0056b3;
  opacity: 0.8; /* Aumenta la opacidad cuando se pasa el mouse */
}

.container-services-img-buton i {
  margin-bottom: 8px; /* Añade espacio entre el icono y el texto */
  font-size: 24px; /* Tamaño del icono */
}




@media (min-width: 768px) and (max-width: 1024px) {
  .container-services-img-div {
    grid-template-columns: repeat(2, 1fr); /* 2 columnas */
    grid-template-rows: auto;
  }

  .container-services-img-buton button {
    width: 100%; /* El botón ocupa todo el ancho disponible */
    padding: 2.5rem 5rem; /* Ajustamos el tamaño del padding */
  }
}
@media (max-width: 768px) {
  .container-services-img-div {
    grid-template-columns: 1fr; /* Colocamos todo en una columna */
    grid-template-rows: auto;
  }

  .container-services-img-buton button {
    width: 100%; /* El botón ocupa todo el ancho disponible */
    padding: 2rem; /* Reducimos el padding */
  }

  .container-services-img {
    margin-bottom: 1rem; /* Espaciado entre las imágenes */
  }
}
</style>
