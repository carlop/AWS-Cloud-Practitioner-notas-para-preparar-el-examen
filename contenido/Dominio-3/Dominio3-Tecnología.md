# Dominio 3: Tecnología

- Definir métodos de implementación y funcionamiento en la nube de AWS
    - Identificar formas diferentes de aprovisionamiento y funcionamiento en la nube de AWS a un alto nivel
        - Acceso mediante programación, API, SDK, consola de administración de AWS, CLI, Infrastructure as Code
    - Identificar diferentes tipos de modelos de implementación en la nube
        - Todo en la nube o nativo en la nube
        - Híbrido
        - En las instalaciones
    - Identificar opciones de conectividad
        - VPN
        - AWS Direct Connect
        - Internet pública
- Definir la infraestructura global de AWS
    - Describir las relaciones entre las regiones, las zonas de disponibilidad y las ubicaciones de borde
    - Describir cómo lograr alta disponibilidad mediante el uso de varias zonas de disponibilidad
        - Recordar que la alta disponibilidad se logra mediante el uso de varias zonas de disponibilidad
        - Reconocer que las zonas de disponibilidad no comparten puntos únicos de error
    - Describir cuándo se debe considerar el uso de varias regiones de AWS
        - Recuperación ante desastres y continuidad del negocio
        - Latencia baja para usuarios finales
        - Soberanía de los datos
    - Describir los beneficios de las ubicaciones de borde a un alto nivel
        - Amazon CloudFront
        - AWS Global Accelerator
