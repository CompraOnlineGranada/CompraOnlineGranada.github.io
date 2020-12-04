# Compra Online Granada
Listado público de pequeños comercios de la provincia de Granada con venta online y envío a domicilio

Web: https://compraonlinegranada.github.io

Hecho con ❤️ en Granada por:

<ul>
  <li><a href="https://www.linkedin.com/in/draxus/">Manuel Martín</a></li>
  <li><a href="https://www.linkedin.com/in/annalogik/">Anna P. Martínez</a> </li>
</ul>

# Software y datos libres

El código de este repositorio está disponible bajo la <a href="https://es.wikipedia.org/wiki/Licencia_MIT">licencia MIT</a>.

Los datos (listado de comercios) están disponibles bajo la <a href="https://es.wikipedia.org/wiki/Licencia_Abierta_de_Bases_de_Datos">licencia ODbl</a>.

# Acerca de este pequeño projecto

Este proyecto se ha hecho con un presupuesto total de 0€, y ha sobrepasado todas nuestras expectativas.

Comenzamos con una pequeña lista de comercios que nos habíamos recomendado el uno al otro y pronto creamos un formulario para que nuestras amistades y familia pudiesen sugerir alguna tienda más. Lo que no sabíamos es que nuestra lista iba a hacerse viral...¡en menos de una semana! Un mes después de empezar el proyecto, la lista tiene más de 500 tiendas.

## Metodología de desarrollo

Este proyecto se planteó desde el principio como XKISS: Extreme <a href="https://es.wikipedia.org/wiki/Principio_KISS">Keep it Simple, Stupid</a>. La metodología de diseño KISS ("¡Hazlo sencillo, so tonto!") se centra en mantener los sistemas desarollados tan sencillos como sea posible. Pero nosotros además de mantenerlo sencillo, no teníamos mucho tiempo para invertir: los dos autores estamos trabajando en trabajos que nuestras familias consideran, ejem, respetables. De ahí que lo llevásemos al extremo: había que ser brutales con cualquier añadido que no fuese realmente necesario.

La lista comenzó su andadura como una simple hoja de cálculo donde ibamos listando los comercios. Inicialmente esto era lo más sencillo puesto que es rápido de crear, fácil de actualizar y de navegar. También creamos un enlace corto para facilitar que la gente compartiera ese link, y no el enlace directo a la lista que no es amigable para los humanos. Pero cuando superó los 100 comercios, nos dimos cuenta de que:
<ul>
  <li>La gente no sabe compartir URLs y no se fijan en los enlaces cortos</li>
  <li>La gente no sabe buscar en hojas de cálculo</li>
</ul>

Siguiendo nuestro principio de XKISS nos dimos cuenta de que la <b>máxima prioridad</b> era solucionar dos problemas que tenían los usuarios de la lista:
<ul>
  <li>Poner la lista en un formato donde se pudiese buscar de algún modo. Lo importante es encontrar rápidamente la información.</li>
  <li>Ponerlo muy fácil para que la gente comparta con un tap/click (<i>¡Es que nadie piensa en nuestros padres!</i>)</li>
</ul>

### Ideas que se barajaron o que nos propusieron y rápidamente descartamos

<ul>
  <li>Montar una web con Wordpress: queríamos algo super, super sencillo de montar.</li>
  <li>Hacer una app: no estamos locos y no queremos "encerrar" la información en una app.</li>
  <li>Buscar financiación pública/privada para montar una web: había que aprovechar el tirón viral de la lista, y queríamos mantenerlo dentro de nuestro presupuesto de 0€</li>
  <li>Usar Airtable para mostrar la lista: se descartó porque no está traducida la interfaz y nuestros usuarios no sabrían usar sus filtros</li>
  <li>Clasificar las tiendas en categorías y ofrecer un filtro usándolas: al hacer el ejercicio de intentar clasificar las tiendas salieron más de 50 categorías. No queremos que buscar la categoría sea ahora el problema...</li>
</ul>

### Implementación actual

Al final decidimos usar https://www.datatables.net/ para presentar la lista ya que cargaba deprisa y buscaba aún más deprisa. Era fácil de maquetar ya que usa Bootstrap y podríamos montar una web con buscador en cuestión de horas. Esto resuelve nuestro primer problema de nuestros usuarios. Además se puede traducir todo lo que sale por pantalla. Luego añadimos el pequeño menú para compartir en redes sociales y apps de mensajería para resolver el segundo problema.


