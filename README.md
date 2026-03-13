# 🌿 EcoRuta - Sistema de Logística Sostenible

## Descripción

**EcoRuta** es un prototipo de interfaz de usuario para un sistema de gestión de logística sostenible. Implementa 10 casos de uso diferentes para demostrar el flujo completo de un sistema de entregas ecológico.

## Características

- ✅ **100% HTML/CSS/JavaScript puro** - Sin dependencias externas
- ✅ **Interfaz responsiva** - Funciona en escritorio, tablet y móvil
- ✅ **Datos simulados (Mock)** - Arrays de JavaScript con datos de prueba
- ✅ **Interactividad completa** - Formularios, búsquedas, filtros y actualizaciones
- ✅ **Dashboard moderno** - Diseño limpio con cards y tablas
- ✅ **10 casos de uso implementados** - Todas las funcionalidades solicitadas

## 10 Casos de Uso Implementados

### 1. 📝 Registrar Paquete
- Formulario con campos: remitente, destinatario, dirección, peso, descripción
- Genera automáticamente código de seguimiento único
- Agrega el paquete a la lista de paquetes

### 2. 📦 Ver Lista de Paquetes
- Tabla completa de todos los paquetes registrados
- Muestra información: código, remitente, destinatario, estado, courier asignado, fecha

### 3. 🔍 Buscar Paquete por Código
- Input para buscar por código de seguimiento
- Muestra detalles completos del paquete encontrado
- Información de remitente, destinatario, estado y courier

### 4. 👤 Asignar Paquete a Courier
- Selector de paquetes (solo los en almacén)
- Dropdown con lista de couriers disponibles
- Asigna y cambia el estado a "En Ruta"

### 5. 🗺️ Ver Rutas de Entrega
- Visualiza rutas activas por courier
- Muestra lista de direcciones ordenadas
- Indica número de paquetes en cada ruta

### 6. 📊 Actualizar Estado del Paquete
- Selector de paquetes y nuevos estados
- Estados disponibles: En Almacén, En Ruta, Entregado, Entrega Fallida
- Actualización instantánea con confirmación

### 7. ✅ Confirmar Entrega
- Selecciona paquetes en ruta
- Botón para confirmar entrega
- Cambia estado a "Entregado" y registra hora

### 8. 👥 Gestión de Couriers
- Tabla de todos los couriers disponibles
- Muestra: nombre, teléfono, vehículo, estado, paquetes activos
- Información de capacidad de trabajo

### 9. 📜 Historial de Entregas
- Tabla de paquetes entregados
- Filtro automático de estado "Entregado"
- Información completa: código, destinatario, courier, fecha

### 10. 📍 Ubicación del Courier (Simulación)
- Selector de courier activo
- Muestra coordenadas GPS simuladas
- Botón para actualizar ubicación (simula movimiento)
- Visualización de posición en tiempo real

## Estructura del Archivo

El archivo `ecorouta.html` contiene:

- **HTML Semántico**: Estructura clara con `<header>`, `<nav>`, `<main>`, `<section>`
- **CSS Integrado**: Estilos responsive con gradientes, cards, tablas y formularios
- **JavaScript Puro**: Lógica de datos mock, navegación y funcionalidades interactivas

### Datos Mock Incluidos

**Couriers (4 ejemplos)**:
- Carlos Rodríguez - Bicicleta
- Ana Martínez - Moto
- Pedro García - Furgoneta
- Laura Fernández - Bicicleta

**Paquetes (5 ejemplos iniciales)**:
- PKG001 - PKG005 con diferentes estados

**Rutas (3 rutas activas)**:
- Ruta Madrid (Carlos)
- Ruta Barcelona (Ana)
- Ruta Bilbao (Pedro)

## Cómo Usar

### Opción 1: Abrir en el navegador
1. Descarga o navega a `ecorouta.html`
2. Haz doble clic en el archivo
3. Se abrirá en tu navegador predeterminado

