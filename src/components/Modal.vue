<template>
    <section>
      <div>
        <!-- Todo el contenedor ahora abre el modal -->
        <div class="image-container" @click="openModal">
          <img
            src="../assets/slide-1.jpg"
            alt="Abrir Modal"
            class="cursor-pointer image-to-open-modal"
          />
          <div class="image-overlay">
            <p class="image-text">
              How we contact you?<br />
              We're always here to help!
            </p>
          </div>
        </div>
  
        <!-- Modal -->
        <div id="myModal" class="modal">
          <div class="modal-content">
            <div class="container-modal-div-form">
              <!-- Tachita para cerrar el modal -->
              <span class="close" @click="closeModal">&times;</span>
              <div class="container-modal-form left">
                <p>Want to receive the hottest news?</p>
                <p>Subscribe us to keep up-to-date!</p>
                <div>
                  <div class="container-forms">
                    <input type="number" class="number-input" />
                  </div>
                  <button class="suscribirce">SUBSCRIBE!</button>
                </div>
              </div>
              <div class="container-modal-form right">
                <div class="container-forms-img">
                  <img
                    src="../assets/Modal.png"
                    alt="img modal"
                    @click="openModal"
                    class="cursor-pointer"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>

  <script>
  import $ from "jquery"; // Importa jQuery
  
  export default {
    mounted() {
      // Abrir el modal al cargar el componente (al refrescar la página)
      this.openModal();
    },
    methods: {
      openModal() {
        // Usar jQuery para abrir el modal
        $("#myModal").fadeIn();
      },
      closeModal() {
        // Usar jQuery para cerrar el modal al hacer clic en la "X"
        $("#myModal").fadeOut();
      },
    },
  };
  </script>
  
  <style scoped>
/* Estilo para el contenedor que abre el modal */
.image-container {
  position: relative;
  display: inline-block;
  cursor: pointer;
  width: 80%; /* Asegura que el div sea del tamaño adecuado */
  height: auto;
}

.image-container:hover .image-to-open-modal {
  filter: grayscale(0%) !important; /* Eliminar filtro blanco y negro al hacer hover */
}

.image-container:hover .image-text {
  color: #FF0000 ; /* Cambiar color del texto al hacer hover */
}

.image-to-open-modal {
  width: 100%; /* Asegura que la imagen ocupe todo el contenedor */
  height: auto;
  filter: grayscale(100%) !important; /* Filtro blanco y negro por defecto */
  transition: filter 0.3s ease !important; /* Transición suave al quitar el filtro */
}

.image-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: transparent; /* Eliminado el efecto de opacidad */
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-text {
  font-family: 'Montserrat', sans-serif; /* Fuente Montserrat */
  font-size: 46px; /* Tamaño de la fuente */
  font-weight: 600; /* Peso de la fuente (grueso) */
  color: #007bff; /* Color azul */
  text-align: center;
  padding: 10px;
  transition: color 0.3s ease; /* Transición para el cambio de color */
}

