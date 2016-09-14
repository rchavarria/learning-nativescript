# [Getting up and running](http://docs.nativescript.org/angular/tutorial/ng-chapter-1)

## 1.1 Instalar dependencias de NativeScript

### Node.js

Esta es fácil. Comprobar que se tiene una versión más o menos actualizada, la 4.x supongo que será suficiente. Tengo instalada la versión 5.x, y en el siguiente paso tengo un error diciendo que NativeScript no soporta esa versión de Node.js. Toca instalar una versión TLS, por ejemplo la 4.5.0.

### Instalar la herramienta de línea de comandos de NativeScript

Instalarla con `npm` (es posible que se necesite `sudo`):

```
npm install -g nativescript
```

Eso debería instalar dos comandos: `tns` y `nativescript`. Ambos son equivalentes, así que nos quedamos con `tns` que es más cortico.

### Instalar requisitos iOS o Android

iOS no me interesa.

Para Android hay scripts que te facilitan la vida, pero son para Windows y Mac, nada para Linux.

### Verificar el sistema

Con el comando:

```
tns doctor
```

NativeScript nos dirá si encuentra algún problema con al configuración de nuestro sistema. Ya que el paso anterior no está documentado para Linux, probaré con este comando a ver si detecta algún problema en mi máquina. Parece ser que existe una documentación un poco más detallada de la que encontramos en la página de NativeScript. Esta documentación es [Requisitos sobre Linux](https://github.com/NativeScript/nativescript-cli#linux).

Empezamos mal. `tns doctor` me dice que mi instalación de Java no está bien. Necesito tener instalada Java 8, y tener la variable `JAVA_HOME` bien configurada. Corrijo la variable de entorno, pero resulta que necesito el Java Development Kit (o JDK), con lo que toca instalarlo via `apt-get`:

```
sudo apt-get install openjdk-8-jdk-headles
```

Una vez echo esto... `tns doctor` dice que OK. Supongo que dice eso porque tengo instalado el [Android SDK]() correctamente y con una versión soportada. Recuerda: [Requisitos sobre Linux](https://github.com/NativeScript/nativescript-cli#linux).




