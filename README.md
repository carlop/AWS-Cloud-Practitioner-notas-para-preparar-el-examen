# AWS Cloud Practitioner - Notas para preparar el examen

![AWS Certified Cloud Practitioner badge](AWS-Certified-Cloud-Practitioner_badge.png "AWS Certified Cloud Practitioner badge")

El propósito de este repositorio es contener toda la información necesaria para preparar y aprobar fácilmente el examen para obtener la certificación AWS Cloud Practitioner.


## Tabla de Contenido

- [Contenido del examen](/contenido/Contenido-del-examen.md)

- [Dominio 1: Conceptos de la nube](/contenido/Dominio-1/Dominio1-Conceptos-de-la-nube.md)
    - Definir la nube de AWS y su propuesta de valor
        - Definir los beneficios de la nube de AWS, incluidos los siguientes:
            - Seguridad
            - Fiabilidad
            - Alta disponibilidad
            - Elasticidad
            - Agilidad
            - Precios de pago por uso
            - Escalabilidad
            - Alcance global
            - Economía de escala
        - Explicar cómo la nube de AWS permite que los usuarios se enfoquen en el valor de negocio
            - Transición de recursos técnicos a actividades que generan ingresos en lugar de administrar la infraestructura
    - Identificar aspectos de la economía de la nube de AWS
        - Definir elementos que formarían parte de una propuesta de Costo total de propiedad
            - Comprender el rol de los gastos operativos (OpEx)
            - Comprender el rol de la inversión de capital (CapEx)
            - Comprender el costo de mano de obra asociado a las operaciones en las instalaciones
            - Comprender el impacto del costo de las licencias de software cuando se migra a la nube
        - Identificar qué operaciones reducirán los costos cuando se migra a la nube
            - Infraestructura del tamaño indicado
            - Beneficios de la automatización
            - Reducción del alcance de la conformidad (por ejemplo, informes)
            - Servicios administrados (por ejemplo, RDS, ECS, EKS, DynamoDB)
    - Explicar los diferentes principios de diseño de la arquitectura de nube
        - Explicar los principios de diseño
            - Crear un diseño preparado para los errores
            - Desacoplar componentes en comparación con la arquitectura monolítica
            - Implementar elasticidad en la nube o en las instalaciones
            - Pensar en paralelo


- [Dominio 2: Seguridad y conformidad](/contenido/Dominio-2/Dominio2-Seguridad-y-Conformidad.md)
    - Describir el modelo de responsabilidad compartida de AWS
        - Reconocer los elementos del modelo de responsabilidad compartida
        - Describir la responsabilidad del cliente en AWS
            - Describir cómo las responsabilidades del cliente pueden cambiar en función del servicio que se usa (por ejemplo, con RDS, Lambda o EC2)
        - Describir las responsabilidades de AWS
    - Definir los conceptos de seguridad y conformidad de la nube de AWS
        - Identificar dónde encontrar información sobre la conformidad de AWS
            - Ubicar las listas de controles de conformidad reconocidos disponibles (por ejemplo, HIPPA, SOC)
            - Reconocer que los requisitos de conformidad varían entre los servicios de AWS
        - Describir cómo los clientes logran la conformidad en AWS en un nivel alto
            - Identificar las diferentes opciones de cifrado en AWS (por ejemplo, en tránsito, en reposo)
        - Describir quién habilita el cifrado de un servicio determinado en AWS
        - Reconocer que existen servicios que ayudan a auditar e informar
            - Reconocer que existen registros para auditar y monitorear (no es necesario comprender los registros)
            - Definir Amazon CloudWatch, AWS Config y AWS CloudTrail
        - Explicar el concepto de acceso con privilegios mínimos
    - Identificar las capacidades de administración de acceso a AWS
        - Comprensión del propósito de la administración de usuarios e identidades
            - Políticas de claves de acceso y contraseñas (rotación, complejidad)
            - Multi-Factor Authentication (MFA)
            - AWS Identity and Access Management (IAM)
                - Grupos y usuarios
                - Roles
                - Políticas, políticas administradas en comparación con políticas personalizadas
            - Tareas que requieren el uso de cuentas raíz. Protección de cuentas raíz
    - Identificar recursos para respaldar la seguridad
        -  Reconocer que existen diferentes capacidades de seguridad de red
            - Servicios nativos de AWS (por ejemplo, grupos de seguridad, ACL de red, AWS WAF)
            - Productos de seguridad de terceros en AWS Marketplace
        - Reconocer que hay documentación y dónde encontrarla (por ejemplo, prácticas recomendadas, documentos técnicos, documentos oficiales)
            - Centro de conocimientos de AWS, centro de seguridad, foro de seguridad y blogs de seguridad
            - Integradores de sistemas de socios
        - Saber que las verificaciones de seguridad son un componente de AWS Trusted Advisor


- [Dominio 3: Tecnología](/contenido/Dominio-3/Dominio3-Tecnología.md)
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
        - [Servicios de almacenamiento de AWS](/contenido/Dominio-3/Dominio3-Tecnología.md#servicios-de-almacenamiento-de-aws)
            - [Almacenamiento de objetos](/contenido/Dominio-3/Dominio3-Tecnología.md#almacenamiento-de-objetos)
            - [Amazon S3](/contenido/Dominio-3/Dominio3-Tecnología.md#amazon-s3)
            - [Almacenes de instancias](/contenido/Dominio-3/Dominio3-Tecnología.md#almacenes-de-instancias)
            - [Amazon Elastic Block Store (Amazon EBS)](/contenido/Dominio-3/Dominio3-Tecnología.md#amazon-elastic-block-store-amazon-ebs)
            - Describir Amazon S3 Glacier
            - Describir AWS Snowball
            - Describir Amazon Elastic File System (Amazon EFS)
            - Describir AWS Storage Gateway
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


- [Dominio 4: Facturación y precios](/contenido/Dominio-4/Dominio4-Facturación-y-precios.md)
    - Comparar y contrastar los distintos modelos de precios de AWS (por ejemplo, precios de instancias bajo demanda, instancias reservadas e instancias de spot)
        - Identificar situaciones o la mejor opción para precios de instancias bajo demanda
        - Identificar situaciones o la mejor opción para precios de instancias reservadas
            - Describir la flexibilidad de las instancias reservadas
            - Describir el comportamiento de las instancias reservadas en AWS Organizations
        - Identificar situaciones o la mejor opción para precios de instancias de spot
    - Reconocer las distintas estructuras de cuentas en relación con la facturación y los precios de AWS
        - Reconocer que la facturación unificada es una característica de AWS Organizations
        - Identificar la forma en que varias cuentas ayudan a asignar costos entre departamentos
    - Identificar los recursos de soporte de facturación disponibles
        - Identificar formas de obtener soporte e información sobre la facturación
            - Cost Explorer, Informe de uso y costo de AWS, Amazon QuickSight, socios externos y herramientas de AWS Marketplace
            - Abrir un caso de soporte de facturación
            - El rol del Concierge para clientes del plan de soporte de AWS Enterprise
        - Identificar dónde encontrar información sobre precios en los servicios de AWS
            - Calculadora de costo mensual de AWS
            - Páginas de productos de servicios de AWS
            - API de precios de AWS
        - Reconocer que existen alarmas y alertas
        - Identificar cómo se usan las etiquetas en la asignación de costos