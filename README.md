# SSGS_labo_docker

Programma  sciluppato come progetto per il corso di SSGS dell'Universita' degli Studi di Genova. 

### Membri:
 - Andrea Valenzano
 - Nicola Incardona

## Introduzione

Come base per l'esercitazione abbiamo scelto il secondo progetto proposto:

 - <a href="https://github.com/novuhq/blog/tree/main/scheduling-app-with-react-nodejs-emailjs">scheduling-app-with-react-nodejs-emailjs</a>

Essendo questo progetto suddiviso in due sottoprogetti (client e server) abbiamo anche noi diviso la 
consegna in due immagini docker separate.

<b>NOTA</b>: per semplificare il lavoro (avendone avuto la possibilita') il progetto e' stato stolto interamente
in <b>pair programming</b>.


## Docker Images
Per creare le immagini abbiamo utilizzato due Dokerfile separati e per evitare problemi 
di *versioning* (aggiornamenti, eliminazioni ecc..) abbiamo clonato localmente dal repo originale la parte di codice
di interesse.

<b>NOTA:</b> all'interno dei Dockerfile abbiamo volutamente omesso di esporre una porta. Questo per non avere di 
default una porta aperta in ogni container creato a partire dall'immagine. La scelta non crea pero' problemi siccome e' possibile imposrtare le porte alla creazione del container.

## Compose
Abbiamo creato inoltre un file docker-compose per avviare direttamente entrambe le immagini e gestirne
tutti i setup (es. il port forwarding). Questo file di configurazione utilizza direttamente le immagini
caricate su DockerHUB ed e' quindi completamentente indipendente dalla parte di building delle immagini.

## Github Workflow
Per lo sviluppo di questa sezione non abbiamo seguito la guida fornita da GitHub stesso bensi la
documentazione ufficiale di Docker, partendo dal loro file di *template* invece che da quello consigliato a lezione.
