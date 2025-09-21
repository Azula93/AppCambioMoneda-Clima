# 🌎 TravelApp — Planifica tu viaje con cambio de moneda y clima

Aplicación web que permite seleccionar un país y ciudad destino, ingresar un presupuesto en pesos colombianos (COP), convertirlo automáticamente a la moneda local y consultar el clima actual del destino.  
Frontend en Angular, Backend en Laravel.

---

## 📑 Índice
- [Características](#características)
- [Arquitectura](#arquitectura)
- [Tecnologías](#tecnologías)
- [Instalación](#instalación)
- [Uso](#uso)
- [Configuración de API Keys](#configuración-de-api-keys)
- [Contribuir](#contribuir)
- [Licencia](#licencia)

---

## ✨ Características

- Selección de **país y ciudad** destino (con traducción al español y alemán usando ngx-translate).
- Conversión de **presupuesto en COP** a la moneda local mediante API externa.
- Consulta del **clima en tiempo real** en la ciudad destino.
- **Historial de consultas** guardado en el backend (Laravel + DB).
- **Frontend** desarrollado con Angular 19.
- **Backend** en Laravel 10, expone API REST.
- Arquitectura preparada para despliegue en producción.

---

## 🏗 Arquitectura

El proyecto está compuesto por dos carpetas principales:

- **frontend/** → Aplicación Angular (selección de país/ciudad, presupuesto, traducciones, consumo de APIs).
- **backend/** → API en Laravel. Gestiona:
  - Conexión a la base de datos.
  - Endpoints para guardar y consultar historial.
  - Llamadas a APIs externas (ExchangeRate, OpenWeatherMap) desde el servidor para mayor seguridad.

La comunicación entre frontend y backend se realiza vía **HTTP REST** usando JSON.

---

## 🛠 Tecnologías

- **Frontend:** Angular 19, ngx-translate, Bootstrap 5.
- **Backend:** Laravel 10, PHP 8.
- **Base de datos:** MySQL / MariaDB.
- **APIs externas:**
  - [ExchangeRate API](https://exchangerate.host/) para conversión de monedas.
  - [OpenWeatherMap](https://openweathermap.org/) para clima.

---

## ⚙️ Instalación

### Backend (Laravel)

1. Clona el repositorio y entra a la carpeta backend:
   ```bash
   git clone https://github.com/tuusuario/travelapp.git
   cd travelapp/backend
````markdown
# 📝 Guía de Instalación y Uso

## ⚙️ Backend (Laravel)

### Instala dependencias

```bash
composer install
````

### Crea y configura el archivo `.env`

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=infodec_db
DB_USERNAME=root
DB_PASSWORD=

EXCHANGE_API_KEY=tu_clave_exchangerate
WEATHER_API_KEY=tu_clave_openweather
```

### Ejecuta migraciones y seeders

```bash
php artisan migrate --seed
```

### Inicia el servidor

```bash
php artisan serve
```

## ⚙️ Frontend (Angular)

### Ve a la carpeta frontend

```bash
cd ../frontend
```

### Instala dependencias

```bash
npm install
```

### Inicia la app

```bash
ng serve
```

Abre [http://localhost:4200](http://localhost:4200) en tu navegador.

---

## 🚀 Uso

1. **Paso 1:** Selecciona país y ciudad destino.
2. **Paso 2:** Ingresa presupuesto en COP y selecciona la moneda.
3. **Paso 3:** Visualiza:

   * País y ciudad seleccionados.
   * Presupuesto original en COP.
   * Presupuesto convertido a la moneda local con símbolo.
   * Tasa de cambio aplicada.
   * Clima actual en la ciudad destino.

---

## 🔑 Configuración de API Keys

En el archivo `.env` del backend:

```env
EXCHANGE_API_KEY=tu_clave_exchangerate
WEATHER_API_KEY=tu_clave_openweather
```

El backend usará estas claves para hacer las llamadas a las APIs externas y devolver los datos al frontend.

---

## 🤝 Contribuir

Haz un fork del proyecto.

Crea una rama para tu feature:

```bash
git checkout -b mi-feature
```

Haz commit de tus cambios:

```bash
git commit -m 'Agrego mi feature'
```

Haz push a la rama:

```bash
git push origin mi-feature
```

Abre un Pull Request en GitHub.

---

## 📄 Licencia

Este proyecto está bajo la licencia MIT. Puedes usarlo, modificarlo y distribuirlo libremente mencionando al autor original.

---

## 📸 Capturas

*Agrega aquí capturas de pantalla de la aplicación en funcionamiento.*

```
```

<img width="1904" height="536" alt="Captura de pantalla 2025-09-21 130518" src="https://github.com/user-attachments/assets/00ac5f89-2fb5-4461-a3cf-8ccf84e55e6d" />
<img width="1912" height="620" alt="Captura de pantalla 2025-09-21 130531" src="https://github.com/user-attachments/assets/2a449217-f4a7-46bf-bf83-ee68e1c3f9d2" />
<img width="1911" height="867" alt="Captura de pantalla 2025-09-21 130553" src="https://github.com/user-attachments/assets/ae416bc7-3885-4548-bc3a-9bab4c981cbc" />



