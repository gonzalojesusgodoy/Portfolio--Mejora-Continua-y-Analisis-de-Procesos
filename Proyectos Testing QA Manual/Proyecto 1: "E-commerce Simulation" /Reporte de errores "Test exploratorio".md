## 📊 Reporte de errores — Test Exploratorio

| ID | Título | Descripción | Pasos | Datos | R. esperado | R. obtenido | Severidad |
|---|---|---|---|---|---|---|---|
| **003** | Advertencia/alerta de que la contraseña no era segura / Registrarse con caracteres | A la hora de iniciar sesión en los requerimientos utilicé datos falsos y me dejó navegar sin problemas en la página web. | 1. Acceder al Sign-up.<br>2. Completar campos.<br>3. Iniciar sesión. | Usuario: `12121213`<br>Contraseña: `12121213` | No poder registrarse con datos falsos. | Puede registrarse con datos falsos. | Alta |
| **004** | Se deja registrar a los usuarios con datos inválidos | Al intentar loguearse con datos inválidos, la página permite hacerlo. | 1. Acceder al Sign-up.<br>2. Completar los campos.<br>3. Ingresar correctamente. | `usuario_falso`<br>`contraseña_falsa` | No poder registrarse. | Puede registrarse correctamente. | Alta |
