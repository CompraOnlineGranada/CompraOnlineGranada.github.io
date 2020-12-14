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

# Acerca de este pequeño proyecto

Este proyecto se ha hecho con un presupuesto total de 0€, y ha sobrepasado todas nuestras expectativas.

Comenzamos con una pequeña lista de comercios que nos habíamos recomendado el uno al otro y pronto creamos un formulario para que nuestras amistades y familia pudiesen sugerir alguna tienda más. Lo que no sabíamos es que nuestra lista iba a hacerse viral...¡en menos de una semana! Un mes después de empezar el proyecto, la lista tiene más de 500 tiendas.

## Metodología de desarrollo

Este proyecto se planteó desde el principio como XKISS: Extreme <a href="https://es.wikipedia.org/wiki/Principio_KISS">Keep it Simple, Stupid</a>. La metodología de diseño KISS ("¡Hazlo sencillo, so tonto!") se centra en mantener los sistemas desarollados tan sencillos como sea posible. Pero nosotros además de mantenerlo sencillo, no teníamos mucho tiempo para invertir: los dos autores estamos trabajando en trabajos que nuestras familias consideran, ejem, respetables. De ahí que lo llevásemos al extremo: había que ser brutales con cualquier añadido que no fuese realmente necesario.

La lista comenzó su andadura como una simple hoja de cálculo pública en Google Sheet donde ibamos listando los comercios. Inicialmente esto era lo más sencillo puesto que es rápido de crear, fácil de actualizar y de navegar. También creamos un enlace corto para facilitar que la gente compartiera ese link, y no el enlace directo a la lista que no es amigable para los humanos. Pero cuando superó los 100 comercios, nos dimos cuenta de que:
<ul>
  <li>❌ Es complicado encontrar algo en concreto entre tanto comercio</li>
  <li>❌ La hoja de cálculo no se ajustaba bien a los móviles</li>
</ul>

## Implementación: solucionando los problemas de los usuarios

Siguiendo nuestro principio de XKISS nos dimos cuenta de que la <b>máxima prioridad</b> era solucionar estos dos problemas que tenían los usuarios de la lista:
<ul>
  <li>✔️ Poner la lista en un formato donde se pudiese buscar de algún modo. Lo importante es encontrar rápidamente la información.</li>
  <li>✔️ Ponerlo muy fácil para que la gente comparta con un tap/click (<i>¡Es que nadie piensa en nuestros padres!</i>)</li>
</ul>


### Ideas que se barajaron o que nos propusieron y finalmente descartamos

<ul>
  <li>Montar una web con Wordpress: queríamos algo super, super sencillo de montar.</li>
  <li>Hacer una app:  no queremos "encerrar" la información en una app, si no que el listado de comercios fuese lo más accesible y rápido de compartir como fuese posible.</li>
  <li>Buscar financiación pública/privada para montar una web: había que aprovechar el tirón viral de la lista, y queríamos mantenerlo dentro de nuestro presupuesto de 0€ y nuestra limitada disponibilidad.</li>
  <li>Usar Airtable para mostrar la lista: se descartó porque no está traducida la interfaz y nuestros principales usuarios no sabrían usar su sistema de filtros.</li>
  <li>Clasificar las tiendas en categorías y ofrecer un filtro usándolas: al hacer el ejercicio de intentar clasificar las tiendas salieron más de 50 categorías. No queremos que buscar la categoría sea ahora el problema...</li>
</ul>

### Implementación actual

Al final decidimos usar la biblioteca de JavaScript [DataTables](https://www.datatables.net) para presentar la lista ya que cargaba deprisa y buscaba aún más deprisa. Era fácil de maquetar ya que está preparada para trabajar junto con [Bootstrap](https://getbootstrap.com) y podríamos montar una web con buscador en cuestión de horas. Esto resuelve nuestro primer problema de nuestros usuarios. Además se puede traducir todo el texto de la interfaz. Luego añadimos el pequeño menú para compartir en redes sociales y apps de mensajería para resolver el segundo problema.

Para publicar la web usamos [Github Pages](https://pages.github.com), un alojamiento gratuito pero que sólo nos permite servir contenido estático. Pero eso no nos ha supuesto un problema, ya que la web es básicamente un único fichero HTML con JavaScript y CSS.

La base de datos principal sigue siendo Google Sheet, ya que es ahí donde recibimos los comercios a través del formulario y los revisamos manualmente. Como no podemos acceder dinámicamente dadas las limitaciones del alojamiento, lo que hacemos es descargar la hoja de cálculo pública en formato CSV y actualizarlo en el repositorio. Usando [GitHub Actions](https://github.com/features/actions) podemos hacer este proceso de una manera bastante cómoda con sólo pulsar un botón.

## Implementación: solucionando los problemas de los creadores

Recibimos bastantes más de 500 tiendas a través del formulario, y los datos no llegaban listos para ser publicados ya que solían estar incompletos: nos daban el nombre de la tienda y el municipio, pero ningún enlace a redes sociales. O los enlaces estaban mal, o se habían equivocado dándonos el nombre de la tienda en la red social. Para cada tienda, debíamos revisar manualmente la información comprobando que de verdad era una tienda en la provincia de Granada, que aceptaban pedidos y repartían a domicilio... y luego corregir erratas y encontrar los perfiles sociales correctos. Esto requería tanto tiempo de investigación que antes de que terminase la semana ya contábamos con la ayuda inestimable de dos personas más para procesar las tiendas nuevas que iban llegando. 

Manuel además creó una serie de macros para facilitar la creación de las URLS que se usaban en la tabla y enlazar los nombres de los comercios, y reducir así el tiempo manual de procesamiento. 

Al final conseguimos tener un método interno para procesar las tiendas lo más deprisa posible, manteniendo la lista maestra en la hoja de cálculo de la que tomamos los datos para la web aquí en GitHub. Otro punto para XKISS.

# Conclusiones

¡Nos lo hemos pasado muy bien con este proyecto! Descubriendo un sin fin de pequeños comercios de nuestra provincia y siendo efectivos con lo que podíamos hacer en un tiempo limitado, centrándonos siempre en ponérselo fácil a los usuarios de la lista. Los comercios son los protagonistas y necesitan toda la visibilidad que pudiésemos darles.

Muchos Granadinos y Granadinas no habían pensado en pedir por web/teléfono a sus comercios de toda la vida hasta que los vieron en la lista. Sólo necesitaban ver que las tiendas tenían también un escaparate online, que existe una manera distinta de contactar con sus tiendas de confianza. La lista fue el empujoncito que necesitaban para animarse y hacer un pedido a un negocio local, sin salir de casa. 
