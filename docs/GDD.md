OZMA: ASPHALT REBELS
GAME DESIGN DOCUMENT V0.4
- Estudio: OZMA GAMING
- Proyecto: OZMA PLAY / Game Studio
- Desarrollador: Oscar Garnica
- Fecha de revisión: 26/11/2026
- Plataforma inicial: navegador móvil
- Orientación: vertical (portrait)
- Estado: preproducción / prototipo académico
- Entorno: LOCAL / TEST
1. Concepto
Videojuego arcade original de conducción y reparto en motocicleta, con estética pixel art Top-Down 2D, ambientado en una ciudad ficticia inspirada en México.

Bucle principal: recoger un pedido en A → conducir y esquivar obstáculos → elegir rutas en bifurcaciones → entregar en B → obtener Puntos Rebel → intentar mejorar el resultado.
2. Pilares de diseño
1. Fácil de comenzar: avance automático y controles táctiles sencillos.
2. Habilidad y decisiones: cambios de carril y selección de ruta afectan el resultado.
3. Partidas cortas y repetibles: primera entrega de duración objetivo aproximada de 45–90 segundos, ajustable tras pruebas.
4. Identidad original: cultura biker urbana mexicana, humor, grafiti y eventos inesperados.
5. Competencia justa: los rankings por habilidad no dependen de compras comerciales.
3. Identidad visual
- Pixel art retro original, inspirado en arcades de 16 bits.
- Perspectiva cenital 2D (Top-Down).
- Paleta Urban Predator: negro, blanco, verde neón y colores distintivos por personaje.
- Distritos urbanos ficticios; vehículos, locales y personajes originales.
- Eventos extraordinarios y OVNIs como easter eggs futuros.
4. Personajes
- LINA: agilidad, identidad turquesa.
- NYX: velocidad, identidad morada.
- TORO: resistencia, identidad roja.
Los retratos están incorporados a la pantalla de selección. Sus atributos jugables aún no están programados; para el primer prototipo pueden funcionar como variantes cosméticas con las mismas reglas de conducción.
5. Distritos previstos
1. Distrito Cero: tutorial y primera entrega jugable.
2. Distrito Mercado: más tránsito y obstáculos urbanos.
3. Distrito Lluvia: clima y superficies complicadas.
4. Distrito Federal Rebel: persecuciones ficticias y dificultad avanzada.
5. Distrito Anomalía: situaciones extraordinarias.
Solo Distrito Cero está contemplado en el alcance del primer prototipo.
6. Mecánica de conducción: MODELO HÍBRIDO APROBADO
6.1 Avance automático
La motocicleta avanza hacia adelante sin mantener pulsado un acelerador. En la primera versión la velocidad será controlada por las reglas de la misión; aceleración y frenado manuales quedan para evaluación posterior.
6.2 Maniobras laterales
El jugador desliza a izquierda o derecha para cambiar de carril y esquivar obstáculos. Para pruebas de escritorio se contemplan teclas de dirección o A/D. Las maniobras deben ser legibles, predecibles y compatibles con pantallas táctiles.
6.3 Bifurcaciones
Antes de un cruce aparece una señal anticipada y una ventana de decisión. El jugador selecciona RUTA IZQUIERDA o RUTA DERECHA mediante controles visibles diferenciados de los cambios de carril. Las dos rutas tienen obstáculos o riesgos diferentes y pueden volver a unirse antes del destino.

