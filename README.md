# Taller 6 – GUIs con Swing y Java2D (Diario de restaurantes)

Aplicación Swing para llevar un diario de restaurantes visitados y por visitar:
lista de restaurantes con sus detalles, ventana para agregar uno nuevo marcándolo
en un mapa y ventana con el mapa de todos (o sólo los visitados).

## Contenido

- `src/` – código fuente (paquetes `uniandes.dpoo.swing.mundo` e `uniandes.dpoo.swing.interfaz.*`).
- `imagenes/` – mapa y estrellas de calificación (se cargan con rutas relativas `./imagenes/...`).
- `docs/diagrama_clases.png` – diagrama de clases de la aplicación completa
  (editable en draw.io: `docs/diagrama_clases.drawio`).

## Cómo ejecutar

**Importante:** el directorio de trabajo debe ser la raíz del proyecto (la carpeta que
contiene `imagenes/`); si no, no se cargan el mapa ni las estrellas.

### En Eclipse
1. `File > Import… > General > Existing Projects into Workspace` y seleccione esta carpeta.
2. Abra `uniandes.dpoo.swing.interfaz.principal.VentanaPrincipal`.
3. Clic derecho → `Run As > Java Application`.
   (Eclipse usa por defecto la raíz del proyecto como directorio de trabajo.)

### Desde la terminal (Java 11 o superior)
Desde la raíz del proyecto:

```bash
javac -encoding UTF-8 -d bin $(find src -name "*.java")
java -cp bin uniandes.dpoo.swing.interfaz.principal.VentanaPrincipal
```

En Windows (PowerShell):

```powershell
javac -encoding UTF-8 -d bin (Get-ChildItem -Recurse src -Filter *.java).FullName
java -cp bin uniandes.dpoo.swing.interfaz.principal.VentanaPrincipal
```

## Uso
- **Nuevo**: abre la ventana para agregar un restaurante. Haga clic en el mapa para marcar
  su ubicación, escriba el nombre, elija calificación y si ya fue visitado, y pulse
  **Crear restaurante**.
- **Ver todos**: abre el mapa con los nombres de los restaurantes. Los radio buttons
  **Todos / Visitados** filtran lo que se dibuja.
- Al seleccionar un restaurante en la lista se muestran abajo su nombre, su calificación
  (estrellas) y si fue visitado.
