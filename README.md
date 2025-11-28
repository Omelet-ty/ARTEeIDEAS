
# 🎨 ArteIDEAS - Plataforma de Personalización de Fotos

Esta aplicación es una plataforma de comercio electrónico desarrollada en React para la personalización y venta de productos fotográficos (Marcos, Collages, Impresiones). Destaca por su flujo de personalización avanzado, integración con Inteligencia Artificial y una experiencia de usuario optimizada tanto para escritorio como para móviles mediante un simulador integrado.

## 🚀 Funcionalidades Implementadas

### 1. Interfaz y Navegación (UI/UX)
- **Diseño de Marca**: Paleta de colores consistente utilizando Naranja (`#FF7F40`) y Verde Azulado (`#00A9C3`). Estilo limpio sin degradados excesivos.
- **Simulador Móvil**: 
  - Un wrapper completo que simula un dispositivo iPhone (Notch, biseles, barra de estado).
  - Botón en la cabecera para alternar entre "Modo Computadora" y "Modo Celular".
  - Diseño responsivo que adapta la grilla de productos y el tamaño de las imágenes automáticamente.
- **Cabecera Responsiva**: 
  - Logotipo centrado y barra de búsqueda optimizada.
  - Iconos de navegación (Monitor, Celular, Mis Pedidos, Carrito).

### 2. Catálogo de Productos
- **Landing Page**: Hero section con fondo degradado suave (Cyan a Naranja) y tarjetas de productos optimizadas.
- **Detalle de Producto**: Galería de imágenes, precios (con ofertas tachadas), badges de promoción y descripción detallada.

### 3. Flujo de Personalización Avanzado
- **Subida de Archivos**: Interfaz drag-and-drop.
- **Recorte Dinámico (Cropping)**: 
  - Herramienta de recorte arrastrable sobre la imagen.
  - Relación de aspecto forzada según el formato seleccionado (ej: 9x13, 10x15).
  - **Dimensiones Personalizadas**: Opción para ingresar ancho y largo manual en cm.
- **Editor de Fotos Manual**: Ajustes de Brillo, Contraste y Saturación mediante sliders personalizados.
- **Editor con IA (Gemini API)**:
  - Integración con el modelo `gemini-2.5-flash-image`.
  - **Chat Interface**: El usuario escribe instrucciones (ej: "Quita el fondo", "Ponle un sombrero") y la IA edita la imagen.
  - **Historial de Versiones**: Tira de miniaturas para deshacer cambios y volver a versiones anteriores.
  - **Diseño Móvil**: Layout vertical optimizado (Imagen arriba, Chat abajo) para maximizar la visibilidad.

### 4. Carrito y Checkout
- **Carrito de Compras**: Gestión de cantidades, resumen de subtotal y envío estimado.
- **Checkout (Finalizar Compra)**:
  - **Validación Estricta**:
    - Teléfono y DNI: Solo números, exactamente 9 dígitos.
    - Email: Validación de formato con `@` y `.com`.
  - **Tipos de Entrega**: 
    - Envío a Domicilio (con formulario de dirección).
    - Recojo en Tienda (Gratis - muestra mapa/dirección de la tienda y oculta campos innecesarios).
- **Pasarela de Pago Simulada**:
  - Formateo automático de Tarjeta de Crédito (agrupa dígitos de 4 en 4).
  - Formateo automático de Fecha de Vencimiento (MM/AA).

### 5. Gestión de Pedidos
- **Confirmación de Pedido**: Pantalla de éxito con resumen financiero, estado y pasos siguientes.
- **Mis Pedidos**: 
  - Historial accesible desde el icono de "Caja" en la cabecera.
  - Listado de pedidos pasados con estados (ej: "En Procesamiento").
  - Botón "Ver Detalles" para re-imprimir o revisar el recibo de un pedido anterior.

## 🛠 Tecnologías Utilizadas

- **Frontend**: React 19, TypeScript.
- **Estilos**: Tailwind CSS (Diseño utility-first).
- **Iconos**: Lucide React.
- **IA**: Google GenAI SDK (`@google/genai`).
- **Manipulación de Imagen**: HTML5 Canvas API (para recortes y filtros CSS).

## 📱 Adaptabilidad Móvil

Se ha puesto especial énfasis en la experiencia móvil:
- Las grillas de productos pasan de 4 columnas a 2 columnas.
- Los formularios y tarjetas reducen su padding.
- El Editor de IA cambia su disposición para que el teclado no cubra la imagen.
- Los botones de acción son más grandes y accesibles.

