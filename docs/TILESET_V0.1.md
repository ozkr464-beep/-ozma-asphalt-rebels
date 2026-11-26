# DISTRITO CERO — TILESET DE PRUEBA V0.1

## Objetivo

Comprobar la composición de un mapa cenital usando tiles de 16 x 16 píxeles.
Este es un ejercicio visual LOCAL / TEST, no un nivel jugable.

## Archivos

- `assets/tilesets/distrito-cero-tiles-v01.png`: atlas de 4 columnas x 4 filas (64 x 64 píxeles).
- `assets/maps/distrito-cero-map-v01.png`: composición estática de 20 x 24 tiles (320 x 384 píxeles).
- `assets/sprites/moto-prototipo-v01.png`: motocicleta provisional de 16 x 24 píxeles.
- `map-demo.html` y `css/map-demo.css`: página de pruebas independiente.

## Índice del atlas

| Fila | Col 1 | Col 2 | Col 3 | Col 4 |
| --- | --- | --- | --- | --- |
| 1 | Asfalto | Carril vertical | Carril horizontal | Cruce |
| 2 | Banqueta | Césped | Plaza | Bordillo |
| 3 | Techo azul | Techo terracota | Techo gris | Paso peatonal |
| 4 | Arbusto | Alcantarilla | Cono | Charco |

Los edificios tienen detalles decorativos añadidos al mapa de prueba.
Por ahora no existe un sistema que interprete la cuadrícula ni las colisiones.

## Qué practicar

1. Identificar la diferencia entre `tile`, `tileset` y `tilemap`.
2. Abrir `map-demo.html` desde Live Server.
3. Revisar `image-rendering: pixelated` y `aspect-ratio`.
4. Probar a 390 x 844, 375 x 812 y 360 x 800.
5. Verificar que el mapa no se sale horizontalmente y que se ve la leyenda.

## Restricciones

- No hay movimiento, cronómetro, obstáculos funcionales o puntuación.
- No se modifica el flujo de menú certificado.
- No se conecta Shopify, Ozma Coins ni servidores productivos.
- No se realiza commit hasta validar el resultado local.
