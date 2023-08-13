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
        - Amazon Elastic Block Store (Amazon EBS)
        - Amazon S3 Glacier
        - AWS Snowball
        - Amazon Elastic File System (Amazon EFS)
        - AWS Storage Gateway
    - Identificar los servicios de redes de AWS
        - Identificar VPC
        - Identificar grupos de seguridad
        - Identificar el fin de Amazon Route 53
        - Identificar VPN, AWS Direct Connect
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



## Servicios de almacenamiento de AWS

### Almacenamiento de objetos

![Almacenamiento de objetos](/contenido/Dominio-1/almacenamiento-de-objetos.png "Almacenamiento de objetos")

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


### Amazon Elastic Block Store (Amazon EBS)
### Amazon S3 Glacier
### AWS Snowball
### Amazon Elastic File System (Amazon EFS)
### AWS Storage Gateway