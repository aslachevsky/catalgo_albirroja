# Catálogo Albirroja 2026 — Instrucciones del Proyecto

> Catálogo cooperativo de artículos coleccionables de la Selección Paraguaya de Fútbol
> con motivo del Mundial FIFA 2026.
> Creado y mantenido por **CPC** y **AndyS**.

---

## 🎯 Propósito

Registrar y compartir información sobre coleccionables de la Albirroja en el contexto del
Mundial 2026, exclusivamente como herramienta de referencia para los socios de CPC.
**Sin fines comerciales. No se permite publicar precios ni facilitar compraventas.**

---

## 🎨 Identidad Visual

| Elemento       | Valor                    |
|----------------|--------------------------|
| Color principal | Rojo `#CC0001`           |
| Color secundario | Blanco `#FFFFFF`        |
| Color acento    | Azul `#0038A8`           |
| Tipografía títulos | Montserrat (700–900) |
| Tipografía cuerpo  | Open Sans (400–600)  |

- El diseño evoca la camiseta **albirroja** (franjas verticales rojo y blanco).
- Se puede usar imágenes del **Estadio Defensores del Chaco** como elemento visual.
- **No usar ningún logo de la APF** (Asociación Paraguaya de Fútbol) ni de la FIFA.
- Logos autorizados: `logocpc.webp` y `logotr.webp` (ambos en la carpeta raíz del proyecto).

---

## 📁 Estructura de Archivos

```
Catalogo Albirroja/
├── index.html          ← Landing page principal
├── catalogo.html       ← Vista del catálogo con lista y filtros
├── firebase-config.js  ← Configuración de Firebase (no modificar)
├── logocpc.webp        ← Logo CPC
├── logotr.webp         ← Logo AndyS
└── INSTRUCCIONES.md    ← Este archivo
```

---

## 🔥 Firebase

**Base de datos:** Firebase Firestore  
**Nombre del proyecto Firebase:** `helio-produce`  
**Nombre lógico del catálogo:** `andyslapry`

```javascript
const firebaseConfig = {
  apiKey: "AIzaSyBOB3EZQQ8jKOyieOqt5_EebUn8ITknAfY",
  authDomain: "helio-produce.firebaseapp.com",
  projectId: "helio-produce",
  storageBucket: "helio-produce.firebasestorage.app",
  messagingSenderId: "217860282947",
  appId: "1:217860282947:web:de5d1c000d2ff0c8efd2f6"
};
```

Las imágenes de los artículos se almacenan en **Firebase Storage**.
Los datos del catálogo se almacenan en **Firestore** (colección: `articulos`).

---

## 📋 Campos del Catálogo

Cada artículo registrado debe tener los siguientes campos:

| Campo | Tipo | Descripción |
|-------|------|-------------|
| `categoria` | Selección | Categoría del artículo |
| `oficial` | Booleano (Sí/No) | Si es oficial de la APF |
| `marca` | Texto | Nombre de la marca |
| `tipo` | Selección | Formato físico del artículo |
| `descripcion` | Texto largo | Descripción del artículo |
| `imagen` | Archivo/URL | Imagen representativa |
| `linkOficial` | URL | Link a más info del artículo |
| `cantidadVariantes` | Número | Cantidad de versiones distintas |
| `dondeConseguir` | Texto | Puntos de venta colaborativos |
| `fechaCarga` | Timestamp | Fecha de carga (automático) |

---

## 📂 Categorías disponibles

- Bebidas
- Yerba Mate
- Comestibles
- Figuritas
- *(Se pueden agregar nuevas categorías dinámicamente)*

## 📦 Tipos de artículo disponibles

- Vaso
- Lata
- Caja
- Muñeco
- *(Se pueden agregar nuevos tipos dinámicamente)*

---

## ✅ Reglas del Catálogo

1. **Cualquier usuario puede cargar un nuevo artículo** — el catálogo es cooperativo.
2. **No se permite publicar precios** de ningún artículo.
3. **No se permite facilitar compras o ventas** entre usuarios.
4. Las imágenes se muestran mediante un **ícono** (no directamente en la lista) para mantener la legibilidad.
5. La lista debe poder **filtrarse** por: categoría, tipo, marca, oficial (Sí/No).
6. La lista debe poder **imprimirse** mostrando: tipo, marca y descripción.

---

## 🖨️ Función de Impresión

Al imprimir, la lista debe mostrar únicamente:
- Tipo
- Marca
- Descripción

Ocultar: imágenes, botones, filtros, header y footer decorativo.

---

## 🤝 Créditos y Autoría

- **CPC** — Club de Coleccionistas del Paraguay
- **AndyS** — Colaborador principal

**Disclaimer legal:** Este sitio no está afiliado a la APF ni a la FIFA.
Todos los nombres de marcas y productos pertenecen a sus respectivos propietarios.
El uso de nombres relacionados al fútbol paraguayo es exclusivamente descriptivo.

---

## 🚀 Roadmap

- [x] Landing page (`index.html`)
- [ ] Catálogo con lista y filtros (`catalogo.html`)
- [ ] Formulario de carga de artículo
- [ ] Vista detalle de artículo
- [ ] Función de impresión
- [ ] Gestión de categorías/tipos dinámicos

---

*Última actualización: Abril 2026*

El site deber ser responsive para adecuarse a todos los dispositivos
