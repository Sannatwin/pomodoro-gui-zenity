# Pomodoro Bash con Zenity

Questo repository contiene un semplice **Pomodoro Timer** realizzato in Bash con interfaccia grafica Zenity (Linux). L’obiettivo è sperimentare rapidamente risorse gratuite e open source per creare strumenti utili in autonomia: questo script è solo il primo passo di un percorso di apprendimento “learning by doing”.

---

## 📖 Descrizione

Lo script `pomodoro.sh` permette di:

* **Inserire il tempo totale di lavoro** (minimo 25 minuti) tramite una finestra di dialogo.
* **Ricevere una barra di progresso** che conteggia in minuti (da 25 a 0) e mostra i minuti rimanenti.
* **Essere avvisato di una pausa lunga** (20 minuti) ogni 4 cicli consecutivi da 25 minuti.
* **Ricevere il messaggio finale “OTTIMO LAVORO!!”** al termine di tutti i cicli.

Tutto è pensato per essere semplice, immediato e replicabile da chiunque abbia una distribuzione Linux con Zenity installato.

---

## ⚙️ Installazione

1. **Clona il repository**:

   ```bash
   git clone https://github.com/tuoutente/pomodoro-zenity.git
   cd pomodoro-zenity
   ```

2. **Rendi lo script eseguibile**:

   ```bash
   chmod +x pomodoro.sh
   ```

3. **Verifica di avere Zenity installato**:

   * Su Ubuntu/Debian:

     ```bash
     sudo apt-get update
     sudo apt-get install zenity
     ```
   * Su Fedora/RHEL:

     ```bash
     sudo dnf install zenity
     ```
   * Su Arch Linux:

     ```bash
     sudo pacman -S zenity
     ```

---

## ▶️ Utilizzo

Esegui lo script:

```bash
./pomodoro.sh
```

1. **Finestra di benvenuto**

   * Titolo: **POMODORO FAST LIFE** (testo centrato).
   * Pulsante “Go!” per procedere. Se premi “Annulla” o chiudi la finestra, appare un messaggio di arresto e lo script termina.

2. **Impostazione del tempo**

   * Inserisci il numero di minuti totali di lavoro (intero ≥ 25).
   * Se inserisci un valore non valido o minore di 25, viene mostrato un avviso e puoi riprovare.
   * Se clicchi “Annulla” o chiudi la finestra, appare un messaggio di arresto e lo script termina.

3. **Barra di progresso (in minuti)**

   * Viene avviato un ciclo di 25 minuti con una barra che si aggiorna ogni 60 secondi.
   * Sotto la barra compare il conteggio dei minuti rimanenti.

4. **Pausa lunga ogni 4 cicli**

   * Al termine di 4 cicli (100 minuti di lavoro) appare una finestra di pausa lunga:

     ```
     Hai completato 4 cicli!
     Ora pausa lunga: 20 minuti.
     ```
   * Dopo aver premuto “Ok, prendo la pausa”, lo script attende 20 minuti.
   * Se chiudi la finestra di pausa, appare un avviso di arresto e lo script termina.

5. **Messaggio finale**

   * Al termine di tutti i cicli (Tempo totale ÷ 25), compare la finestra:

     ```
     OTTIMO LAVORO!!
     ```

     e lo script termina.

---

## 🚧 Limiti attuali

* **Solo Linux**: funziona grazie a Zenity (GTK).
* **Interfaccia minimale**: finestre di dialogo e barra di progresso di base.
* **Nessuna versione Windows/macOS**: non esiste un equivalente diretto a Zenity su altri sistemi.
* **Funzionalità ridotte**:

  * Non ci sono pause brevi da 5 minuti.
  * Non esiste un flag “verbose” per mostrare secondi rimanenti.
  * Non sono previste suonerie o notifiche extra.

---

## 🌱 Miglioramenti possibili

* **Cross‐platform**

  * Sviluppare un eseguibile Windows (PowerShell + GUI) o una versione Python/Tkinter.
  * Creare una variante per macOS usando `osascript` o un’app nativa.

* **UI più ricca**

  * Aggiungere opzioni per pause brevi (5 minuti).
  * Integrare un flag `--verbose` per mostrare secondi rimanenti e log a terminale.
  * Aggiungere suoni o notifiche desktop (oltre a Zenity).
  * Realizzare un piccolo frontend web o un’app Electron per una GUI più curata.

* **Estensioni e personalizzazioni**

  * Salvare un log dei “pomodori” completati.
  * Permettere l’inserimento di minuti residui (ad esempio, se il totale non è multiplo di 25).
  * Aggiungere temi di colore o utilizzare altre librerie di dialogo.

---

## 🙌 Contribuisci

Ogni contributo è il benvenuto! Se hai idee, segnalazioni di bug o vuoi proporre miglioramenti:

1. **Forka** il repository.
2. Crea un **branch** dedicato (`git checkout -b mia-feature`).
3. Apporta le modifiche e testa localmente.
4. Fai un **commit** significativo (`git commit -m "Descrizione delle modifiche"`).
5. Pusha su **origin** (`git push origin mia-feature`).
6. Apri una **Pull Request** descrivendo il cambiamento.

---

## 📄 Licenza

Questo progetto è rilasciato sotto licenza **MIT**. Per ulteriori dettagli, consulta il file [LICENSE](LICENSE).

---

Grazie per aver visitato questo repository! 🚀
Se trovi utile lo script, metti una ⭐ e condividilo con chi potrebbe trovarlo interessante.

> *“Un piccolo passo alla volta: sperimentare, correggere e imparare insieme.”*

```
```

