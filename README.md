# Gym Site Manager 🇮🇹

Un sito web per la gestione di una palestra: login e profili per clienti e dipendenti, calendari, promozioni, messaggistica. Backend PHP, database MySQL (XAMPP) e tunnel pubblico con ngrok.

---

## 📁 Struttura delle directory

```
.
├── README.md                         # Documentazione del progetto
└── site/                             # Contiene tutta la logica dell'applicazione web
    ├── calendario_cliente.php        # Calendario riservato al cliente
    ├── calendario_dipendente.php     # Calendario per il dipendente
    ├── carica_ingressi.php           # Script per caricare ingressi
    ├── carica_iscritti.php           # Script per caricare iscritti
    ├── carica_messaggi.php           # Script per caricare messaggi
    ├── change_password.php           # Cambio password
    ├── db.php                        # Connessione al database
    ├── home_cliente.php              # Homepage lato cliente
    ├── home_dipendente.php           # Homepage lato dipendente
    ├── index.php                     # Entry point del sito
    ├── inserisci_iscritto.php        # Inserimento di un nuovo iscritto
    ├── invia_messaggio.php           # Invio messaggi
    ├── location_cliente.php          # Gestione location per cliente
    ├── location_dipendente.php       # Gestione location per dipendente
    ├── login_cliente.php             # Login per i clienti
    ├── login_dipendente.php          # Login per i dipendenti
    ├── logout.php                    # Logout
    ├── profilo_cliente.php           # Profilo cliente
    ├── profilo_dipendente.php        # Profilo dipendente
    ├── promo_cliente.php             # Promo visibili al cliente
    ├── promo_dipendente.php          # Promo gestite dal dipendente
    ├── sign_up.php                   # Registrazione nuovo utente
    ├── style/                        # Fogli di stile CSS divisi per pagina/ruolo
    │   ├── styles_calendario_cliente.css
    │   ├── styles_calendario_dipendente.css
    │   ├── styles_home_cliente.css
    │   ├── styles_home_dipendente.css
    │   ├── styles_location_cliente.css
    │   ├── styles_location_dipendente.css
    │   ├── styles_profilo_cliente.css
    │   ├── styles_profilo_dipendente.css
    │   ├── styles_promo_cliente.css
    │   └── styles_promo_dipendente.css
    └── img/                          # Risorse grafiche
        ├── 1.png
        ├── 2.png
        ├── 3.jpg
        ├── 4.png
        ├── 5.jpeg
        ├── background.png
        └── logo.png
```

---

## 🧰 Requisiti di sistema

* PHP 7.4+
* XAMPP (Apache + MySQL)
* ngrok (per tunnel pubblico)
* `git`

---

## 📦 Installazione su Ubuntu/Debian

```bash
sudo apt-get update
sudo apt-get install apache2 mysql-server php libapache2-mod-php php-mysql unzip
```

---

## ⚙️ Configurazione ambiente di sviluppo

1. Clona il repository:

   ```bash
   git clone https://github.com/<tuo-username>/gym-site.git
   cd gym-site/site
   ```
2. Copia i file nella cartella di XAMPP (es. `/opt/lampp/htdocs/gym-site` su Linux o `C:\xampp\htdocs\gym-site` su Windows).
3. Avvia XAMPP e attiva Apache e MySQL.
4. Importa il database MySQL dal file di dump (se presente) tramite Workbench o phpMyAdmin.
5. Modifica i parametri di connessione in `db.php`:

   ```php
   $host = '127.0.0.1';
   $user = 'root';
   $pass = '';
   $dbname = 'nome_database';
   ```

---

## 🔗 Tunnel pubblico con ngrok

Per esporre l’app localmente:

```bash
ngrok http 80
```

Copia l’URL generato (es. `https://abcd1234.ngrok.io`) e incollalo nel browser.

---

## 🚀 Avvio dell’applicazione

Con Apache e MySQL attivi e ambiente configurato:

1. Apri il browser su `http://localhost/gym-site/` o sull’URL di ngrok.
2. Effettua il login come cliente o dipendente.

---

## ✅ Funzionalità

* **Autenticazione:** login e registrazione per clienti e dipendenti.
* **Profili:** visualizzazione e modifica dei dati personali.
* **Calendario:** prenotazioni e orari per clienti e dipendenti.
* **Promozioni:** gestione e visualizzazione offerte.
* **Messaggistica:** invio e ricezione messaggi interni.
* **Ingressi e iscritti:** caricamento massivo tramite script PHP.

---

## 🧹 Pulizia

```bash
delete htdocs/gym-site folder
```