### Opción 2: Abrir desde VS Code
1. Click derecho en `ecorouta.html`
2. Selecciona "Open with Live Server" (si tienes la extensión instalada)
3. O arrastra el archivo a tu navegador

### Opción 3: Servidor local simple
```bash
# Con Python 3
python -m http.server 8000

# Con Python 2
python -m SimpleHTTPServer 8000

# Con Node.js
npx http-server
```

Luego accede a: `http://localhost:8000/ecorouta.html`

## Navegación

La interfaz tiene un **menú de navegación en la parte superior** con botones para cada caso de uso:

1. Haz click en cualquier botón del menú
2. Se carga automáticamente la sección correspondiente
3. Los datos son persistentes durante la sesión

## Interactividad

### Registrar Paquete
- Completa el formulario con datos reales o de prueba
- Haz click en "Registrar Paquete"
- Se genera automáticamente un código de seguimiento
- Se muestra mensaje de éxito con el código

### Buscar Paquete
- Ingresa un código de seguimiento (ej: PKG001)
- Haz click en "Buscar"
- Se muestran todos los detalles del paquete

### Asignar Courier
- Selecciona un paquete de la lista (solo los en almacén)
- Selecciona un courier disponible
- Haz click en "Asignar Courier"
- El paquete pasa a estado "En Ruta"

### Actualizar Estado
- Selecciona un paquete
- Elige el nuevo estado
- Haz click en "Actualizar Estado"
- Se confirma el cambio

### Confirmar Entrega
- Selecciona un paquete en ruta
- Haz click en "Confirmar Entrega"
- El estado cambia a "Entregado"
- Se registra la hora de entrega

### Ubicación Courier
- Selecciona un courier
- Se muestra su posición GPS simulada
- Haz click en "Actualizar Ubicación" para simular movimiento

## Características de Diseño

### Colores
- **Principal**: Púrpura/Azul (`#667eea`, `#764ba2`)
- **Éxito**: Verde (`#d4edda`)
- **Error**: Rojo (`#f8d7da`)
- **Advertencia**: Amarillo (`#fff3cd`)
- **Información**: Azul claro (`#e7f3ff`)

### Elementos Visuales
- Iconos y emojis para claridad visual
- Badges de estado con colores significativos
- Cards con efecto hover
- Tablas con filas alternadas
- Animaciones suaves de transición

### Responsividad
- Funciona perfectamente en:
  - 📱 Móviles (320px+)
  - 📱 Tablets (768px+)
  - 🖥️ Escritorio (1200px+)
- Grid flexible que se adapta

## Datos Persistentes

Los datos se mantienen durante toda la sesión del navegador:

- Los paquetes registrados se guardan en memoria
- Las asignaciones de couriers se persisten
- Los cambios de estado son inmediatos
- Al recargar la página, vuelven los datos iniciales

**Nota**: Para almacenamiento persistente, sería necesario un backend con base de datos.

## Mejoras Futuras

Para convertir esto en un sistema de producción, se podría:

1. ✅ Conectar a un backend (Node.js, Python, etc.)
2. ✅ Usar una base de datos real (PostgreSQL, MongoDB)
3. ✅ Implementar autenticación de usuarios
4. ✅ Integrar mapas reales (Google Maps, OpenStreetMap)
5. ✅ Agregar geolocalización GPS real
6. ✅ Implementar notificaciones en tiempo real (WebSockets)
7. ✅ Crear aplicación móvil nativa
8. ✅ Integrar pagos y facturación

## Navegadores Soportados

- ✅ Chrome/Edge (v90+)
- ✅ Firefox (v88+)
- ✅ Safari (v14+)
- ✅ Opera (v76+)

## Licencia

Proyecto de demostración - Uso libre para fines educativos y de demostración.

## Autor

Sistema de Logística EcoRuta - Prototipo HTML5
Año: 2026

---

**¡Disfruta explorando EcoRuta! 🌿📦**
