<template>
  <section class="container-section">
    <div class="ancho">
      <div></div>
    </div>
  </section>
  <section class="container-section">
    <div class="ancho">
      <div>
        <div class="container-title-seccion">
          <h1>Team</h1>
        </div>
      </div>
    </div>
  </section>

  <section class="container-section">
    <div class="ancho">
      <div class="container-team">
        <div class="container-team-title">
          <h2>Our Team</h2>
        </div>
        <div div class="container-team-p">
          Experienced and skilled repairmen will free you from many problems!
          You’ll definitely will be pleased with the result as we guarantee the
          best service!
        </div>
        <div div class="container-team-img-div">
          <div class="container-team-img-div-div">
            <div class="container-team-img">
              <img src="../assets/team1.jpg" />
              <div class="container-team-img-buton">
                <div>
                  <h3>
                    Jim Harris <br />
                    <span> Senior electrician</span>
                  </h3>
                  <p>
                    Jim has over 10 years of experience working as an
                    electrician here. Jim knows about plumbing everything and
                    even more!
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="container-team-img-div-div">
            <div class="container-team-img">
              <img src="../assets/team2.jpg" />
              <div class="container-team-img-buton">
                <div>
                  <h3>
                    Jim Harris <br />
                    <span> Senior electrician</span>
                  </h3>
                  <p>
                    Jim has over 10 years of experience working as an
                    electrician here. Jim knows about plumbing everything and
                    even more!
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="container-team-img-div-div">
            <div class="container-team-img">
              <img src="../assets/team3.jpg" />
              <div class="container-team-img-buton">
                <div>
                  <h3>
                    Jim Harris <br />
                    <span> Senior electrician</span>
                  </h3>
                  <p>
                    Jim has over 10 years of experience working as an
                    electrician here. Jim knows about plumbing everything and
                    even more!
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="container-team-img-div-div">
            <div class="container-team-img">
              <img src="../assets/team4.jpg" />
              <div class="container-team-img-buton">
                <div>
                  <h3>
                    Jim Harris <br />
                    <span> Senior electrician</span>
                  </h3>
                  <p>
                    Jim has over 10 years of experience working as an
                    electrician here. Jim knows about plumbing everything and
                    even more!
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="container-team-img-div-div">
            <div class="container-team-img">
              <img src="../assets/team5.jpg" />
              <div class="container-team-img-buton">
                <div>
                  <h3>
                    Jim Harris <br />
                    <span> Senior electrician</span>
                  </h3>
                  <p>
                    Jim has over 10 years of experience working as an
                    electrician here. Jim knows about plumbing everything and
                    even more!
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="container-team-img-div-div">
            <div class="container-team-img">
              <img src="../assets/team6.jpg" />
              <div class="container-team-img-buton">
                <div>
                  <h3>
                    Jim Harris <br />
                    <span> Senior electrician</span>
                  </h3>
                  <p>
                    Jim has over 10 years of experience working as an
                    electrician here. Jim knows about plumbing everything and
                    even more!
                  </p>
                </div>
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

/* Estilos para la sección del equipo */
.container-team {
  width: 100%;
  background-color: #f9fafb; /* Fondo claro para la sección del equipo */
  padding: 2rem 1rem; /* Padding alrededor de la sección */
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.container-team-title {
  text-align: center; /* Centra el título */
  margin-bottom: 1.5rem; /* Espaciado debajo del título */
}

.container-team-title h2 {
  font-size: 2.5rem;
  font-weight: 600;
  color: #333;
}

.container-team-p {
  text-align: center;
  margin-bottom: 2rem;
}

.container-team-p p {
  font-size: 1.2rem;
  color: #555;
}

.container-team-img-div {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 columnas */
  grid-template-rows: repeat(2, auto); /* 2 filas */
  gap: 20px; /* Espacio entre los elementos */
}

.container-team-img-div-div {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.container-team-img-div {
  width: 100%; /* Asegura que las imágenes tengan el tamaño adecuado */
}

.container-team-img-div-div {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 1rem; /* Espacio entre las filas */
}

.container-team-img {
  width: 100%;
  max-width: 350px; /* Ajusta el tamaño máximo de la imagen */
  margin: 0.5rem; /* Espacio entre cada imagen */
}

.container-team-img img {
  width: 100%; /* Hace que la imagen ocupe todo el ancho del contenedor */
  height: auto; /* Mantiene la proporción de la imagen */
}

.container-team-img-buton {
  background-color: #fff;
  color: #333;
  padding: 1rem;
  text-align: center;
  width: 100%;
}

.container-team-img-buton h3 {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
}

.container-team-img-buton span {
  font-size: 1rem;
  font-weight: 400;
  color: #555;
}

.container-team-img-buton p {
  font-size: 1rem;
  color: #333;
  margin-top: 0.5rem;
  line-height: 1.5;
}

/* Grid layout para las imágenes */
.container-team-img-div {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 columnas */
  gap: 1rem; /* Espacio entre las columnas y filas */
  margin-top: 1rem;
}
@media (min-width: 768px) and (max-width: 1024px) {
  .container-team-img-div {
    grid-template-columns: repeat(2, 1fr); /* Dos columnas en tabletas */
    gap: 15px; /* Ajuste del espacio entre las columnas */
  }

  .container-team-img {
    max-width: 90%; /* Las imágenes ocupan el 90% del ancho en tabletas */
  }

  .container-team-img-buton h3 {
    font-size: 1.4rem; /* Ajusta el tamaño del título */
  }

  .container-team-img-buton p {
    font-size: 1rem; /* Ajusta el tamaño del texto */
  }

  .container-team-title h2 {
    font-size: 2.2rem; /* Título ligeramente más grande en tabletas */
  }
}
@media (max-width: 768px) {
  .container-team-img-div {
    grid-template-columns: 1fr; /* Una sola columna en dispositivos pequeños */
    gap: 10px; /* Reduce el espacio entre los elementos */
  }

  .container-team-img {
    max-width: 100%; /* Las imágenes ocupan el 100% del ancho del contenedor */
  }

  .container-team-img-buton h3 {
    font-size: 1.2rem; /* Ajusta el tamaño del título */
  }

  .container-team-img-buton p {
    font-size: 0.9rem; /* Ajusta el tamaño del texto */
  }

  .container-team-p p {
    font-size: 1rem; /* Ajusta el tamaño del texto descriptivo */
  }

  .container-team-title h2 {
    font-size: 2rem; /* Reduce el tamaño del título en dispositivos móviles */
  }
}
</style>
