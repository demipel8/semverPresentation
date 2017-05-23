# Semantic Veresioning

  - Introducción:
    - frase: hablemos de versionado de dependencias.
    - Idea base: Vivimos en un mundo dominado por las dependencias en el que una falta
      de control puede enviar a paseo todo aquello en lo que estamos trabajando
    - Apoyo, historia personal: Pete en NBN23 al desplegar en el client por culpa de una mala actualización una de nuestras dependencias.
    - EVITAR VERSION LOCK Y VERSION PROMISCUITY, BUSCAR ALGO EN MEDIO
    - Una gran ayuda es usar un sistema de versiones solido, con un contrato que todo el ecosistema pueda seguir. Semantic version nos propone una solución

  - Cuerpo:
    - Que es?: Un simple set de reglas y requerimientos que dictan como establecer un numero de version y su incremento.
    - Como funciona?: Lo primero que has de hacer es declarar una API pública, ya sea en forma de documentación y implicito en el código, lo importantees que sea clara y precisa. A partir de este momento cada modificación en el código supondra una modificación en la version del software.
    - Formato: MAJOR.MINOR.PATCH
    - Reglas para cambiar de version:
      - PATCH: Correciones de errores que son compatibles con la API actual
      - MINOR: Adiciones a la API que rompen la retrocompatibilidad
      - MAJOR: Cambios incompatibles con la API actual
      - Una vez una version es lanzada, NO SE PUEDE modificar.
    - UN EJEMPLO
    - Idea: Los numeros de version y cambios muestran la evolución del codigo que hay detras.
    - Casos adicionales:
      - 0.y.z: Cualquier cosa puede cambiar. La API pública no se considera estable.
      - 1.0.0: El contrato de la API publica se formaliza
      - versiones de pre-lanzamiento: El numero de la version seguido de un guion y el nombre del patch. Ej. 2.13.4-alpha

  - Conslusión:
    - La mayoria de equipos ya hace algo parecido, pero no es suficiente. Sin una especificacion formal y un compromiso por parte del sector con dicha especificacion, los numeros de version no valen de nada.
    - Por responsabilidad y por respeto al resto decompañeros del sector se responsable con la gestion de versiones del software que crees para ser usado por otros.
    - Así podremos evitar dolores de cabeza a muchos compañeros y a nosotros mismos.

## Ignite

1.
   - Hablemos de control de dependencias.
   - En el proyecto que trabajaba hace unos meses, se nos pidio hacer una demo a un cliente de nuestra aplicación.
2.
   - A pesar de estar en una fase bastante temprana del desarrollo habiamos cerrado una version que ofrecia la funcionalidad minima, y la teniamos perfectamente preparada para el despliegue.
   - o eso creiamos...
3.
   - Llega el dia de la presentación y,... suena el telefono. Nuestro compañero, desde Madrid. La aplicación no se podia ni levantar.
4.
   - Resulta que aunque nosotros teniamos las versiones de nuestras dependencias fijadas, nuestras dependencias eran mas laxas con sus dependencias.
   - Consiguiendo que una mala actualizacion de un tercero, tirara por tierra meses de trabajo nuestro.
5.
   - El software que desarrollamos esta dominado por dependencias externas. Desde librerias de terceros que usamos para facilitarnos la vida, servicios externos que consumimos, incluido el tooling de desarrollo, testing y despliegue.
6.
   - La falta de control de estado actual, y la evolución de estas dependencias nos puede llevar desde dolores de cabeza e incertidumbre en el workflow habitual hasta fallos en producción como el citado anteriormente
7.
   - Necesitamos una forma de gestión que nos permita manejar de forma solida, algo que evite esa actualización imprevista, VERSION PROMISCUITY, pero que no nos ate tanto que no podamos beneficiarnos de los adelantos que aportan otros miembros de la comunidad, VERSION LOCKING.
8.
   - SEMVER, al rescate.
	 - El versionado semantico es un simple set de reglas y requerimientos que dictan como establecer un numero de version y su incremento.
9.
   - Lo primero que has de hacer es declarar una API pública. Tu API pública, ya sea en forma de documentación o implicita en el código, forma el contrato que tienes con los usuarios de tu proyecto. Expondra qué y como se pueden hacer las cosas con el.
10.
   - A partir de ese momento, cada cambio en el código podra afectar a la API pública por lo se mostrara con un cambio en la versión.
   - De manera que puedas transmitir a los usuarios de tu software como actuar ante esa modificación.
11.
   - ¿Como se gestiona? Tres números, con tres siginificados asociados: MAJOR.MINOR.PATCH
12.
   - Reglas para cambiar de version de menor a mayor:
      - PATCH: Correciones de errores que son compatibles con la API actual
      - MINOR: Adiciones a la API que no rompen la retrocompatibilidad
      - MAJOR: Cambios incompatibles con la API actual
   - Una vez una version es lanzada, NO SE PUEDE modificar.
13.
   - Idea subyacente: Los numeros de version y cambios muestran la evolución del código que hay detras.
   - Ofreciendo a los usuarios una forma consistente de enfrentar la evolucion de nuestras dependencias.
14.
   - Algunas dudas mas comunes:
   - Que pasa si el proyecto esta en una versión temprana y la API pública no para de cambiar? tengo que llegar a la version 40.32.168 antes de tener una version estable.
15.
   - 0.y.z: Cualquier cosa puede cambiar. La API pública no se considera estable.
16.
   - Y que pasa si quiero hacer una pre-release? tengo que subir numero de version ordinario.
   - 1.0.0: El contrato de la API publica se formaliza
   - versiones de pre-lanzamiento: El numero de la version seguido de un guion y el nombre del patch. Ej. 2.13.4-alpha
17.
   - La mayoria de equipos ya hace algo parecido, pero no es suficiente. Sin una especificacion formal y un compromiso por parte del sector con dicha especificacion, los numeros de version no valen de nada.
18.
   - Por responsabilidad y por respeto al resto de compañeros del sector se responsable con la gestion de versiones del software que crees para ser usado por otros.
19.
   - Por simplicidad, complicidad y respeto al resto de la comunidad, usemos SEMVER como especificación.
   - Con algo tan facil como como Major Minor y Patch, podremos evitar dolores de cabeza a muchos compañeros y a nosotros mismos.
20.
   - Gracias y a versionar.

## Bibliography
[Semver.org](http://semver.org/)
