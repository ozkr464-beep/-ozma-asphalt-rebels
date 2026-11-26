# DISTRITO CERO — MAP DESIGN V0.2

- **Proyecto:** OZMA: Asphalt Rebels
- **Misión:** Entrega Cero (nombre provisional)
- **Fecha de revisión:** 26/11/2026
- **Estado:** diseño aprobado para documentación; jugabilidad pendiente
- **Entorno:** LOCAL / TEST

## 1. Objetivo

Diseñar el tutorial jugable de Distrito Cero para el modelo de conducción híbrido: avance automático, maniobras laterales y elección de rutas en bifurcaciones.

El mapa estático existente de 20 × 24 tiles es una **prueba de composición**, no la longitud completa de la misión.

## 2. Identidad

- Ciudad ficticia inspirada en México.
- Perspectiva cenital Top-Down 2D.
- Pixel art retro original; paleta Urban Predator.
- Orientación vertical (portrait).
- Taller Ozma, taquería, calles, viviendas y plaza urbana.

## 3. Escala y estructura

- **Tile base:** 16 × 16 píxeles.
- **Mapa estático actual:** 20 columnas × 24 filas (320 × 384 píxeles de diseño).
- **Recorrido futuro:** múltiples tramos conectados; cada tramo podrá reutilizar la misma cuadrícula de trabajo.
- **Cámara:** seguirá la moto y revelará nuevos tramos al avanzar.
- **Escalado móvil y altura visible:** por certificar durante implementación.
- **Velocidad y distancia exacta:** por definir mediante pruebas.

No confundir **mapa visible** con **longitud de la misión**. Un jugador podrá recorrer varios mapas/pantallas durante una entrega.

## 4. Flujo de la primera misión

```text
TALLER OZMA / INICIO
         |
         v
TAQUERÍA / RECOGIDA A
         |
         v
TRAMO DE ESQUIVA
         |
         v
   BIFURCACIÓN
      /     \
 IZQUIERDA DERECHA
      \     /
       REUNIÓN
         |
         v
VIVIENDAS / ENTREGA B
         |
         v
RESULTADO / PUNTOS REBEL
```

La bifurcación es una **decisión real de ruta**, no solo un cambio estético de carril. Ambas opciones deben poder completar la misión; pueden presentar riesgos y obstáculos distintos.

## 5. Biblioteca inicial de tramos

| ID | Tipo | Uso | Estado |
|---|---|---|---|
| DC-01 | Inicio y recogida A | Explicar HUD y recolección | Diseño |
| DC-02 | Recta con obstáculo | Practicar cambio de carril | Diseño |
| DC-03 | Bifurcación | Elegir izquierda o derecha | Diseño |
| DC-04L | Ramal izquierdo | Ruta alternativa con riesgo propio | Diseño |
| DC-04R | Ramal derecho | Ruta alternativa con riesgo propio | Diseño |
| DC-05 | Reunión y entrega B | Completar misión | Diseño |

Estos IDs organizan recursos futuros; **no son archivos existentes**. La cantidad y duración final de tramos podrán cambiar.

## 6. Reglas de movimiento previstas

### 6.1 Avance

La motocicleta avanza automáticamente. El jugador se concentra en la dirección lateral, los obstáculos y las bifurcaciones. No habrá acelerador continuo durante el primer prototipo.

### 6.2 Esquiva

- Deslizamiento lateral en móvil.
- Flechas izquierda/derecha o A/D como controles de prueba en PC.
- Se procurarán carriles definidos y retroalimentación visual inmediata.

### 6.3 Elección de ruta

- La bifurcación se anuncia antes de llegar.
- Aparecen dos acciones claras: **RUTA IZQUIERDA** y **RUTA DERECHA**.
- Los botones de ruta se distinguen de la maniobra lateral para evitar entradas ambiguas.
- Una decisión válida conduce al ramal elegido; reglas para no elegir a tiempo por definir en implementación.

Para el primer prototipo los ramales pueden mantener la dirección general vertical y reunirse más adelante. Giros de 90 grados y rotación de cámara no forman parte de esta fase.

## 7. Obstáculos y dificultad

- Primeros obstáculos candidatos: conos, vehículo estacionado y barrera visual.
- Los obstáculos deben ser visibles con suficiente anticipación.
- Reacción ante colisión (penalización, reinicio, pérdida de tiempo): pendiente de diseñar y probar.
- **Duración objetivo inicial:** aproximadamente 45–90 segundos, pendiente de balanceo real.
- Primer tutorial: un cambio de carril obligatorio y al menos una bifurcación.

No introducir todavía persecuciones policiales, tráfico autónomo ni físicas avanzadas.

## 8. HUD y pantalla

Información prevista:

- Nombre del distrito y misión.
- Estado del pedido: sin recoger / en transporte / entregado.
- Aviso anticipado de bifurcación.
- Botón de pausa.
- Resultado al finalizar.

La interfaz debe respetar áreas seguras del teléfono, evitar tapar la moto y funcionar en vertical. El HUD definitivo se probará en dispositivos físicos.

## 9. Puntuación

La primera versión utilizará **Puntos Rebel** como puntuación local por habilidad y resultado de entrega. Valores, penalizaciones y fórmula exacta pendientes de pruebas.

**OZMA COINS** es un sistema comercial futuro y separado. No participa en la primera misión ni determina ventajas competitivas.

## 10. Recursos actuales y nuevos

### Recursos existentes en el trabajo local

- `map-demo.html`: visualización estática del escenario.
- `css/map-demo.css`: estilos de la maqueta.
- Carpetas de recursos `assets/maps`, `assets/tilesets` y `assets/sprites` mostradas en VS Code.

La maqueta es útil para validar apariencia, no demuestra cámara ni lógica de juego. Aún se requiere revisión antes de su commit.

### Recursos por diseñar después

- Módulos visuales compatibles entre sí: recta, bifurcación, ramal y reunión.
- Señalización clara de recogida, entrega y dirección.
- Animación de moto y variantes por rider.
- Pantalla de resultado.

## 11. Pruebas y criterios de aceptación

**Fase de diseño (ahora):**

- [ ] Revisar que la maqueta estática se muestre correctamente a 390 × 844 y 360 × 800.
- [ ] Certificar carga de recursos sin errores 404.
- [ ] Verificar que los tramos futuros tendrán uniones de calle coherentes.
- [ ] Documentar la primera bifurcación y su señalización.
- [ ] Confirmar documentación V0.2 y GDD V0.4 en GitHub.

**Fase jugable (posterior):**

- [ ] Avance automático funcional.
- [ ] Esquiva lateral táctil y con teclado de prueba.
- [ ] Cámara con seguimiento.
- [ ] Recogida A activable.
- [ ] Bifurcación de dos rutas funcionales.
- [ ] Entrega B y resultado con puntuación local.
- [ ] Prueba de jugabilidad con personas externas y teléfono físico.

No marcar casillas sin evidencia.

## 12. Restricciones

- Sin JavaScript nuevo, físicas ni tráfico funcional en esta etapa documental.
- Sin integrar todavía la maqueta a la navegación principal ni activar el botón de iniciar partida.
- Sin conexiones con Shopify, Ozma IA, Ozma BI o sistemas productivos.
- Cualquier paso posterior de implementación requerirá su propio alcance y validación.

## 13. Registro de cambios

- **V0.1:** primer escenario conceptual y misión A→B.
- **V0.2:** recorrido por tramos, controles híbridos, bifurcación real, cámara de seguimiento y criterios de prueba diferenciados.