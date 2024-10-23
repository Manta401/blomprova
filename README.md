# In questa cartella caricherò guide utili alla didattica

### Link guida ai file markdown (.md) - [ENG](https://www.markdowntutorial.com/) - [ITA](https://www.liberliber.it/progetti/manuzio/collaborare/manuale_markdown_20201226.pdf)
### Link guida ai motori passo passo (step by step) - [ENG](https://howtomechatronics.com/tutorials/arduino/stepper-motors-and-arduino-the-ultimate-guide/?utm_content=cmp-true) - [ITA](https://www.makerslab.it/arduino-ed-i-motori-passo-passo/) - [ITA SLIM](https://www.arduinofacile.it/2019/10/14/il-motore-passo-passo-stepper/) 
### Link regolamento Rescue Maze 2023/2024 - [ENG](https://junior.robocup.org/wp-content/uploads/2023/10/RCJRescueMaze2024RulesDraft.pdf)
### Link video guida ai motori passo passo (step by step) - [ITA](https://youtu.be/QRCvC5xhJCw?si=Br6-mjW-0x72jauN)

---

## Raspberry Pi

### Software per installare il sistema operativo sulla SD Card - [ENG](https://www.raspberrypi.com/software/)
Passi da seguire per installare il sistema operativo sulla SD Card con software Raspberry Pi Imager v. 1.8.1
- Selezionare il modello del vostro Raspberry Pi
- Sistema operativo: Raspberry Pi OS (64 bit)
- Selezionare la scheda SD
- Avanti
- Modifica impostazioni
  * Su nome host scrivere il nome del vostro robot
  * Scegliere un nome utente e password semplici e riportarli anche su un file all'interno della cartella "Altro"
  * Configura WiFi:
      + SSID: Robotica
      + Password: ferraris2023
      + Nazione WiFi: IT
  * Impostare fuso orario e layout tastiera
  * Su "Servizi" abilitare SSH (vi permetterà di accedere al Raspberry Pi da un altro computer)
  * Salva
- Si

### Operazioni preliminari
Durante l'esecuzione di comandi contenenti apt o pip potrebbero presentarsi degli errori, nel caso aggiungere in coda "--break-system-packages"
- Andare su impostazioni e modificare il layout tastiera mettendo quello corretto
- Aprire il terminale ed eseguire in ordine:
  * sudo apt-get update
  * sudo apt-get upgrade -y
- Se presente installare gli aggiornamenti dall'icona comparsa in alto a destra vicino l'orario
- Riavviare

### Picamera2 - [Manuale ENG](https://datasheets.raspberrypi.com/camera/picamera2-manual.pdf)
Questa libreria vi permettera di accedere alle camere collegate al Raspberry Pi ed ottenere i vari frame
- Aprire il terminale ed eseguire:
  * sudo apt install -y python3-picamera2
  * Solo su Raspbarry Pi 5 eseguire anche sudo rpi-update pulls/5691
 
### OpenCV - [ENG TUTORIAL](https://www.geeksforgeeks.org/opencv-python-tutorial/) - [ENG DOCUMENTATION](https://docs.opencv.org/4.8.0/d6/d00/tutorial_py_root.html)
OpenCV è una libreria che vi permetterà di manipolare le immagini fornendovi strumenti utili ad individuare colori, forme e oggetti.
- Aprire il terminale ed eseguire:
 * pip3 install opencv-python
- ~~sudo apt install -y python3-pyqt5 python3-opengl~~
- ~~sudo apt install -y python3-opencv~~
- ~~sudo apt install -y opencv-data~~

### Codice per testare le camere - [ENG](https://toptechboy.com/using-the-raspberry-pi-camera-on-bullseye-os-and-opencv/)
Nel precedente link viene usata la libreria picamera2 per ottenere i frame della camera e OpenCV (cv2) per visualizzarli in una finestra grafica.

### GPIO - [ENG](https://www.raspberrypi.com/documentation/computers/os.html#gpio-and-the-40-pin-header)
I GPIO sono i pin della vostra scheda. ***!!!ATTENZIONE!!! I GPIO TOLLERANO SOLO TENSIONI INFERIORI AI 3,3V ALTRIMENTI SI DANNEGGIA IRREPARABILMENTE IL RASPBERRY PI. QUINDI NON COLLEGARE MAI DIRETTAMENTE I PIN DI ARDUINO E SENSORI CHE LAVORANO A 5V.***
Per collegare tra loro i GPIO e pin a 5V è necesario usare un convertitore logico ([LINK](https://www.sparkfun.com/products/12009)) oppure un photocoupler come il PC817C.

### Tesseract-ocr
Questa libreria che permette di estrapolare il testo contenuto in un immagine
- Aprire il terminale ed eseguire:
  * sudo apt-get install tesseract-ocr
  * pip install pytesseract

### Putty - [ENG](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
Questo software è un client SSH e vi permetterà di accedere al terminale da remoto.

### FileZilla - [ENG](https://filezilla-project.org/download.php?type=client)
Questo software è un client FTP e vi permetterà di accedere alle cartelle del Raspberry Pi da un computer esterno.
