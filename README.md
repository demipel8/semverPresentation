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

	- 1.
		- Hablemos de control de dependencias.
		- En el proyecto que trabajaba hace unos meses, se nos pidio hacer una demo a un cliente de nuestra aplicación.
	- 2.
		- A pesar de estar en una fase bastante temprana del desarrollo habiamos cerrado una version que ofrecia la funcionalidad minima, y la teniamos perfectamente preparada para el despliegue.
		- o eso creiamos...
	- 3.
		- Llega el dia de la presentación y,... suena el telefono. Nuestro compañero, desde Madrid. La aplicación no se podia ni levantar.
	- 4.
		- Resulta que aunque nosotros teniamos las versiones de nuestras dependencias fijadas, nuestras dependencias eran mas laxas con sus dependencias.
		- Consiguiendo que una mala actualizacion de un tercero, tirara por tierra meses de trabajo nuestro.
	- 5.
		- Vivimos en un momento 
