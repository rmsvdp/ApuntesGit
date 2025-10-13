# Acerca de esta sección
Una buena práctica es un conjunto de proedimientos que da un resultado acpetable para resolver un derteminado problema

# Técnica estándar de programación

Sin entrar en técnicas más complejas para coordinación de equipos y dependiendo además del tamaño de la aplicación, lo más normal es mantener una rama principal (main/master) de la que vamos sacando
ramas para las funcionalidades (features) principales.

![Gestión de Ramas](/assets/git-flow.png)

Esto permite ir desarrollando en paralelo y posteriormente incoporar los resultados a la rama principal
Se suele también abrir ramas específicas para resolver bugs que se cierran en la rama donde se localizan o en la rama principal.
Este gráfico resume este tipo de técnicas.

# Versionado

Ciertos momentos del desarrollo suponen la liberación de un determinado módulo o versión de la aplicación, para ello git ofrece el comando tag,
que permite etiquetar un determinado COMMIT

Si se utiliza Github como respositorio de la nube, este dispone de una sección especial denominada releases, que permiten, de una vez empaquetar
fuentes y ejecutables.
Para generar una release, es preciso utilizar un TAG previamente creado o crearlo en el momento.

# Consideraciones

- Siempre antes de un commit -m, ejecuta un git add para capturar tanto los nuevos archivos como los modificados
- Manten una disciplina de equipo , aislando en lo posible el desarrollo para que dos personas no estén editando versiones del mismo archivo
- Evita los conflictos, resuélvelos mediante los comandos a tal efecto o si dispones de una versión fiable , vuelve a regenerar el proyecto local con git clone
- Evalúa la facilidad pull request de github para sincronizar el desarrollo