- Identificar los servicios principales de AWS
    - Describir las categorías de servicios en AWS (informática, almacenamiento, red, base de datos)
    - Identificar los servicios informáticos de AWS
        - Reconocer que existen diferentes familias de informática
        - Reconocer los diferentes servicios que proporcionan informática (por ejemplo, AWS Lambda en comparación con Amazon Elastic Container Service [Amazon ECS] o Amazon EC2, etcétera)
        - Reconocer que la elasticidad se logra a través de Auto Scaling
        - Identificar el fin de los balanceadores de carga
    - [Servicios de almacenamiento de AWS](#servicios-de-almacenamiento-de-aws)
        - [Almacenamiento de objetos](#almacenamiento-de-objetos)
        - [Amazon S3](#amazon-s3)
        - [Almacenes de instancias](#almacenes-de-instancias)
        - [Amazon Elastic Block Store (Amazon EBS)](#amazon-elastic-block-store-amazon-ebs)
        - [Amazon S3 Glacier](#amazon-s3-glacier)
        - [AWS Snowball](#aws-snowball)
        - [Amazon Elastic File System (Amazon EFS)](#amazon-elastic-file-system-amazon-efs)
        - [AWS Storage Gateway](#aws-storage-gateway)
    - Identificar los servicios de redes de AWS
        - Identificar VPC
        - Identificar grupos de seguridad
        - Identificar el fin de Amazon Route 53
        - [AWS Direct Connect](#aws-direct-connect)
    - Identificar diferentes servicios de bases de datos de AWS
        - Instalar bases de datos en Amazon EC2 en comparación con las bases de datos que administra AWS
        - Identificar Amazon RDS
        - Identificar Amazon DynamoDB
        - Identificar Amazon Redshift
- Identificar recursos para respaldar la tecnología
    - Reconocer que hay documentación (prácticas recomendadas, documentos técnicos, Centro de conocimientos de AWS, foros, blogs)
    - Identificar los distintos niveles y el alcance de AWS Support
        - AWS Abuse
        - Casos de AWS Support
        - Premium Support
        - Directores técnicos de cuentas
    - Reconocer que existe una red de socios (Marketplace, terceros) que incluye proveedores de software independientes e integradores de sistemas
    - Identificar fuentes de asistencia técnica y conocimientos de AWS, incluidos servicios profesionales, arquitectos de soluciones, capacitación y certificación, y la red de socios de Amazon
    - Identificar los beneficios de usar AWS Trusted Advisor

## Métodos de implementación y funcionamiento en la nube de AWS
### Identificar opciones de conectividad

#### VPN

#### AWS Direct Connect

**AWS Direct Connect** es un servicio que le permite establecer una conexión privada dedicada entre su centro de datos y una VPC.  


La conexión privada que proporciona AWS Direct Connect le ayuda a reducir los costos de red y a aumentar la cantidad de ancho de banda que puede viajar a través de la red.

#### Internet pública


## Servicios de almacenamiento de AWS

### Almacenamiento de objetos

![Almacenamiento de objetos](/contenido/Dominio-3/almacenamiento-de-objetos.png "Almacenamiento de objetos")

En el almacenamiento de objetos, cada objeto consta de datos, metadatos y una clave.

Los datos pueden ser una imagen, un video, un documento de texto o cualquier otro tipo de archivo. Los metadatos contienen información sobre qué son los datos, cómo se usan, el tamaño del objeto, etc. La clave de un objeto es su identificador único.

Recuerde que cuando modifica un archivo en el almacenamiento de bloques, solo se actualizan las piezas que se modifican. Cuando se modifica un archivo del almacenamiento de objetos, se actualiza todo el objeto.


### Amazon S3

[Amazon Simple Storage Service (Amazon S3)](https://aws.amazon.com/s3/) es un servicio que proporciona almacenamiento a nivel de objetos. Amazon S3 almacena los datos como objetos en buckets.

Puede cargar cualquier tipo de archivo en Amazon S3, como imágenes, videos, archivos de texto, etc. Por ejemplo, puede utilizar Amazon S3 para almacenar archivos de copia de seguridad, archivos multimedia de un sitio web o documentos archivados. Amazon S3 ofrece espacio de almacenamiento ilimitado. El tamaño máximo de archivo de un objeto de Amazon S3 es de 5TB.

Al cargar un archivo en Amazon S3, pueden establecer permisos para controlar la visibilidad y el acceso a él. También puede utilizar la función de control de versiones de Amazon S3 para realizar un seguimiento de los cambios en los objetos a lo largo del tiempo.

#### Clases de almacenamiento de Amazon S3

Con Amazon S3, solo paga por lo que utiliza. Puede elegir entre una variedad de clases de almacenamiento para seleccionar la que mejor se adapte a sus necesidades empresariales y económicas. Al seleccionar una clase de almacenamiento de Amazon S3, tenga en cuenta estos dos factores:

- Con qué frecuencia piensa recuperar sus datos
- Qué tanta disponibilidad deben tener los datos

##### S3 Standard

- Diseñado para los datos a los que se accede con frecuencia
- Almacena datos en un mínimo de tres zonas de disponibilidad

S3 Standard proporciona alta disponibilidad para los objetos. Esto lo convierte en una buena opción para una amplia gama de casos de uso, como sitios web, distribución de contenido y análisis de datos. S3 Standard tiene un costo superior al de otras clases de almacenamiento destinadas al almacenamiento de archivos y datos a los que se accede con poca frecuencia.

##### S3 Standard-Infrequent Access (S3 Standard-IA)

- Ideal para datos a los que se accede con poca frecuencia
- Similar a S3 Standard, pero tiene un precio de almacenamiento más bajo y un precio de obtención más alto

S3 Standard-IA es ideal para los datos a los que se accede con poca frecuencia, pero requiere una alta disponibilidad cuando es necesario. Tanto S3 Standard como S3 Standard-IA almacenan datos en un mínimo de tres zonas de disponibilidad. S3 Standard-IA proporciona el mismo nivel de disponibilidad que S3 Standard, pero con un precio de almacenamiento más bajo y un precio de recuperación más alto.

###### S3 One Zone-Infrequent Access (S3 One Zone-IA)

- Almacena datos en una única zona de disponibilidad
- Tiene un precio de almacenamiento inferior al de S3 Standard-IA

En comparación con S3 Standard y S3 Standard-IA, que almacenan datos en un mínimo de tres zonas de disponibilidad, S3 One Zone-IA almacena datos en una única zona de disponibilidad. Esto hace que sea una buena clase de almacenamiento a tener en cuenta si se cumplen las siguientes condiciones:

- Desea ahorrar costos de almacenamiento.
- Puede reproducir fácilmente los datos en caso de que se produzca un error en la zona de disponibilidad.

###### S3 Intelligent-Tiering

- Ideal para datos con patrones de acceso desconocidos o cambiantes
- Requiere una pequeña tarifa mensual de monitoreo y automatización por objeto

En la clase de almacenamiento S3 Intelligent-Tiering, Amazon S3 supervisa los patrones de acceso de los objetos. Si no ha accedido a un objeto durante 30 días consecutivos, Amazon S3 lo traslada automáticamente al nivel de acceso poco frecuente, S3 Standard-IA. Si accede a un objeto en el nivel de acceso poco frecuente, Amazon S3 lo traslada automáticamente al nivel de acceso frecuente, S3 Standard.

###### S3 Glacier

- Almacenamiento de bajo costo diseñado para archivar datos
- Puede obtener objetos desde en unos minutos hasta en unas horas

S3 Glacier es una clase de almacenamiento de bajo costo ideal para archivar datos. Por ejemplo, puede utilizar esta clase de almacenamiento para almacenar registros de clientes archivados o archivos de fotos y videos antiguos.

###### S3 Glacier Deep Archive

- Clase de almacenamiento de objetos de menor costo ideal para archivar
- Puede obtener objetos en 12 horas

Al decidir entre Amazon S3 Glacier y Amazon S3 Glacier Deep Archive, tenga en cuenta la rapidez con la que necesita obtener los objetos archivados. Puede obtener objetos almacenados en la clase de almacenamiento de S3 Glacier desde en unos minutos hasta en unas horas. En comparación, puede obtener objetos almacenados en la clase de almacenamiento de S3 Glacier Deep Archive en un plazo de 12 horas.

### Almacenes de instancias

Los volúmenes de almacenamiento a nivel de bloque se comportan como discos duros físicos.

Un **almacén de instancias** proporciona almacenamiento temporal a nivel de bloques para una instancia de Amazon EC2. Un almacén de instancias es un almacenamiento en disco que está conectado físicamente a la computadora host para una instancia de EC2 y, por lo tanto, tiene la misma vida útil que la instancia. Cuando se termina la instancia, se pierden los datos del almacén de instancias.

#### Ejemplos

Se está ejecutando una instancia de Amazon EC2 con un almacén de instancias adjunto.

![Ejemplo almacen de instancias 1](/contenido/Dominio-3/ejemplo-almacen-instancias-1.png "Ejemplo almacen de instancias 1")

La instancia se detiene o termina.

![Ejemplo almacen de instancias 2](/contenido/Dominio-3/ejemplo-almacen-instancias-2.png "Ejemplo almacen de instancias 2")

Se eliminan todos los datos del almacén de instancias adjunto.

![Ejemplo almacen de instancias 3](/contenido/Dominio-3/ejemplo-almacen-instancias-3.png "Ejemplo almacen de instancias 3")

Las instancias de Amazon EC2 son servidores virtuales. Si inicia una instancia desde un estado detenido, la instancia podría iniciarse en otro host, donde el volumen del almacén de instancias usado anteriormente no existe. Por lo tanto, AWS recomienda los almacenes de instancias para casos de uso que implican datos temporales que no necesita a largo plazo.

![Ejemplo almacen de instancias 4](/contenido/Dominio-3/ejemplo-almacen-instancias-4.png "Ejemplo almacen de instancias 4")

### Amazon Elastic Block Store (Amazon EBS)

[Amazon Elastic Block Store (Amazon EBS)](https://aws.amazon.com/ebs) es un servicio que proporciona volúmenes de almacenamiento a nivel de bloque que puede utilizar con instancias de Amazon EC2. Si detiene o termina una instancia de Amazon EC2, todos los datos del volumen de EBS adjunto siguen estando disponibles.

Para crear un volumen de EBS, debe definir la configuración (como el tamaño y el tipo de volumen) y aprovisionarlo. Después de crear un volumen de EBS, se puede adjuntar a una instancia de Amazon EC2.

Dado que los volúmenes de EBS son para datos que deben persistir, es importante hacer una copia de seguridad de los datos. Puede realizar copias de seguridad progresivas de volúmenes de EBS mediante la creación de instantáneas de Amazon EBS.

#### Instantáneas de Amazon EBS

![Instantáneas de Amazon EBS](/contenido/Dominio-3/instantaneas-de-ebs.png "Instantáneas de Amazon EBS")

Una instantánea de EBS es una copia de seguridad progresiva. Esto significa que la primera copia de seguridad realizada de un volumen copia todos los datos. Para las copias de seguridad posteriores, solo se guardan los bloques de datos que han cambiado desde la última instantánea. 

Las copias de seguridad progresivas son diferentes de las copias de seguridad completas, en las que todos los datos de un volumen de almacenamiento se copian cada vez que se realiza una copia de seguridad. La copia de seguridad completa incluye datos que no han cambiado desde la copia de seguridad más reciente.

### Amazon S3 Glacier

Las clases de almacenamiento de Amazon S3 Glacier se crearon específicamente para el archivado de datos y le ofrecen el mayor rendimiento, la mayor flexibilidad de recuperación y el menor costo de almacenamiento de archivos en la nube. Todas las clases de almacenamiento S3 Glacier ofrecen escalabilidad prácticamente ilimitada y están diseñadas para lograr un 99,999999999 % (11 nueves) de durabilidad de datos. Las clases de almacenamiento S3 Glacier ofrecen opciones para acceder más rápidamente a los datos de archivos y el menor costo en almacenamiento de archivos en la nube.

![Amazon S3 Glacier](/contenido/Dominio-3/s3-glacier-1.png "Amazon S3 Glacier")

Puede elegir entre tres clases de almacenamiento de archivos optimizadas para diferentes patrones de acceso y duraciones del almacenamiento.

#### S3 Glacier Instant Retrieval

S3 Glacier Instant Retrieval ofrece el almacenamiento de menor costo, hasta un 68 % menor (que S3 Standard-Infrequent Access), para datos de larga duración a los que se accede una vez por trimestre y que requieren una recuperación en milisegundos. Está diseñado para datos a los que rara vez se accede pero a los que se necesita acceso inmediato en casos de uso sensible al rendimiento como alojamiento de imágenes, aplicaciones que permiten compartir archivos en línea, imágenes médicas e historias clínicas, activos de los medios de comunicación e imágenes aéreas y satelitales. S3 Glacier Instant Retrieval ofrece alta durabilidad, alto rendimiento y baja latencia similares a los de S3 Standard-IA, con un precio menor por GB de almacenamiento y un precio ligeramente mayor por GB de recuperación. S3 Glacier Instant Retrieval está diseñado para brindar una durabilidad de los datos del 99,999999999 % (11 nueves) y una disponibilidad del 99,9 % mediante el almacenamiento redundante de los datos en varias zonas de disponibilidad de AWS separadas físicamente en un año determinado.

![S3 Glacier Instant Retrieval](/contenido/Dominio-3/s3-glacier-2.png "S3 Glacier Instant Retrieval")

#### S3 Glacier Flexible Retrieval

S3 Glacier Flexible Retrieval ofrece almacenamiento de bajo costo, hasta un 10 % menor (que S3 Glacier Instant Retrieval), para los datos de archivo a los que se accede 1 o 2 veces al año y se recuperan de manera asíncrona. S3 Glacier Flexible Retrieval, es la clase de almacenamiento ideal para los datos de archivado que no requieren acceso inmediato, pero necesitan la flexibilidad de recuperar grandes conjuntos de datos sin costo alguno, como los casos de uso de copias de seguridad o recuperación de desastres. S3 Glacier Flexible Retrieval ofrece las opciones de recuperación más flexibles que equilibran el costo con tiempos de acceso que varían de minutos a horas y con recuperaciones masivas gratuitas. Esta es una solución ideal para las necesidades de copia de seguridad, recuperación de desastres, almacenamiento de datos fuera del sitio y para cuando algunos datos deben recuperarse ocasionalmente en minutos y no desea preocuparse por los costos. S3 Glacier Flexible Retrieval está diseñado para brindar una durabilidad de los datos del 99,999999999 % (11 nueves) y una disponibilidad del 99,99 % mediante el almacenamiento redundante de los datos en varias zonas de disponibilidad de AWS separadas físicamente en un año determinado.

![S3 Glacier Flexible Retrieval](/contenido/Dominio-3/s3-glacier-3.png "S3 Glacier Flexible Retrieval")

#### S3 Glacier Deep Archive

S3 Glacier Deep Archive ofrece el almacenamiento de menor costo, hasta un 75 % menos (que S3 Glacier Flexible Retrieval), para datos de archivo de larga duración a los que se accede menos de una vez al año y que se recuperan de manera asincrónica. A tan solo 0,00099 USD por GB al mes (o 1 USD por TB al mes), S3 Glacier Deep Archive ofrece el almacenamiento en la nube de menor costo, a precios significativamente más bajos que el almacenamiento y el mantenimiento de datos en las instalaciones en cintas o el archivado de datos en ubicaciones remotas. S3 Glacier Deep Archive es una alternativa a las cintas rentable y fácil de administrar. Se diseñó para clientes, en concreto para aquellos que pertenecen a los servicios financieros, sanidad, medios y entretenimiento y sector público, que retienen los conjuntos de datos durante un periodo de 7 a 10 años o más a fin de cumplir con las necesidades de los clientes y con los requisitos de conformidad normativa. S3 Glacier Deep Archive está diseñado para brindar una durabilidad de los datos del 99,999999999 % (11 nueves) y una disponibilidad del 99,99 % mediante el almacenamiento redundante de los datos en varias zonas de disponibilidad de AWS separadas físicamente en un año determinado.

![S3 Glacier Deep Archive](/contenido/Dominio-3/s3-glacier-4.png "S3 Glacier Deep Archive")

### AWS Snowball

La [familia AWS Snow](https://aws.amazon.com/snow) es un conjunto de dispositivos físicos que ayudan a transportar físicamente hasta exabytes de datos dentro y fuera de AWS. 

La familia AWS Snow está compuesta por **AWS Snowcone**, **AWS Snowball** y **AWS Snowmobile**.

![Familia AWS Snow](/contenido/Dominio-3/aws-snowball-1.png "Familia AWS Snow")

#### AWS Snowcone

AWS Snowcone es un dispositivo pequeño, resistente y seguro que ofrece computación de periferia y almacenamiento y transferencia de datos en cualquier momento y lugar en entornos austeros con conectividad escasa o nula.

Cuenta con 2 CPU, 4 GB de memoria y 8 TB de almacenamiento utilizable.

##### Casos de uso

###### Acelere el análisis y recopilación de datos de flotas
Recopile a diario terabytes de datos de grandes flotas de vehículos con facilidad en un tamaño pequeño mediante un diseño resistente, opciones de alimentación y una seguridad mejorada.

###### Recopile datos de IoT en condiciones extremas

Implemente una solución de almacenamiento e informática de periferia para entornos con espacio limitado, ancho de banda y condiciones medioambientales adversas, como plantas de producción, minas y campos petroleros.

###### Mejore los resultados de los pacientes

Preste servicios superiores de atención a los pacientes en tránsito o sobre el terreno y transmita datos fundamentales en tiempo real con implementaciones integradas de Wi-Fi y AWS DataSync.

###### Agilice la distribución de contenido

Recopile y procese contenido, incluidas imágenes de alta resolución, y mejore el rendimiento del equipo en entornos con ritmos acelerados y espacio reducido.

#### AWS Snowball

AWS Snowball ofrece dos tipos de dispositivos:

- Los dispositivos optimizados para almacenamiento de Snowball Edge son adecuados para migraciones de datos a gran escala y flujos de trabajo de transferencias recurrentes, además del cómputo local con mayores necesidades de capacidad. 
    - Almacenamiento: 80 TB de capacidad de disco duro (HDD) para volúmenes de bloques y almacenamiento de objetos compatible con Amazon S3, y 1 TB de unidad de estado sólido (SSD) SATA para volúmenes de bloques. 
    - Cómputo: 40 vCPU y 80 GiB de memoria para admitir instancias sbe1 de Amazon EC2 (equivalente a C5).
- Snowball Edge Compute Optimized proporciona potentes recursos de cómputo para casos de uso como aprendizaje automático, análisis de video de movimiento completo, análisis y pilas de cómputo locales. 
    - Almacenamiento: capacidad de disco duro utilizable de 42 TB para almacenamiento de objetos compatible con Amazon S3 o volúmenes de bloques compatibles con Amazon EBS y 7.68 TB de capacidad SSD NVMe utilizable para volúmenes de bloques compatibles con Amazon EBS. 
    - Cómputo: 52 vCPU, 208 GiB de memoria y una GPU NVIDIA Tesla V100 opcional. Los dispositivos ejecutan instancias sbe-c y sbe-g de Amazon EC2, que son equivalentes a las instancias C5, M5a, G3 y P3.

##### Casos de uso

###### Migre datos a escala de petabytes

Transfiera bases de datos, copias de seguridad, archivos, registros sanitarios, conjuntos de datos de análisis, contenido multimedia y datos de sensores con IoT, especialmente cuando las condiciones de la red son limitadas.

###### Procese y analice datos de forma local

Ejecute las imágenes de máquina de Amazon (AMI) en Amazon EC2 e implemente código de AWS Lambda en dispositivos Snowball Edge con machine learning (ML) u otras aplicaciones.

###### Optimice los datos de fabricación

Recopile y analice datos de plantas de producción locales para perfeccionar los procesos y mejorar la seguridad, la eficiencia y la productividad.

#### AWS Snowmobile

AWS Snowmobile es un servicio de transferencia de datos a escala de exabytes que se utiliza para trasladar grandes cantidades de datos a AWS.

Puede transferir hasta 100 petabytes de datos por Snowmobile, un contenedor de transporte resistente de 13.7 metros de largo, arrastrado por un camión semirremolque.

AWS Snowmobile mueve cantidades sumamente grandes de datos a AWS. Puede transferir hasta 100 PB por Snowmobile, un contenedor de envío reforzado de 13,71 metros de longitud, colocado en un camión semitráiler.

![Familia AWS Snow](/contenido/Dominio-3/aws-snowball-2.png "Familia AWS Snow")

##### Casos de uso

###### Migre volúmenes masivos de datos

Traslade volúmenes masivos de datos a la nube, incluidas bibliotecas de videos, repositorios de imágenes e inclusive un centro de datos completo.

###### Personalice las operaciones de transferencia de datos a su ubicación

Cada lugar físico es diferente. AWS adapta los requisitos de entrega y migración para cumplir con las necesidades de su sitio.
 
###### Cumpla con los requisitos de seguridad para migrar datos

Mantenga la seguridad de sus datos transferidos físicamente con videovigilancia las 24 horas del día, hardware a prueba de manipulaciones, seguimiento por GPS, cifrado de datos y personal de seguridad opcional.

### Amazon Elastic File System (Amazon EFS)

En el almacenamiento de archivos, varios clientes (como usuarios, aplicaciones, servidores, etc.) pueden acceder a los datos almacenados en carpetas de archivos compartidas. En este enfoque, un servidor de almacenamiento utiliza el almacenamiento de bloques con un sistema de archivos local para organizar los archivos. Los clientes acceden a los datos mediante rutas de archivos.

En comparación con el almacenamiento de bloques y el almacenamiento de objetos, el almacenamiento de archivos es ideal para casos de uso en los que un gran número de servicios y recursos necesitan acceder a los mismos datos al mismo tiempo.

[Amazon Elastic File System (Amazon EFS)](https://aws.amazon.com/efs/) es un sistema de archivos escalable que se utiliza con los servicios de AWS Cloud y los recursos en las instalaciones locales. A medida que agrega y elimina archivos, Amazon EFS crece y se reduce automáticamente. Puede escalar a petabytes según la demanda sin interrumpir las aplicaciones.

#### Comparación de Amazon EBS y Amazon EFS

Un volumen de Amazon EBS almacena los datos en una única zona de disponibilidad. 

Para adjuntar una instancia de Amazon EC2 a un volumen de EBS, tanto la instancia de Amazon EC2 como el volumen de EBS deben residir en la misma zona de disponibilidad.

Amazon EFS es un servicio regional. Almacena datos en varias zonas de disponibilidad y entre ellas. 

El almacenamiento duplicado le permite acceder a los datos simultáneamente desde todas las zonas de disponibilidad de la región en la que se ubica un sistema de archivos. Además, los servidores en las instalaciones locales pueden acceder a Amazon EFS mediante AWS Direct Connect.


### AWS Storage Gateway

AWS Storage Gateway es un conjunto de servicios de almacenamiento en la nube híbrida que brinda acceso en las instalaciones a un almacenamiento en la nube prácticamente ilimitado.

#### Casos de uso

##### Tienda de flujos de trabajo en la nube híbrida

Archiva los datos como objetos utilizando datos generados por aplicaciones locales para que los procesen los servicios de AWS, como el aprendizaje automático o el análisis de macrodatos.

##### Migre los datos de las aplicaciones a EBS

Utilice una instantánea de sus volúmenes locales para recrear los datos en EBS y utilizarlos con aplicaciones basadas en Amazon EC2.

##### Realice copia de seguridad de datos en la nube

Proporcione una copia de seguridad basada en la nube para los archivos y las aplicaciones de bases de datos locales, con un costo bajo y una escala prácticamente ilimitada.