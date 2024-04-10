El fichero .env crea variables de entorno, seran utilizadas en docker-compose.
El fichero .env.dev/prod crea variables de entorno que utilizará la aplicacion en application.properties
El fichero start-dev.sh se inicializan mas variables de entorno tanto para el docker-compose como para el .env
*En un entorno de produccion, las env vars que se inicializan en start-dev.sh se crean manualmente en la maquina.

El fichero compose utiliza las env vars de la maquina y del .env para construirlo y define env vars extra en env_file
*Que seran utilizadas en application.properties

Se eligirá el application del entorno correcto gracias a esta linea spring.profiles.active=${ACTIVE_PROFILE:dev}
*Y a los perfiles declarados en el POM
