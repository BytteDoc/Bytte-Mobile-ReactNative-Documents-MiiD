![Directories](http://www.bytte.com.co/ftpaccess/Varios/CarlosG/Documentaci%C3%B3n/LogoBytte.png)

# Bytte S.A.S
# Documento Integración React Native
### CONFIDENCIALIDAD

La información contenida en el presente documento es **CONFIDENCIAL**, hace parte del secreto comercial e industrial de la empresa e implica transmisión de información cuya propiedad corresponde exclusivamente a BYTTE SAS. En consecuencia, la divulgación o el uso inapropiado de la información aquí contenida por parte del receptor de la misma, implicarán la aplicación de las normas legales pertinentes para su debida protección.

### 1. INTRODUCCIÓN

#### Propósito General del Documento

El presente documento tiene como finalidad dar a conocer el paso a paso de la instalación del SDK provisto por Bytte en una aplicación hibrida generada en React Native.

#### 1.1. Objetivo

El presente documento tiene como objetivo explicar basado en un ejemplo, cómo realizar la integración del SDK Bytte a una aplicación React Native.

#### 1.2. Factores Limitantes

Los factores limitantes para la integración del SDK son:
* El Plugin SDK Bytte, está disponible para plataformas IOS y Android.
* Se recomiendan cámaras con resolución mayores o iguales a 8 Mega Pixeles para un óptimo rendimiento.
* Se debe verificar la calidad de la cámara, es recomendable utilizar dispositivos con cámara que tengan la característica de “Auto Foco” habilitada.
* El SDK no funciona sobre dispositivos virtuales, únicamente sobre dispositivos físicos IPhone y Android.

### 2. INSTALACIÓN

#### 2.1. Pre requisitos

* General:
    > * NPM (sistema de gestión de paquetes)

* Para la compilación de aplicación en plataforma IOS, se requiere:
    > * XCode 15 o Superior con SDK IOS 13 o superior.

#### 2.2. Instalación Plugin react-native-bytte-document

#### 2.2.1 Configuración Token

#### 2.2.1.1 MAC

Una vez instalado NPM (sistema de gestión de paquetes). En la ruta por defecto de instalación se debe encontrar el archivo .npmrc, si no se encuentra se debe crear a nivel de usuario.

Una vez detectado el archivo se debe configurar de la siguiente manera.


``` txt
registry=https://byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/registry/ 
                        
always-auth=true 
                        
; begin auth token
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/registry/:username=BytteTFS
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/registry/:_password=(TOKEN)
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/registry/:email=npm requires email to be set but doesn't use the value
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/:username=BytteTFS
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/:_password=(TOKEN)
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/:email=npm requires email to be set but doesn't use the value
; end auth token
```

En el espacio (*TOKEN*) se debe ingresar el password enviado por Bytte sas.

#### 2.2.1.2 WINDOWS

Una vez instalado NPM (sistema de gestión de paquetes). Se debe ejecutar el siguiente comando en la terminal.

``` vsts-npm-auth -config .npmrc```

este comando creará un archivo .npmrc en la ruta por defecto C:\Users\USER\\.npmrc

Una vez detectado el archivo se debe configurar de la siguiente manera.

``` txt
registry=https://byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/registry/ 
                        
always-auth=true

; begin auth token
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/registry/:username=BytteTFS
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/registry/:_password=(TOKEN)
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/registry/:email=npm requires email to be set but doesn't use the value
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/:username=BytteTFS
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/:_password=(TOKEN)
//byttetfs.pkgs.visualstudio.com/c1dcbe70-4508-4f44-bfa8-e50bdbfea41f/_packaging/react-native-bytte-document/npm/:email=npm requires email to be set but doesn't use the value
; end auth token
```

En el espacio (*TOKEN*) se debe ingresar el password enviado por Bytte sas.

#### 2.2.2 Instalación 

`$ npm install react-native-bytte-document`


Una vez instalado el plugin, se debe realizar la consulta a la aplicación para verificar que este quedó correctamente instalado.

#### 2.3. Configuración nativo iOS (XCode)

Luego de instalar las dependencias npm se ingresa a la carpeta ***ios*** y se ejecuta el comando `pod install`

    $ cd ios
    $ pod install

######   Permisos
Los permisos en runtime deben ser solicitados por la app para el uso de bytte es necesario el siguiente:
configurar en el archivo Info.plist para el uso de la ***Cámara***

`Privacy - Camera Usage Description`

####  2.4. Configuración  Android
## Android


* **Se debe verificar la calidad de la cámara, es recomendable utilizar dispositivos con cámara que tengan la característica de “Auto Foco” habilitada**
* **Se recomiendan cámaras con resolución mayores o iguales a 5 Mega Pixeles para un óptimo rendimiento**
* **El SDK no funciona sobre dispositivos virtuales, únicamente sobre dispositivos físicos IPhone y**
* **Sistemas soportados Android 5.0 o superior gradle 4.1.2 o superior arquitecturas x86,64 bits**


### Para compilación de aplicación en plataforma Android, se requiere:
* **Java JDK Versión 1.8, 11, 17
* **Android SDK** 
* **Funciona con Android 24 o superior**

## Los permisos en runtime deben ser solicitados por la app
para el uso de bytte es necesario los siguientes:
uso de ***Camara y almacenamiento***

`<uses-permission android:name="android.permission.CAMERA" />`

`<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>`

######   Adicionar la implementación bytte a su proyecto 

``` npm i react-native-rn-bytte-bio-lib-miid --save```

Luego vamos a android en la app, para la configuración en el archivo 
`build.gradle` del proyecto

`android/build.gradle`:

##### en la etiqueta 
   ``` 
allprojects {
    repositories {
      maven {
            url ''
            name ''
        credentials {
            username ""
            password ""
        }
    }
    }
}

   ``` 

Solicitar a **Bytte lo siguiente:**   ingresarlo dentro de los "" 
- **url**
- **name**
- **username**
- **password**


Tener en cuenta que debe estar habilitado multidex para android revisar la documentación para generarlo en react-native
' multiDexEnabled true'
Las librerías bytte soportan las arquitecturas a 32 y 64 bits necesarias para Android
 ndk{
             abiFilters  "armeabi-v7a", 'arm64-v8a'
        }
        


#### 2.5. Uso de la librería

Bytte proporcionará los siguientes datos de configuración:

* URL
* ClientID
* ClientKey
* SesionID

El parámetro tipoCaptura determinará el documento que se capturará:
* cc
  * Cédula Colombiana Hologramas
* ccv2
  * Cédula Colombiana Digital
* ccext
  * Cédula Extranjeria
* pasport
  * Pasaporte (Únicamente disponible para **startFrontDocument**)

Una vez instalado el plugin, la aplicación destino heredará el Javascript expuesto por este, el cual expone las siguientes operaciones:

   * startBackDocument
   * startFrontDocument

##### ***startBackDocument***

```javascript
    //Captura documento reverso
    onCaptureBackDocument = () =>{
        NativeModules.BytteDocument.startBackDocument(
        url,
        clientID,
        clientKey,
        sesionId,
        timeOut,
        tipoCaptura,(response)=>{
            var obj = JSON.parse(response);
            if(obj.StatusOperacion){
              //Operacion Exitosa
            } else {
              //Operacion No Exitosa
            } 
        }); 
    }
```

##### ***startFrontDocument***

```javascript
    //Captura documento frente
    onCaptureFrontDocument = () =>{
        NativeModules.BytteDocument.startFrontDocument(
        url,
        clientID,
        clientKey,
        sesionId,
        timeOut,
        tipoCaptura,(response)=>{
            var obj = JSON.parse(response);
            if(obj.StatusOperacion){
              //Operacion Exitosa
            } else {
              //Operacion No Exitosa
            } 
        }); 
    }
```









