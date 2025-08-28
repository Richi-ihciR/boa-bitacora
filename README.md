En ésta rama vamos a añadir una nueva función para que el usuario pueda visualizar el contenido de las entradas de texto, imagen, etc, que el usuiario vaya ingresando dentro de la interfaz misma. 
Documentación / pseudocódigo para el “visor de entradas y obras”

Feature: Visor de entradas y obras
Objetivo: Permitir que el usuario visualice en detalle las entradas de bitácora (texto completo) y las obras asociadas (fotos y dibujos).

Flujo de usuario:
1. El usuario abre la pestaña Bitácora o Galería.
2. Junto a cada obra aparece un botón "👁️ Ver".
3. Al presionar el botón:
   - Se abre una ventana emergente (Toplevel).
   - Se muestran los datos principales (título, tipo, fecha, descripción).
   - Si la obra es una imagen (foto/dibujo), se carga y muestra con un tamaño reducido.
   - Si es parte de una entrada, se incluye también el texto asociado.

Esquema:
[Obra en lista/galería] → [Botón "👁️ Ver"] → [Toplevel con detalle]  
                                   ↳ [Texto completo]  
                                   ↳ [Imagen (si aplica)]

Estado actual:
- La app ya guarda y carga obras/entradas, pero no las visualiza.
- Falta añadir: función de visor + botones en interfaces.

Riesgos:
- Manejo de archivos inexistentes.
- Redimensionado de imágenes grandes.
- Dependencia: Pillow (PIL).
