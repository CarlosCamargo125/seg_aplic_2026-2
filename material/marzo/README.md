# Material cursado durante el mes de marzo

## _Unidad 2_: El panorama de la seguridad informática hoy

1. `2026.03.03`

   - Evaluación de los modelos de riesgo FMEA / OCTAVE Allegro realizados
     por los alumnos

   **Otros temas:**

   _Ligeramente_ vinculado con el tema visto anteriormente (modelos de
   riesgo): Matthew Garrett publicó un texto acerca de la [confianza sobre
   los _blobs_
   binarios](https://codon.org.uk/~mjg59/blog/p/to-update-blobs-or-not-to-update-blobs/)
   que se distribuyen, típicamente para ejecutar en procesadores
   _no-primarios_ de nuestro equipo de cómputo (simplificando
   fuertemente). Esto se conecta con una [discusión al respecto que se está
   teniendo](https://lists.debian.org/debian-devel/2026/02/threads.html#00297)
   (...otra vez 🙄) en Debian. Considero que es un tema interesante para el
   grupo actual para dedicarle un poco de plática 🙂

2. `2026.03.05`

	**Modelos de ataque**

	Los modelos de riesgo que vimos en las clases anteriores sirven para
    identificar nuestros _principales activos_ y las _amenazas_ que puede
    haber sobre ellos — _qué queremos o requerimos proteger_.

	En contraste, los modelos de ataque catalogan y describen _Tácticas,
    Técnicas y Procedimientos_ que utilizan nuestros adversarios para
    comprometer nuestra información. Consisten _conocimiento especializado
    y estructurado_, ya específico al área de seguridad informática, sobre
    el _comportamiento real_ y desde una _perspectiva adversarial_,
    permitiéndonos avanzar de una _defensa reactiva_ (corregir
    vulnerabilidades detectadas) a una _defensa proactiva_ (anticipar y
    detectar campañas de ataque).

     - [Lockheed Martin Cyber Kill
       Chain](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html)
       (_Cadena de Ataque Cibernético_) desarrollado como parte del modelo
       /Intelligence Driven Defense/ para identificar y prevenir actividad
       de intrusiones (2011). Identifica los pasos que un adversario debe
       seguir para montar un reto APT (/Advanced Persistent Threat/), para
       ayudar al defensor a _romper la cadena_:

	   1. Reconocimiento
	   2. Armamento o _armificación_ (_weaponization_)
	   3. Entrega
	   4. Explotación
	   5. Instalación
	   6. Control y Comando (C2)
	   7. Acción sobre los objetivos

	   Ojo: Hay críticas importantes al modelo:

	   1. Es un modelo muy _lineal y secuencial_
       2. Se enfoca demasiado en APTs, omite muchos otros tipos de amenaza,
          incluyendo ataques internos o robos de identidad
       3. Falta de contexto post-explotación

     - [Microsoft
       STRIDE](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool-threats#stride)
       ayuda a modelar y clasificar amenazas y ataques para tenerlos
       presentes de forma preventiva, enfocado a aplicarlo conforme se
       **desarrolla** un sistema (y no cuando éste ya está
       **desplegado**). STRIDE toma su nombre de _**S**poofing,
       **T**ampering, **R**epudiation, **I**nformation disclosure,
       **D**enial of service, **E**levation of privileges_, las seis
       categorías de amenazas que un desarrollador debe considerar al
       desarrollar cualquier componente.

	   Para aplicar STRIDE es necesario seguir una metodología de
       desarrollo con un componente visual, como lo hace la [Herramienta de
       Modelado de
       Amenazas](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool-getting-started),
       en que cada uno de los tipos de objeto representados _responde_ a
       determinadas categorías de amenazas (Procesos (Círculos) ⇒
       T,R,I,D,E; Flujos de Datos (Flechas) ⇒ T,I,D; Almacenes de Datos
       (Líneas) ⇒ T,R,I y a veces D; Entidades Externas (Rectángulos) ⇒ S).

     - [MITRE ATT&CK](https://attack.mitre.org/) _Adversarial Tactics,
       Techniques, and Common Knowledge_ (2013–, actualización bianual)
       detalla técnicas para distintos entornos, describiendo el /cómo/ y
       /por qué/ de /cada paso/ en el ciclo de vida de un ataque.

	   Surge de cierta manera reaccionando ante el _Cyber Kill Chain_,
       describiendo el modelo de ataque ya no como una _cadena_, sino como
       un _laberinto_, con múltiples posibilidades a cada paso. Si Cyber
       Kill Chain da las 7 fases de un crimen (vigilar, entrar, robar,
       huir...), ATT&CK es el manual que usan los detectives, lleno de
       huellas dactilares, _modus operandi_ de cada ladrón, las
       herramientas que usan para forzar cerraduras y cómo se mueven dentro
       de la casa una vez que han entrado, etc.

	   Se ha convertido en el estándar de facto para describir el
       comportamiento de los atacantes después de la intrusión inicial. Es
       una matriz detallada de tácticas (el "por qué") y técnicas (el
       "cómo") que los adversarios utilizan.

     - [MITRE D3FEND](https://d3fend.mitre.org/) siguiente paso natural de
       ATT&CK: «gráfica de conocimiento de contramedidas de ciberseguridad»

