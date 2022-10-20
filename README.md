### Servicios utilizados en esta actividad práctica

*   Amazon S3
*   Amazon Glue
*   Amazon Athena
*   Amazon QuickSight

### Etapas para el desarrollo

### Crear bucket en Amazon S3

*   Consola de Amazon S3 -> buckets -> Create bucket -> Nombre del bucket \[bucket nome_do] - Crear bucket
*   Crear carpeta `/output` y otro con el nombre del conjunto de datos. Este nombre definirá el nombre de la tabla creada en Glue)
*   Cargue los archivos de datos ubicados en la carpeta `/data`

#### Crear Glue Crawler

*   Consola de Amazon Glue -> rastreadores -> Agregar rastreador
*   Tipo de origen -> Rastrear todas las carpetas
*   Almacén de datos \[S3] -> Incluir ruta de acceso
*   Crear rol de IAM
*   Frecuencia \[Ejecutar bajo demanda]
*   Nombre de la base de datos \[seu_nome_de_db]
*   Comportamiento del grupo \[Crear un único esquema para cada ruta de acceso de S3]
*   Terminar
*   Bases de datos -> Tablas -> Ver datos de tablas creadas

### Creación de aplicaciones en Amazon Athena

*   Editor de consultas -> Configuración -> Administrar configuración -> Ubicación y cifrado de resultados de consulta -> Examinar S3 -> seleccionar el bucket creado
*   Seleccione Base de datos -> crear consultas (ejemplos en la carpeta `/src`)
*   Comprobar las consultas no guardadas en el bucket creado en S3
*   Salavar queries -> Run again -> comprobar el bucket creado en S3

#### Creación de una nueva tabla

*   Generar tabla DDL
*   Copiar la consulta generada
*   Seleccione la base de datos y cree la nueva tabla en una nueva consulta

### Ver datos en Amazon QuickSight

*   Regístrese (si no tiene una cuenta) -> Elija \[Estándar]
*   Datasets -> Crear nuevo dataset -> Athena -> > Nombre
*   Seleccione la base de datos -> seleccione la tabla -> Editar o previsualizar -> Guardar y ver
*   Cree visualizaciones seleccionando columnas, creando filtros y parámetros, y seleccionando tipos visuales para gráficos.

### Eliminar recursos

*   Decantar los elementos creados
