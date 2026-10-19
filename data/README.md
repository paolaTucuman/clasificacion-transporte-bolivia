# Conjunto de imágenes

La [versión 1 del proyecto Deteccion de transporte en Roboflow Universe](https://universe.roboflow.com/piedra-papel-y-tijera-wtgoh/deteccion-de-transporte) reúne **422 imágenes preparadas** en `train/`, `valid/` y `test/`. Las 176 imágenes originales se reunieron para el proyecto e incluyen imágenes obtenidas de internet. No se conservó un listado individual de sus enlaces de origen.

El archivo [transporte-imagenes-418.zip](transporte-imagenes-418.zip) contiene un **subconjunto** de la versión 1: 366 imágenes de entrenamiento, 34 de validación y 18 de prueba. Por tanto, no reproduce exactamente los datos con los que se obtuvo la métrica de validación publicada.

| Clase | Originales de entrenamiento | JPG de entrenamiento tras aumento | Validación | Prueba | Originales totales |
| --- | ---: | ---: | ---: | ---: | ---: |
| Micro | 38 | 114 | 14 | 11 | 63 |
| Mini bus | 40 | 120 | 10 | 3 | 53 |
| Teleférico | 45 | 135 | 11 | 4 | 60 |
| **Total** | **123** | **369** | **35** | **18** | **176** |

| Clase en el archivo descargable | Entrenamiento | Validación | Prueba |
| --- | ---: | ---: | ---: |
| Micro | 111 | 13 | 11 |
| Mini bus | 120 | 10 | 3 |
| Teleférico | 135 | 11 | 4 |
| **Total** | **366** | **34** | **18** |

La versión preparada documenta orientación automática, redimensionamiento a **640 × 640** con recorte central, volteo horizontal, recorte aleatorio y cambios de brillo. Cada imagen original de entrenamiento tiene tres versiones; validación y prueba mantienen una por original.

Para extraer el subconjunto desde la raíz del repositorio con Python 3:

```sh
python -m zipfile -e data/transporte-imagenes-418.zip data/transporte-imagenes-418
```

La versión completa y el modelo alojado se consultan desde Roboflow Universe. El repositorio tampoco contiene el procedimiento completo de entrenamiento de ViT ni sus pesos.