/* Modal básico */
.modal {
  display: none; /* Oculto por defecto */
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.4);
  padding-top: -80px; /* Subir el modal hacia arriba */
}
  /* Modal básico */
  .modal {
    display: none; /* Oculto por defecto */
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.4);
    padding-top: -80px; /* Subir el modal hacia arriba */
  }
  
  .modal-content {
    margin: 5% auto;
    padding: 20px;
    width: 60%; /* Ajustado el ancho del modal */
  }
  
  /* Cambiado para mover la flecha al lado derecho */
  .close {
    color: #fff; /* Color del icono de la "tachita" */
    position: absolute; /* Posicionamiento absoluto para que se coloque en la parte superior */
    top: 10px; /* Separación desde el top */
    right: 10px; /* Cambié left a right para moverlo al lado derecho */
    font-size: 28px;
    font-weight: bold;
    cursor: pointer;
    background-color: #007bff; /* Color de fondo */
    width: 35px; /* Tamaño del círculo */
    height: 35px; /* Tamaño del círculo */
    border-radius: 50%; /* Hace el fondo circular */
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 5;
  }
  
  .close:hover,
  .close:focus {
    color: black;
    text-decoration: none;
  }
  
  /* Flexbox para distribuir los contenedores a la izquierda y derecha */
  .container-modal-div-form {
    display: flex; /* Usar flexbox para colocar los elementos en fila */
    justify-content: space-between; /* Distribuir espacio entre los elementos */
    align-items: center; /* Alinear los elementos al centro verticalmente */
    position: relative; /* Necesario para el posicionamiento relativo de los contenedores */
  }
  
  .container-modal-form {
    width: 50%; /* Ambos contenedores ocuparán el mismo ancho */
    padding: 10px; /* Agregar algo de relleno si es necesario */
  }
  
  /* Estilos para el contenedor derecho */
  .container-modal-form.right {
    position: relative; /* Permite el desplazamiento */
    margin-left: -10%; /* Desplaza el contenedor derecho hacia la izquierda */
  }
  
  /* Estilos adicionales para el contenedor izquierdo */
  .container-modal-form.left {
    background-color: rgba(0, 0, 0, 0.4);
    margin-right: 0; /* Elimina el margen entre los contenedores */
  }
  
  /* Estilos para la imagen dentro del contenedor derecho */
  .container-forms-img img {
    width: 50%; /* Ajusta el tamaño de la imagen para que ocupe todo el contenedor */
    height: auto; /* Mantiene las proporciones de la imagen */
  }
  
  .container-forms {
    margin-bottom: 15px; /* Separar un poco el input y el botón */
  }
  
  .number-input {
    width: 50%; /* Hace el input más grande */
    padding: 12px;
    font-size: 16px;
    border-radius: 5px;
    border: 1px solid #ccc;
  }
  
  .suscribirce {
    padding: 12px 20px;
    font-size: 16px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .suscribirce:hover {
    background-color: #0056b3;
  }
/* Media Queries para tabletas */
@media (min-width: 768px) and (max-width: 1124px) {
  .modal-content {
    width: 70%; /* Ajustar el tamaño del modal en pantallas medianas */
  }

  .container-modal-div-form {
    flex-direction: row; /* Mantener los formularios uno al lado del otro */
    justify-content: space-between; /* Separar los formularios */
  }

  .container-modal-form {
    width: 48%; /* Reduce el ancho de los formularios */
    margin-bottom: 0;
  }

  .container-modal-form.left,
  .container-modal-form.right {
    padding: 20px;
  }

  .container-forms-img img {
    width: 80%; /* Ajusta el tamaño de la imagen */
    margin: 0 auto; /* Centra la imagen */
  }

  .number-input {
    width: 100%; /* Hace el input más ancho */
  }

  .suscribirce {
    width: 100%; /* Hace el botón de suscripción ocupar todo el ancho */
  }
}

@media (max-width: 768px) {
  .modal-content {
    width: 80%; /* Ajustar el tamaño del modal en pantallas pequeñas */
  }

  .container-modal-div-form {
    flex-direction: column; /* Coloca los formularios uno debajo del otro */
    align-items: center; /* Centra los formularios */
  }

  .container-modal-form {
    width: 100%; /* Formulario ocupa todo el ancho */
    margin-bottom: 20px;
  }

  .container-modal-form.left,
  .container-modal-form.right {
    padding: 15px;
  }

  .container-forms-img img {
    width: 100%; /* Imagen ocupa todo el ancho del contenedor */
  }
  .number-input {
    width: 80%; /* Hace el input más ancho */
  }

  .suscribirce {
    width: 80%; /* Hace el botón de suscripción ocupar todo el ancho */
    font-size: 14px; /* Reducir el tamaño de fuente en dispositivos móviles */
    padding: 10px 15px; /* Ajustar el padding para que el botón no sea tan grande */
  }

  .image-text {
    font-size: 25px; /* Reducir el tamaño del texto en dispositivos móviles */
    padding: 5px; /* Ajustar el padding del texto */
  }
}

  </style>
  