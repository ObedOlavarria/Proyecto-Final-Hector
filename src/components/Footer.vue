<template>
  <section class="zipcode-footer">
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
</template>

<style scoped>

.ancho {
  max-width: 1200px; /* Limita el ancho máximo a 1200px */
  width: 100%; /* Ocupa todo el ancho del contenedor padre */
  margin: 0 auto; /* Centra horizontalmente */
  box-sizing: border-box; /* Incluye padding en el cálculo del ancho */
}


/* Contenedor para limitar el ancho a 1200px */
.zipcode-container-footer{
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

/* Sección antes del footer */
.zipcode-footer {
  display: flex;
  justify-content: center;
  width: 100%;
  padding: 40px 0;
  position: relative; /* Sin fijar, solo aparece en el flujo normal */
  bottom: 0; /* Al final de la página */
  z-index: 10;
  background-color: #fff;

  display: flex;
  justify-content: center; /* Centra el contenido de la sección */
  width: 100%;
  padding: 40px 0;
  bottom: 0;
  left: 0;
  z-index: 0;
}

.zipcode-footer h2 {
  color: #007bff; /* Azul para el h2 en la sección antes del footer */
}

.zipcode-footer .field p {
  color: black; /* Color negro para el texto de los campos */
}


@media (max-width: 1024px) {
  .zipcode-footer h2 {
    display: none; /* Oculta el h2 */
  }

  .zipcode-fields {
    display: none; /* Oculta los campos en pantallas pequeñas */
  }

  .container-flex-zipcode {
    flex-direction: column; /* Cambia la dirección a columna */
    gap: 20px; /* Aumenta el espacio entre los campos */
  }

  .zipcode-footer {
    padding: 20px 0; /* Ajusta el padding en pantallas pequeñas */
  }

  .go-button {
    width: 100%; /* Hace que el botón ocupe el 100% del contenedor */
    padding: 15px 0; /* Ajusta el padding */
  }
}

.zipcode-footer .field p {
  color: black; /* Color negro para el texto de los campos */
}

</style>
