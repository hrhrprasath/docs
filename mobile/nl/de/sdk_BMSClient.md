---

copyright:
  years: 2015, 2016
lastupdated: "2016-11-07"

---
{:new_window: target="_blank"}
{:codeblock:.codeblock}

# BMSClient initialisieren
{: #sdk_BMSClient}

`BMSCore` stellt die HTTP-Infrastruktur bereit, die die anderen {{site.data.keyword.Bluemix}} Mobile-Services-Client-SDKs zur Kommunikation mit ihren entsprechenden {{site.data.keyword.Bluemix_notm}}-Services verwenden.


## Eigene Android-Anwendung initialisieren
{: #init-BMSClient-android}

Sie können das `BMSCore`-Paket entweder in Ihr Android Studio-Projekt herunterladen und importieren oder Gradle verwenden.

1. Importieren Sie das Client-SDK durch Hinzufügen der folgenden Anweisung des Typs `import` an den Anfang Ihrer Projektdatei:

  ```
  import com.ibm.mobilefirstplatform.clientsdk.android.core.api.*;
  ```
  {: codeblock}

2. Initialisieren Sie das `BMSCore`-SDK in Ihrer Android-Anwendung, indem Sie den Initialisierungscode in der Methode `onCreate` der Hauptaktivität in Ihrer Android-Anwendung oder an einer Position hinzufügen, die für Ihr Projekt am geeignetsten ist.

	```Java
	BMSClient.getInstance().initialize(getApplicationContext(), BMSClient.REGION_US_SOUTH); // Make sure that you point to your region
	```
	{: codeblock}

  Sie müssen `BMSClient` mit dem Parameter **bluemixRegion** initialisieren. Im Initialisierungsoperator gibt der Wert **bluemixRegion** an, welche {{site.data.keyword.Bluemix_notm}}-Bereitstellung Sie verwenden, z. B. `BMSClient.REGION_US_SOUTH`, `BMSClient.REGION_UK` oder `BMSClient.REGION_SYDNEY`.


## Eigene iOS-Anwendung initialisieren
{: #init-BMSClient-ios}

Sie können mithilfe von [CocoaPods](https://cocoapods.org){: new_window} oder [Carthage](https://github.com/Carthage/Carthage){: new_window} das `BMSCore`-Paket abrufen.

1. Fügen Sie zur Installation von `BMSCore` mithilfe von CocoaPods die folgenden Zeilen zu Ihrer Podfile hinzu. Wenn Ihr Projekt noch keine Podfile aufweist, verwenden Sie den Befehl `pod init`.

  ```Swift
  use_frameworks!

  target 'MyApp' do
    pod 'BMSCore'
  end
  ```
  {: codeblock}

  Führen Sie anschließend den Befehl `pod install` aus und öffnen Sie die generierte Datei des Typs `.xcworkspace`. Zur Aktualisierung auf ein neueres Release von `BMSCore` müssen Sie den Befehl `pod update BMSCore` verwenden.

  Weitere Informationen zur Verwendung von CocoaPods finden Sie in den [Leitfäden zu CocoaPods](https://guides.cocoapods.org/using/index.html){: new_window}.

2. Befolgen Sie zur Installation von `BMSCore` mit Carthage diese [Anweisungen](https://github.com/Carthage/Carthage#getting-started){: new_window}.

  1. Fügen Sie die folgende Zeile zu Ihrer Cartfile hinzu:

      ```
      github "ibm-bluemix-mobile-services/bms-clientsdk-swift-core"
      ```
      {: codeblock}

  2. Führen Sie den Befehl `carthage update` aus.

  3. Nach der Fertigstellung des Builds fügen Sie `BMSCore.framework` zu Ihrem Projekt hinzu; führen Sie hierfür [Schritt 3](https://github.com/Carthage/Carthage#getting-started) in den Carthage-Anweisungen durch.

  Verwenden Sie für Anwendungen, die mit Swift 2.3 aufgebaut sind, den Befehl `carthage update --toolchain com.apple.dt.toolchain.Swift_2_3`. Verwenden Sie andernfalls den Befehl `carthage update`.

3. Importieren Sie das Modul.

  ```Swift
  import BMSCore
  ```
  {: codeblock}

4. Initialisieren Sie mithilfe des folgenden Codes die Klasse `BMSClient`.

  Platzieren Sie den Initialisierungscode in der Methode `application(_:didFinishLaunchingWithOptions:)` Ihres Anwendungsbeauftragten oder an einer Position, die für Ihr Projekt am geeignetsten ist.

    ```Swift
    BMSClient.sharedInstance.initialize(bluemixRegion: BMSClient.Region.usSouth) // Make sure that you point to your region
    ```
   {: codeblock}

    Für die Verwendung des {{site.data.keyword.mobileanalytics_short}}-Client-SDK müssen Sie `BMSClient` mit dem Parameter **bluemixRegion** initialisieren. Im Initialisierungsoperator gibt der Wert **bluemixRegion** an, welche {{site.data.keyword.Bluemix_notm}}-Bereitstellung Sie verwenden, z. B. `BMSClient.Region.usSouth`, `BMSClient.Region.unitedKingdom` oder `BMSClient.Region.sydney`.
