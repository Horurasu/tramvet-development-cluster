# “Entornos 3D Inclusivos: Puente Cultural hacia 'El Cerrito'”

-  Oscar Gael Mayen Tello
-  Sergio Rangel Vargas
-  Adrian Dolores Sanchez Rios
-  Vanessa Marshall
-  Ricardo Rivera Carrillo
-  Guadalupe Ilén Carrera Rivera


# Development Guide
Discord oficial de la comunidad de cluster [Discord](https://discord.com/invite/p3QVat6cD4).


## Unity y Cluster Creator Kit
Unity es un motor de juegos 2D/3D desarrollado y proporcionado por Unity Technologies.
Además de utilizarse para la creación de juegos, se utiliza en diversos campos, como las industrias manufactureras, la producción de vídeos y anime y las industrias de la construcción.

Para Cluster, Unity se utiliza para producir y cargar espacios virtuales.
Unity se puede utilizar de forma gratuita si se utiliza con fines personales y no comerciales.
El “Cluster Creator Kit” (denominado CCK en las siguientes secciones) es un kit de desarrollo distribuido por Cluster, Inc.
Al instalar CCK en Unity, puedes producir y cargar fácilmente tus mundos en un clúster.

También se incluyen elementos, activadores y trucos en CCK para crear diversas experiencias.

Instalar Unity con  Unity con el Cluster Creators Kit [Unity and CCK](https://medium.com/@cluster_official/installing-unity-and-the-cluster-creator-kit-c27b607cfb56).
 [Tutorial facil](https://medium.com/@cluster_official/installing-unity-and-the-cluster-creator-kit-c27b607cfb56).

Página que te proporciona un mundo descargable con funciones básicas [Mundo de Ejemplo](https://creator.cluster.mu/2022/07/18/template-sample-en/).


## Unity y Cluster Creator Kit Documentacion Oficial
 [ Documentacion](https://docs.cluster.mu/creatorkit/en/installation/install-creatorkit/).


> [!TIP]
> Sigue los tutoriales que se encuentran en los enlaces de arriba.

> [!CAUTION]
> La versión de Unity recomendada en el tutorial puede marcar errores en las funciones de colaboración.

-  Una vez que se hayan instalado la versión adecuada de Unity y UnityHub, abra UnityHub
  ![](https://i0.wp.com/creator.cluster.mu/wp-content/uploads/2023/02/CreatorsGuide-%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%83%AF%E3%83%BC%E3%83%AB%E3%83%89%E3%83%BB%E3%82%B5%E3%83%B3%E3%83%97%E3%83%AB%E3%83%97%E3%83%AD%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88_english_1.png?w=975&ssl=1)
-  Una vez iniciado, haga clic en "Abrir" en la parte superior derecha.
![](https://i0.wp.com/creator.cluster.mu/wp-content/uploads/2023/02/CreatorsGuide-%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%83%AF%E3%83%BC%E3%83%AB%E3%83%89%E3%83%BB%E3%82%B5%E3%83%B3%E3%83%97%E3%83%AB%E3%83%97%E3%83%AD%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88_english_2.png?w=970&ssl=1)
-  Podrá seleccionar una carpeta una vez que haya hecho clic en "Abrir", elija la carpeta del Proyecto Unity 'Template World'
  ![](https://i0.wp.com/creator.cluster.mu/wp-content/uploads/2023/02/unityhub220302-03.webp?w=728&ssl=1)
-  Asegúrese de hacer clic en la carpeta en lugar de en el contenido dentro de la carpeta.
> [!IMPORTANT]
> Para integrar a un desarrollador al mundo principal del proyecto, favor de hablar con el líder de proyecto para poder agregarlo desde unity y darle permisos de desarrollador.



## Componentes de Item
Item  es un término genérico para objetos interactivos que se pueden colocar en el mundo.
El componente Item es la base de cosas como MovableItem y GrabbableItem.


![](https://github.com/oskarinmate/tramvet-development-cluster/assets/119636778/c138898b-d2ca-4812-afab-a124b9bc5c15)

| Propiedad  | Significado  |
| ------------- | ------------- |
| Id  | Un valor que se establece automáticamente para identificar el elemento.  |
| Item Name  | Nombre del árticulo. Aparece al jugador cuando lo agarra, etc. Si está vacío, se mostrará el valor predeterminado. |
| Size  | El tamaño del área que ocupa principalmente el artículo.   |



### GrabbableItem
### Propiedad y Función

- **Agarre:** Una referencia a una transformación que especifica las coordenadas y la rotación del controlador. Si no se establece, se tomará el punto especificado por el jugador.

  
![](https://docs.cluster.mu/creatorkit/en/item-components/grabbable-item/inspector.png)


Para especificar el rango donde se pueden capturar los objetos, se requiere al menos un componente Collider en la misma jerarquía que el componente Elemento grabable o como hijo.


### MovableItem
### Propiedad y Función

- **MovableItem:** Los elementos móviles te permiten sincronizar la posición de los objetos entre jugadores en el mundo..

  
![](https://docs.cluster.mu/creatorkit/en/item-components/movable-item/inspector.png)


El componente MovableItem requiere un componente Rigidbody. El comportamiento del elemento móvil se puede controlar configurando el cuerpo rígido. Consulte el manual de Unity para obtener detalles sobre la configuración de Rigidbody.

Cuando el elemento móvil se mueve a una posición inferior a la altura de aparición, volverá a su posición inicial. Los elementos móviles generados dinámicamente mediante el truco Crear elemento se descartarán.

# Creación del terreno usando Herramientas 
Pro Terrain: Herramienta para crear y modificar terrenos realistas, permitiendo esculpir paisajes y agregar detalles como texturas, árboles y hierba.
### Agregar Terrain Sample Asset Pack:
Abre tu proyecto en Unity y descarga el Terrain Sample Asset Pack desde el Asset Store o desde un enlace proporcionado.


### Acceder al Package Manager:
Haz clic en el menú Window (Ventana) y selecciona Package Manager.
}
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgSerch1.png)

### Instalar Terrain Tools:
En el Package Manager, selecciona Unity Registry en el menú desplegable, busca Terrain Tools, y haz clic en Download e Install para instalar el paquete.

![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgSerch2.png)

### Usar Terrain Tools:
Para acceder a la herramienta, ve al menú Window, selecciona Terrain y luego Terrain Toolbox. Esto abrirá una pestaña desde la cual podrás crear y personalizar terrenos según tus necesidades.

![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgSerch3.png)

Crear el terreno: Comienza creando el terreno con las medidas adecuadas según las necesidades del proyecto.
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgSerch4.png)

Modificar la elevación: Selecciona la herramienta de elevar o bajar el terreno (Raise or Lower Terrain) y ajusta las montañas o elevaciones de acuerdo a lo que requiera el escenario.
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgSerch5.png)

### Uso de otras herramientas:
 Puedes utilizar diferentes herramientas para personalizar el terreno, como pintar superficies, generar árboles o arbustos, y ajustar la cantidad y distribución de estos elementos según lo que necesites.
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgSerch6.png)

## ProBuilder:
Herramienta de modelado 3D dentro de Unity para crear y editar geometría directamente en el editor, ideal para diseñar niveles y estructuras.

### Acceder al Package Manager:

Haz clic en el menú Window y selecciona Package Manager.
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgSerch7.png)

### Instalar ProBuilder:
En el Package Manager, selecciona Unity Registry en el menú desplegable, busca ProBuilder, y haz clic en Download e Install para instalar el paquete.
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgSerch8.png)

### Abrir ProBuilder:
Ve al menú Tools, selecciona ProBuilder, y luego ProBuilder Window. Se abrirá una ventana con todas las herramientas de ProBuilder listas para usar.
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgSerch9.png)






## Rotación de elementos visuales del museo:

Para agregar rotación a un objeto al interactuar con él en el entorno de desarrollo de Cluster, sigue estos pasos utilizando los __Gimmicks__ (scripts que generan eventos interactivos con el avatar):

1. **Agregar el script "Add Instant Torque Item Gimmick (Script)"**:
   - Este script se encargará de aplicar torque al objeto. En las propiedades del script, verás un campo llamado __Key__. 
   - En el campo __Key__, debes asignar un nombre único, ya que este identificador será utilizado por otros componentes para vincular la interacción.
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgAdrian1.png)

2. **Agregar el script "Interactive Item Trigger (Script)"**:
   - Este script permitirá que el avatar interactúe con el objeto.
   - En las propiedades de este script, en el campo __Target__, debes introducir el nombre que asignaste previamente en el campo __Key__ del script "Add Instant Torque Item Gimmick".
   - Este paso vincula la acción de aplicar torque al interactuar con el objeto.
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgAdrian2.png)

3. **Agregar el script "Movable Item (Script)"**:
   - Este script es necesario para que el objeto sea movible y responda al torque.
   - Asegúrate de que esté agregado dentro de los componentes  para que el objeto pueda rotar adecuadamente en cualquiera de sus ejes al aplicar el torque.
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgAdrian4.png)
Con estos tres componentes configurados correctamente, al interactuar con el objeto, se le aplicará un torque instantáneo, lo que causará su rotación en el eje especificado.

