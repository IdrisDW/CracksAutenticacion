# Autenticacion para todos
 Equipo “Los Cracks”

Los Cracks queremos facilitar la banca a quienes más lo necesitan. Las propuestas de login que tenemos priorizan la facilidad de implementación para trabajar con lo que ya tenemos a nivel banco y atender lo más rápido posible a nuestros apreciados clientes que utilizan nuestros diferentes canales

Para la parte de identificación haremos modelos de clústering con la transaccionalidad del cliente, probando aproximaciones no supervisadas

Tal y como lo propusieron los anfitriones, nuestro trabajo se divide en dos partes: Un conjunto de propuestas enfocadas al inicio de sesión en las que también aplicaremos métodos de machine learning entrenados con datasets que estamos diseñando

Y otro set de propuestas están enfocadas a inferir si un cliente tiene algún tipo de discapacidad, estamos trabajando con los datos que proporcionaron los anfitriones y otros que creemos que los complementan. Como ya mencionamos, trabajaremos con métodos de machine learning supervisados y no supervisados. Como output daremos una probabilidad de que cada cliente tenga los tipos de discapacidad mencionados

Estamos usando python y sus bibliotecas de machine learning más widely used, métodos de clusterización y estamos complementando con datos de internet para nuestros conjuntos de datos

Como equipo queremos lograr que nuestras propuestas sean factibles y sencillas de implementar, para lograr el cometido
de poner al alcance de todos las oportunidades de esta nueva era , es por eso que realizamos una 
reestructuracion de las interfaces de la app pensando en las necesidades especificas de las personas con 
capacidades distintas y proponiendo mejoras  para estar mas cerca los clientes, asi como
modelos para analizar los datos de los cliente y poder ofrecer soluciones.

Propusimos dos tablas para realizar los modelos que nos permiten reconocer a los clientes que por su tiempo de realizar el logueo a la app o de entrar a un ATM
tienen probabilidades de tener alguna discapacidad o ser adulto mayor:

Tabla:
app_login_detection
Con los campos : 
customer_id
age
seconds_to_successful_login
attempts_password
attempts_fingerprint
attempts_voice
attempts_face
login_type

total_attempts es usado para realizar el modelo, y es la sumatoria de los attempts de logeo de las distintas formas disponibles (password, fingerprint, voice,face)

Tabla
atm_login_detection
Con los campos :
customer_id 
operation_type
count_operation_type
count_nip_attempt
count_op_secs

Al proponer las tablas de esta forma:
Se captura los intentos de cada manera disponible y al lograr entrar se considera un registro.

