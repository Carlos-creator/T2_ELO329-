# Requerimientos: Tarea 2 - Simulador Gráfico de ELOTelTags y Aplicación Find My

## Contexto General
- [cite_start]El objetivo es adaptar y extender la Tarea 1 para simular gráficamente usando JavaFX la interacción entre dispositivos (EloTelTags, celulares y tablets)[cite: 17].
- [cite_start]Se debe utilizar "programación conducida por eventos"[cite: 21]. [cite_start]Los eventos del usuario y del programa gobiernan la ejecución[cite: 23].
- [cite_start]Se debe implementar el patrón "modelo-vista-controlador" (MVC)[cite: 140]. 

## Configuración e Interfaz
- [cite_start]La configuración se carga mediante un archivo usando `FileChooser`[cite: 24].
- [cite_start]El archivo define: imagen de fondo [cite: 26][cite_start], delta_tiempo [cite: 27][cite_start], número de personas [cite: 28] [cite_start]y los datos de posición (x,y), rapidez y ángulos de cada dispositivo[cite: 30, 31, 32].
- [cite_start]Un menú "Simulation" debe ofrecer opciones "Play" y "Pause"[cite: 80].

## Dinámica de Simulación
- [cite_start]Los equipos se mueven confinados al territorio de la imagen y rebotan en los bordes[cite: 85, 86]. [cite_start]Al rebotar, mantienen la velocidad paralela e invierten la perpendicular[cite: 87].
- [cite_start]Los celulares reportan posición cada 4 segundos[cite: 88].
- [cite_start]Los EloTelTags buscan celulares cada 4 segundos y las tablets cada 5 segundos[cite: 88, 89]. [cite_start]Esta búsqueda emite un sonido corto y muestra un círculo que crece hasta un radio de 50 pixeles en 1 segundo[cite: 90, 92].

## Funcionalidad "Find My"
- [cite_start]Al presionar un equipo, se muestra un menú emergente con la opción "Find My"[cite: 94, 95].
- [cite_start]Al seleccionar "Find My", se abre una ventana con los bienes y dispositivos de la persona[cite: 95].
- [cite_start]Esta ventana debe actualizarse cada 1 segundo con la información de movimiento[cite: 104].

## Plan de Desarrollo Iterativo (Etapas a programar)
- [cite_start]**Etapa 1:** Leer archivo de configuración, generar ventana gráfica con menú (inactivo) y desplegar sólo celulares (`Stage1`, `Cellular`, `CellularView`, `Equipo`, `Territory`, `TerritoryView`)[cite: 114, 115].
- [cite_start]**Etapa 2:** Desplegar todos los equipos (agregar tags y tablets) y activar botones Play/Pause del menú Simulation[cite: 117, 118]. [cite_start]Aún no reportan posiciones[cite: 119].
- **Etapa 3:** Crear `ETNube`. Celulares reportan posiciones a la nube. Tags/Tablets muestran radar visual sin sonido. [cite_start]El menú "Find My" se despliega pero la ventana no se actualiza[cite: 120, 121, 122, 123, 124].
- [cite_start]**Etapa 4:** Cumplir todas las funcionalidades completas (sonido, actualización de ventana cada 1 segundo) y generar Javadoc para `EloTelTag`, `EloTelTagView` y superclases[cite: 125, 126, 136].