En el primer prototipo las bifurcaciones podrán representarse con tramos que se separan y vuelven a conectarse, conservando el desplazamiento principal vertical. Los giros completos de 90 grados y la rotación de cámara quedan fuera del primer alcance.
6.4 Cámara
La cámara sigue a la moto; el mundo avanza visualmente respecto al jugador. No se mostrará toda la misión en una sola imagen estática. La escala se adaptará al teléfono, conservando proporciones y legibilidad.
6.5 Recogida, entrega y obstáculos
La recogida y la entrega se activan al alcanzar zonas señalizadas. Se incorporarán obstáculos sencillos y un resultado de misión. Las reglas de colisión, penalizaciones y velocidad se determinarán durante pruebas del prototipo; no están implementadas actualmente.
7. Modos de juego
7.1 Modo Repartidor — primero
Recorrido finito con punto A, destino B, al menos una bifurcación y puntuación por desempeño.
7.2 Modo Supervivencia — futuro
Recorrido prolongado con dificultad progresiva y registro de distancia. No forma parte del primer prototipo.
8. Distrito Cero: primera misión
Nombre provisional: Entrega Cero.
1. Salida desde el entorno del taller Ozma.
2. Desplazamiento hacia la taquería y recogida en A.
3. Tramo con cambio de carril y obstáculos señalizados.
4. Elección entre dos rutas en una bifurcación.
5. Reencuentro de rutas y aproximación al destino.
6. Entrega en B y pantalla de resultado.
Los tiempos, distancias y recompensas finales no están certificados. Ver docs/DISTRITO_CERO.md.
9. Sistema de puntos y economía
- Puntos Rebel: puntuación interna por habilidad, entrega y desempeño; futura base de clasificaciones competitivas.
- OZMA COINS: sistema de fidelización y personalización propuesto, sin valor monetario ni funcionalidad actualmente implementada.
- Las compras de Ozma Moto Sport, recompensas físicas y rankings online requerirán evaluación técnica, legal y financiera antes de cualquier integración.
- Ninguna compra comercial deberá otorgar ventaja en competencias de habilidad con premios físicos.
- No implementar criptomonedas durante la etapa académica.
10. Pantallas y experiencia de usuario
1. OZMA GAMING PRESENTS.
2. Intro / carga visual (no refleja todavía carga real).
3. Menú principal.
4. Selección obligatoria de rider.
5. Selección de distrito.
6. Juego (pendiente de implementar).
7. Resultado de misión (pendiente de implementar).
La pantalla map-demo.html es un laboratorio visual independiente: no representa todavía la pantalla del juego ni debe conectarse a la navegación comercial.
11. Tecnología y arquitectura evolutiva
Actual: HTML5, CSS3, imágenes PNG, Git y GitHub.

Siguiente fase, al avanzar en JavaScript: evaluación de Canvas API o Phaser; bucle de actualización, representación de tramos, entrada táctil, cámara, colisiones y estados de juego.

Convenciones iniciales: tile base 16 × 16 píxeles; mapa estático de prueba 20 × 24 tiles. El recorrido jugable utilizará varios tramos; el tamaño del mapa de prueba no limita su duración.

No se ha elegido motor definitivo, formato final de datos ni backend.
12. Criterios de aceptación de la primera versión jugable
- La moto avanza automáticamente sin interacción continua.
- El jugador puede cambiar de carril desde controles táctiles y teclado de prueba.
- Hay una recogida A y una entrega B verificables.
- Una bifurcación ofrece dos elecciones distinguibles y conduce a recorridos válidos.
- Se detecta al menos un obstáculo con una respuesta de juego definida.
- La cámara permite recorrer más de una pantalla sin exponer el mapa completo.
- Hay un estado de final de misión y una puntuación local.
- Se prueba en dispositivo móvil real y no solo en emulación de navegador.
Estos criterios son objetivos, no funciones implementadas.
13. Estado al 26/11/2026
Publicado en GitHub: intro, menú, selección de riders y retratos, pantalla de distritos y documentación conceptual inicial.

Demostrado localmente por captura: map-demo.html, con un escenario cenital estático; paquete de tiles y sprites aún pendiente de certificación y commit.

No implementado: desplazamiento de cámara, conducción, bifurcaciones funcionales, obstáculos interactivos, puntuación, persistencia, publicidad y monetización.
14. Ruta y restricciones
- Próxima prioridad: validar y documentar la maqueta de Distrito Cero antes de programar movimiento.
- Meta orientativa: una beta pequeña jugable de Distrito Cero hacia julio de 2027, condicionada a pruebas y formación.
- Control: ninguna modificación de producción, Shopify, nube, anuncios o integraciones sin autorización separada.
- Portafolio: cada sprint deberá explicar qué se construyó, qué se aprendió y cómo se validó.
15. Registro de cambios
- V0.3: identidad, personajes, distritos y mecánica general de reparto.
- V0.4: modelo híbrido aprobado (avance automático, maniobras laterales y bifurcaciones); misión inicial por tramos, separación Puntos Rebel / OZMA COINS y criterios de aceptación.