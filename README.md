# 🎨 Icons CDN

Una colección de más de 4000 íconos SVG organizados como CDN para usar fácilmente en tus proyectos web.

## 📦 Contenido

- **4170 íconos SVG** organizados en la carpeta `icons/`
- **CSS generado automáticamente** con clases para cada ícono
- **Sistema de tamaños** predefinidos (sm, normal, lg, xl)

## 🚀 Despliegue en GitHub Pages

### Paso 1: Subir el repositorio a GitHub

1. Crea un nuevo repositorio en GitHub (por ejemplo: `icons-cdn`)
2. Inicializa git en tu carpeta local:
```bash
git init
git add .
git commit -m "Initial commit: Icons CDN"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/icons-cdn.git
git push -u origin main
```

### Paso 2: Activar GitHub Pages

1. Ve a la configuración de tu repositorio en GitHub
2. Navega a **Settings** → **Pages**
3. En **Source**, selecciona la rama `main` y la carpeta `/ (root)`
4. Guarda los cambios

### Paso 3: Actualizar las URLs del CSS

Una vez desplegado, necesitas actualizar el archivo `icons.css` para que use la URL completa de GitHub Pages. Puedes hacerlo de dos formas:

**Opción A: Editar manualmente el CSS**
- Reemplaza todas las instancias de `url('icons/` por `url('https://TU_USUARIO.github.io/icons/icons/`
- O crea una nueva versión del CSS con URLs absolutas

**Opción B: Usar el script de actualización**

Ejecuta el script `update-cdn-urls.ps1` (ver más abajo) para actualizar automáticamente las URLs.

### Paso 4: Verificar el despliegue

Tu CDN estará disponible en:
```
https://TU_USUARIO.github.io/icons/icons.css
```

## 📖 Cómo usar el CDN

### 1. Incluir el CSS en tu HTML

```html
<link rel="stylesheet" href="https://TU_USUARIO.github.io/icons/icons.css">
```

### 2. Usar los íconos

```html
<!-- Ícono básico -->
<span class="icons icons-wolf-howl"></span>

<!-- Con tamaño pequeño -->
<span class="icons icons-sm icons-wolf-howl"></span>

<!-- Con tamaño grande -->
<span class="icons icons-lg icons-wolf-howl"></span>

<!-- Con tamaño extra grande -->
<span class="icons icons-xl icons-wolf-howl"></span>
```

### 3. Ejemplos de uso

**En botones:**
```html
<button>
    <span class="icons icons-ancient-sword"></span> Atacar
</button>
```

**En listas:**
```html
<ul>
    <li>
        <span class="icons icons-black-hand-shield"></span> Escudo
    </li>
</ul>
```

**Con texto:**
```html
<p>
    <span class="icons icons-half-heart"></span> Vida: 100%
</p>
```

### 4. Personalización con CSS

Los íconos son SVG y puedes personalizarlos fácilmente con CSS. Los íconos usan máscaras CSS, lo que permite cambiar su color de forma sencilla.

#### Cambiar el color de los íconos

Puedes cambiar el color de los íconos de dos formas:

**Opción 1: Usando la propiedad `color` (recomendado)**

El ícono heredará el color del texto del elemento:

```css
/* Cambiar color usando la propiedad color */
.mi-icono-rojo {
    color: #ff0000; /* Rojo */
}

.mi-icono-azul {
    color: #0066ff; /* Azul */
}
```

```html
<!-- Ejemplo de uso -->
<span class="icons icons-sword" style="color: red;"></span>
<span class="icons icons-shield" style="color: blue;"></span>
```

**Opción 2: Usando la propiedad `background-color`**

Puedes sobrescribir el color directamente:

```css
.mi-icono-verde {
    background-color: #00ff00; /* Verde */
}
```

```html
<!-- Ejemplo de uso -->
<span class="icons icons-half-heart" style="background-color: green;"></span>
```

#### Otras personalizaciones

```css
/* Agregar sombra */
.icons-con-sombra {
    filter: drop-shadow(2px 2px 4px rgba(0,0,0,0.3));
}

/* Cambiar tamaño personalizado */
.icons-personalizado {
    width: 3em;
    height: 3em;
}

/* Combinar color y tamaño */
.icons-grande-rojo {
    width: 2.5em;
    height: 2.5em;
    color: #ff0000;
}
```

## 🔧 Herramientas incluidas

### `generate-css.ps1`
Genera automáticamente el archivo `icons.css` desde todos los SVG en la carpeta `icons/`.

```powershell
powershell -ExecutionPolicy Bypass -File generate-css.ps1
```

### `update-cdn-urls.ps1`
Actualiza las URLs en el CSS para usar la URL completa de GitHub Pages.

```powershell
powershell -ExecutionPolicy Bypass -File update-cdn-urls.ps1
```

**Nota:** Debes editar el script y reemplazar `TU_USUARIO` con tu usuario de GitHub antes de ejecutarlo.

## 📋 Lista de íconos disponibles

Para ver todos los íconos disponibles, puedes:
1. Revisar la carpeta `icons/` para ver los nombres de los archivos
2. Abrir `example.html` en tu navegador (después de actualizar la URL del CSS)
3. Inspeccionar el archivo `icons.css` para ver todas las clases disponibles

## 🎨 Nombres de clases

Los nombres de las clases se generan automáticamente desde los nombres de los archivos SVG:
- El nombre del archivo `sword.svg` se convierte en `.icons-sword`
- Los caracteres especiales se reemplazan por guiones
- Si hay duplicados, se agrega el prefijo del creador

## 📝 Notas

- Todos los íconos están bajo licencia Creative Commons 3.0 BY o CC0
- Los creadores originales están listados en `license.txt`
- Si usas estos íconos, considera mencionar a los creadores originales

## 🔄 Actualizar el CDN

Si agregas nuevos íconos:

1. Coloca los nuevos archivos SVG en la carpeta `icons/`
2. Ejecuta `generate-css.ps1` para regenerar el CSS
3. Si ya está desplegado, ejecuta `update-cdn-urls.ps1` para actualizar las URLs
4. Haz commit y push a GitHub

## 📞 Soporte

Para más información sobre los íconos originales, visita: https://game-icons.net

---

**¡Disfruta usando estos íconos en tus proyectos!** 🎉

