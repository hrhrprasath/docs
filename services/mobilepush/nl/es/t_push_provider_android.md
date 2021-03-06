
---

copyright:
years: 2015, 2016

---

{:new_window: target="_blank"}
# Configuración de credenciales para FCM
{: #create-push-enable-gcm}
Última actualización: 15 de noviembre de 2016
{: .last-updated}

Firebase Cloud Messaging (FCM) es la pasarela utilizada para entregar notificaciones push a dispositivos Android y a los navegadores Google Chrome y Mozilla. FCM ha sustituido a Google Cloud Messaging (GCM). Necesita obtener las credenciales de FCM y, a continuación, configurar el servicio {{site.data.keyword.mobilepushshort}} en el panel de control. Asegúrese de que utiliza las configuraciones de FCM para nuevas aplicaciones. Las aplicaciones existentes seguirán funcionando con las configuraciones de GCM.

##Cómo obtener el ID de remitente y la clave de la API
{: #android-senderid-apikey}

La clave de la API se almacena de forma segura y la utiliza el servicio {{site.data.keyword.mobilepushshort}} para conectarse al servidor de FCM y el ID de remitente (número de proyecto) lo utilizará el SDK de Android y el SDK de JS para Google Chrome y Mozilla Firefox en el lado de cliente. 

Para configurar el FCM, genere la clave de API y el ID de remitente y siga estos pasos:

1. Visite la [Consola de Firebase](https://console.firebase.google.com/?pli=1).
2. Seleccione **Crear nuevo proyecto**. 
3. En la ventana Crear un proyecto, proporcione un nombre de proyecto, elija un país/región y pulse **Crear proyecto**.
3. En el panel de navegación, pulse el icono Valores y seleccione **Valores del proyecto**.
4. Seleccione el separador Cloud Messaging para generar una Clave de API de servidor y un ID de remitente.

##Configuración del servicio {{site.data.keyword.mobilepushshort}} para Android y las aplicaciones y extensiones de Chrome
{: #setup-push-android}

**Nota:** Necesitará la Clave de la API de FCM/GCM y el ID del remitente (número de proyecto).

1. Abra el panel de control de Bluemix y pulse la instancia del servicio {{site.data.keyword.mobilepushfull}} que ha creado para abrir su panel de control. Se mostrará el panel de control de Push. Para configurar un servicio {{site.data.keyword.mobilepushshort}} desenlazado para Android, seleccione el icono de Servicio {{site.data.keyword.mobilepushshort}} desenlazado para abrir el panel de control del servicio {{site.data.keyword.mobilepushshort}}. 

![Panel de control de Push](images/push_unbound.jpg)

2. Pulse el botón **Configurar Push** para configurar las credenciales de FCM/GCM para aplicaciones de Android y aplicaciones y extensiones de Google Chrome.
3. En la página **Configuración**, para Android, vaya al separador **Mobile** y configure el ID del remitente (número de proyecto de GCM) y la Clave de la API. Para las aplicaciones y extensiones de Google Chrome, vaya al separador **Web** y configure el ID del remitente (número de proyecto de FCM/GCM) y la Clave de la API adecuadamente.
4. Pulse **Guardar**.
5. Pasos siguientes. [Habilitación de notificaciones para Android](c_enable_push.html) o [Habilitación de notificaciones para aplicaciones y extensiones de Google Chrome](c_enable_push.html).

###Configuración para push web de Google Chrome y Mozilla Firefox (utilizando FCM/GCM)
{: #config-gcm-mozilla}

1. En el panel de navegación del Panel de control de Push, seleccione **Configurar**.
2. Seleccione el separador Web.
	![Configuraciones de push web](images/webpush_configure.jpg)
3. Configure la clave de la API de FCM/GCM y el URL del sitio web que se registrará para la recepción de notificaciones por push.
4. Pulse **Guardar**.
5. Pasos siguientes. [Habilitación de notificaciones para navegadores Google Chrome y Mozilla Firefox](c_enable_push.html).
