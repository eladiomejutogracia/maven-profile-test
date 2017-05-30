# maven-profile-test
Ejecución de tests unitarios, de integración y aceptación con cucumber en maven a través de perfiles y properties.

En funcion del perfil a ejecutar:

mvn surefire:test -Punit-test
mvn failsafe:integration-test -Pintegration-test
mvn failsafe:integration-test -Pacceptance-test

o bien:

mvn clean install -Punit-test
mvn clean install -Pintegration-test
mvn clean install -Pacceptance-test

En ambos casos esta controlada la ejecución de tests. Nunca se van a ejecutar los test unitarios si se indica otro perfil.