Per rimuovere il database locale, esegui in MySQL:

```sql
DROP DATABASE nome_database;
```

---

## ❓ FAQ

**Come cambiare la password di un utente?**
Usa la pagina `change_password.php` inserendo vecchia e nuova password.

**Perché usare ngrok?**
Permette di testare l’app in remoto condividendo un URL pubblico senza aprire porte sul router.

---

# Gym Site Manager 🇬🇧

A web site for managing a gym: client and staff login, profiles, calendars, promotions, messaging. PHP backend, MySQL database (XAMPP), and public tunnel via ngrok.

---

## 📁 Directory Structure

```
.
├── README.md                         # Project documentation
└── site/                             # All web application logic
    ├── calendario_cliente.php        # Client calendar
    ├── calendario_dipendente.php     # Staff calendar
    ├── carica_ingressi.php           # Upload entries script
    ├── carica_iscritti.php           # Upload members script
    ├── carica_messaggi.php           # Upload messages script
    ├── change_password.php           # Password change
    ├── db.php                        # Database connection
    ├── home_cliente.php              # Client homepage
    ├── home_dipendente.php           # Staff homepage
    ├── index.php                     # Site entry point
    ├── inserisci_iscritto.php        # New member registration
    ├── invia_messaggio.php           # Send messages
    ├── location_cliente.php          # Client location
    ├── location_dipendente.php       # Staff location
    ├── login_cliente.php             # Client login
    ├── login_dipendente.php          # Staff login
    ├── logout.php                    # Logout
    ├── profilo_cliente.php           # Client profile
    ├── profilo_dipendente.php        # Staff profile
    ├── promo_cliente.php             # Client promotions
    ├── promo_dipendente.php          # Staff promotions
    ├── sign_up.php                   # User registration
    ├── style/                        # CSS styles by page/role
    │   ├── styles_calendario_cliente.css
    │   ├── styles_calendario_dipendente.css
    │   ├── styles_home_cliente.css
    │   ├── styles_home_dipendente.css
    │   ├── styles_location_cliente.css
    │   ├── styles_location_dipendente.css
    │   ├── styles_profilo_cliente.css
    │   ├── styles_profilo_dipendente.css
    │   ├── styles_promo_cliente.css
    │   └── styles_promo_dipendente.css
    └── img/                          # Image assets
        ├── 1.png
        ├── 2.png
        ├── 3.jpg
        ├── 4.png
        ├── 5.jpeg
        ├── background.png
        └── logo.png
```

---

## 🧰 System Requirements

* PHP 7.4+
* XAMPP (Apache + MySQL)
* ngrok (for public tunnel)
* `git`

---

## 📦 Install on Ubuntu/Debian

```bash
sudo apt-get update
sudo apt-get install apache2 mysql-server php libapache2-mod-php php-mysql unzip
```

---

## ⚙️ Development Setup

1. Clone the repo:

   ```bash
   git clone https://github.com/<your-username>/gym-site.git
   cd gym-site/site
   ```
2. Copy files into XAMPP htdocs (e.g. `/opt/lampp/htdocs/gym-site` or `C:\xampp\htdocs\gym-site`).
3. Start Apache and MySQL from XAMPP control panel.
4. Import MySQL database via Workbench or phpMyAdmin.
5. Update connection settings in `db.php`:

   ```php
   $host = '127.0.0.1';
   $user = 'root';
   $pass = '';
   $dbname = 'database_name';
   ```

---

## 🔗 Public Tunnel with ngrok

Expose your local app:

```bash
ngrok http 80
```

Copy the generated URL (e.g. `https://abcd1234.ngrok.io`) and open it in your browser.

---

## 🚀 Running the Application

With Apache and MySQL running and environment configured:

1. Open `http://localhost/gym-site/` or the ngrok URL in your browser.
2. Log in as client or staff.

---

## ✅ Features

* **Authentication:** client and staff login/registration.
* **Profiles:** view and edit personal data.
* **Calendar:** bookings and schedules for clients and staff.
* **Promotions:** manage and view offers.
* **Messaging:** internal message sending and receiving.
* **Entries & Members:** bulk upload via PHP scripts.

---

## 🧹 Cleanup

```bash
delete htdocs/gym-site folder
```

To drop the local database, run in MySQL:

```sql
DROP DATABASE database_name;
```

---

## ❓ FAQ

**How to change a user password?**
Use the `change_password.php` page by providing old and new password.

**Why use ngrok?**
It allows remote testing by sharing a public URL without router port forwarding.

---

Happy coding! 🚀
