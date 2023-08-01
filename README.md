# Twitch en català

La traducció no oficial al català de l'aplicació de Twitch. Disponible per a telèfons Android. Pots instal·lar el fitxer APK ja modificat, o crear-lo tu mateix seguint els pasos que expliquem a continuació.

Visita el web https://directes.app/


## Instal·lació

1. Esborra l'aplicació de Twitch en cas que la tinguis.
2. Baixa el fitxer APK. Visita el web https://directes.app/
3. Obre el fitxer APK. Pot demanar permís d'instal·lació per no ser una aplicació de la botiga.

ADVERTÈNCIES
Cal esborrar l'aplicació original de twitch. Cal tindre configurat el dispositiu en català.  
Al tractar-se d'una aplicació modificada, el sistema pot mostrar advertències de seguretat.  
Les compres a través de Play Store poden fallar. Podràs fer la mateixa compra a través de la web de Twitch.


## Creació

1. Baixa els programes necessaris al teu ordinador: Apktool, zipalign, keystore i apksigner.
2. En aquest repositori trobaràs una carpeta per cada versió modificada. Per la última versió baixa tots els fitxers XML en català.
Necessitaras també el paquet APK original de Twitch, de la mateixa versió. Assegura't que descarregues la variant que NO és BUNDLE. Consulta la taula més avall.
3. Descompila el fitxer APK original amb Apktool: `apktool d fitxer.apk -o descompilat`.
4. Navega a `descompilat/res/values`. Substitueix els fitxers XML pels que t'has baixat en català.
5. Torna a compilar l'aplicació amb Apktool: `apktool b descompilat --use-aapt2` Trobaràs el nou APK a `descompilat/dist`
6. Alinea el fitxer APK amb zipalign: `zipalign -f -v 4 descompilat/dist/fitxer.apk twitchcatala.apk`.
7. Signa el fitxer APK amb apksigner: `apksigner sign --ks clau.keystore --ks-key-alias clau twitchcatala.apk`
Pots generar una clau keystore fent: `keytool -genkey -v -keystore clau.keystore -alias clau -keyalg RSA -keysize 2048 -validity 10000`

| Versió   | Enllaç   |
| -------- | -------- |
| 15.7.0   | https://www.apkmirror.com/apk/twitch-interactive-inc/twitch/twitch-15-7-0-release/ |


## Contribueix a millorar la traducció

Ens basem en una traducció feta amb els serveis de SoftCatalà, que poc a poc anem millorant.
Si vols contribuir, pots editar els fitxers que es troben a la carpeta `contribueix` i demanar els canvis.