> [!TIP]
> para una mejor rotación utilizar un collider esférico __(Sphere Collider)__
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/imgAdrian5.png)

> [!IMPORTANT]
>el objeto no debe contar con gravedad 

## Zona 3
Un espacio en donde el usuario puede interactuar con modelos que serán  destruidos para revelar objetos escondidos, cuenta  con un amplio espacio para explorar y visualmente sea atractivo para todos
### Interaccion del Usuario
En Unity creamos piedras o elementos que se pueden destruir junto con la emisión de sonido como actividad principal de esta zona.
Para esto, creamos una carpeta vacía en el apartado de Assets del proyecto, en ella vamos a guardar el sonido que emitirán las rocas al ser destruidas.
![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/Captura%20de%20pantalla%202024-07-31%20191540.png?raw=true)

> [!TIP]
>Nombrar los audios y carpetas con nombres claros y descriptivos.

Después, vamos a crear un objeto vacío en la escena para poder almacenar y ordenar los Assets que van a ser destruidos posteriormente.

![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/Captura%20de%20pantalla%202024-07-31%20191827.png?raw=true)


Ese objeto principal deberá tener estas propiedades o componentes.

![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/Captura%20de%20pantalla%202024-07-31%20191915.png?raw=true)


> [!IMPORTANT]
> Los Scripts usados para todo el proyecto, ya se encuentran en el entorno de desarrollo de Cluster, solo hace falta presionar (Addcomponent) y buscar el Script  deseado.

Dentro del objeto vacío colocamos los Assets que se van a destruir con la interacción del Usuario y deberán tener las siguientes propiedades o componentes.


![](https://github.com/oskarinmate/Cluster_Project_images/blob/main/Captura%20de%20pantalla%202024-07-31%20192340.png?raw=true)






