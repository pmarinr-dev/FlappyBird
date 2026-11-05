# Flappy Bird en Jack (Nand2Tetris)

## Créditos de Autoría
* Juan Pablo Marín Rondón

## Documentación Técnica
El proyecto implementa una arquitectura orientada a objetos dividida en 4 clases principales:
* **Main.jack**: Punto de entrada de la aplicación. Gestiona el ciclo de vida global permitiendo reiniciar el juego tras un Game Over, garantizando la liberación de memoria.
* **FlappyGame.jack**: Controlador central. Implementa el Game Loop sincronizado con `Sys.wait()`, procesa la entrada asíncrona del teclado, actualiza el HUD (puntaje en tiempo real) y calcula las colisiones (AABB).
* **Bird.jack**: Entidad del jugador. Gestiona sus propias coordenadas, la simulación de gravedad, el salto y su renderizado visual desacoplado (`draw` y `erase`).
* **Pipe.jack**: Entidad de obstáculo. Maneja su desplazamiento horizontal infinito, la lógica de dibujado respetando el hueco (gap) y su reciclaje al salir de la pantalla.

## Instrucciones de Compilación
1. Abrir la terminal o línea de comandos.
2. Navegar a la carpeta `tools` de Nand2Tetris.
3. Ejecutar el compilador sobre la carpeta del proyecto: `JackCompiler.bat "ruta/a/la/carpeta/FlappyBird"`.

## Instrucciones de Ejecución
1. Abrir `VMEmulator.bat` (o `.sh`).
2. Hacer clic en "Load Program" y seleccionar la carpeta del proyecto.
3. Configurar la animación en "No animation".
4. Ajustar la velocidad (Speed) al nivel máximo ("Fast").
5. Hacer clic en "Play" (Run).

## Controles
* **Barra Espaciadora**: Saltar (evitar caer y esquivar tubos).
* **Tecla R**: Reiniciar partida tras un Game Over.

## Enlaces
* Repositorio: https://github.com/pmarinr-dev/FlappyBird
* Video demostrativo: https://youtu.be/ksS-cdM37Mw
