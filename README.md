
Use:

Cliccando FAQ hai l'elenco delle domande più frequenti. Basta poi digitare il numero corrisponende alla domanda per la risposta corrispondente. Infine puoi fare una ricerca per parola chiave anteponendo il carattere ? tipo ?Ferie.
Disabilitato: Invia la tua posizione o digita la città per avere la sede più vicina. 

Lic. MIT @piersoft


Config:
In localhost is possible to launch
php start.php 'sethook' per impostare start.php come webhook (inserire https il link per start.php)
php start.php 'removehook' per rimuovere start.php come webhook
php start.php 'getupdates' per eseguire manualmente getupdates.php (se non hai https puoi settare un crontab ogni minuto che esegue questa istruzione)


Devi compilare un file sheet su GoogleDrive e compilare il file settings_t.php.

1) cerca su Telegram l'utente botfather e fai /newbot per creare un nuovo bot. scelto il nome ti verrà indicata l'API key riservata da inserire in settings_t.php
2) apri questo file e fai "crea una copia" https://goo.gl/oaSmdh ogni documento gdrive ha una propria key che è quel codice lungo nell'url tra https://docs.google.com/spreadsheets/d/ e edit#gid=. Incollare questa key nel file settings.php nel campo GDRIVEKEY 
3) compila il primo foglio di calcolo che ho chiamato faq. segnati il valore numerico che hai dopo gid= nell'url e inseriscilo in settings_t.php come GDRIVEGID1
4) compila il secondo foglio di calcolo che ho chiamato risposte. segnati il valore numerico che hai dopo gid= nell'url e inseriscilo in settings_t.php come GDRIVEGID2. Gli ID delle risposte devono corrispondere alla relativa domanda nel foglio faq
5) compila il terzo foglio di calcolo che ho chiamato sedi. segnati il valore numerico che hai dopo gid= nell'url e inseriscilo in settings_t.php come GDRIVEGID3. le coordinate devi incollarle anteponendo il carattere ' esempio '40.123456 cosi "avvisi" google che è un campo testo
6) logo.png aggiorna il logo della tua azienda/sindacato

In sintesi crei un bot da botfather, compili foglio google con domande risposte e faq, compili il file settings_t.php e poi o lanci manualmente php start.php 'getupdates' (o tramite crontab) oppure attivi https e inserisci il link del file start.php nel file settings_t.php (esempio https://www.nomesito/tuobot/start.php)




Buona fortuna
