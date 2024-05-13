# “Entornos 3D Inclusivos: Puente Cultural hacia 'El Cerrito'”

-  Oscar Gael Mayen Tello
-  Sergio Rangel Vargas
-  Juan Manuel López González

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







