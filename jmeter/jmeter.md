# SSLの設定

https://stackoverflow.com/questions/11106796/setting-up-jmeter-to-do-https 

```
Three (3) Steps:

1) Open a command line:
openssl  s_client  -connect  hostname:port  -showcerts

Copy the 2nd+ certs to notepad or text file, with the BEGIN / END Markers: Application_CA_Public_Cert.cer

2) Create trust store with Java keytool  keytool -importcert -alias APPLICATION_NAME_CA_PUBLIC_CERT -file Application_CA_Public_Cert.cer -keystore jmeter_truststore.jks -storepass Password01

3) Update Jmeter system.properties file (per notes in Jmeter, all ssl functionality moved to this file)

JMETER_HOME/bin/system.properties {Jmeter version 2.13}

https.default.protocol=TLSv1
javax.net.ssl.trustStore=C:/jmeter/apache-jmeter-2.13/jmeter_truststore.jks
javax.net.ssl.trustStorePassword=Password01
```