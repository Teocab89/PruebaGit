function login(usuario, clave) {
  validar(usuario, clave);
  // nuevo código
  registrarIntento(usuario);
  console.log("Intento registrado");

  if (esValido(usuario, clave)) {
    acceder(usuario);
  }
}

function cerrarSesion() {
  limpiarSesion();
  console.log("Sesión cerrada");
  alert("Hasta pronto");
}

// Otra función que será modificada más adelante
function mantenerSesionActiva() {
  setInterval(verificarSesion, 60000);
}
