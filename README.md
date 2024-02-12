# mailerDSN
How to generate your MAILER_DSN for .env.local  

include script to dev-tools-console  
change var in script  
copy & paste to .env.local  

```function erzeugeMailerDSN(benutzername, passwort, server, port, encryption) {
  var mailerDSN = `MAILER_DSN=smtp://${encodeURIComponent(benutzername)}:${encodeURIComponent(passwort)}@${server}:${port}?encryption=${encryption}`;
  
  return mailerDSN;
}

// Passe die Variablen an
var benutzername = 'meinBenutzername';
var passwort = 'meinPasswort';
var server = 'smtp.example.com';
var port = '465';
var encryption = 'ssl';

// Rufe die Funktion auf und gebe das Ergebnis in der Konsole aus
console.log(erzeugeMailerDSN(benutzername, passwort, server, port, encryption));```

