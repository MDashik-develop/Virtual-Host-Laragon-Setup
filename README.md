# Laragon-Virtual-Host-Setup

Laragon-e external drive (jemon D Drive) theke Laravel project othoba custom virtual host configure korar step-by-step guideline.

---

### **Step 1: Project Path Check Kora**<br>

Prothome D Drive-e apnar Laravel project-er `public` folder path thik ache kina nishchit hoye nin:

```text
D:/projects/spz/public
```

---

### **Step 2: Virtual Host Configuration File Toiri Kora**<br>

Laragon-er Apache config folder path-e jan:

```text
C:\laragon\etc\apache2\sites-enabled\
```

Oi folder-e ekti notun file toiri korun:

```text
spz.test.conf
```

*(Nishchit hon jeno file extension `.conf` hoy, `.txt` na hoy)*

File-ti open kore nicher code copy kore paste korun ebong save korun:

```apache
<VirtualHost *:80>
    DocumentRoot "D:/projects/spz/public"
    ServerName spz.test
    ServerAlias *.spz.test
    <Directory "D:/projects/spz/public">
        Options Indexes FollowSymLinks MultiViews
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
```

---

### **Step 3: Windows Hosts File-e Domain Map Kora**<br>

Windows hosts file open korar path:

```text
C:\Windows\System32\drivers\etc\hosts
```

*(Othoba Laragon dashboard-e right-click kore **Laragon** -> **Hosts file** open korte paren)*

File-tir ekdom seshe nicher line-ti boshaye save korun:

```text
127.0.0.1      spz.test
```

---

### **Step 4: Apache Server Restart Kora**<br>

Laragon dashboard theke server restart korun:

1. **Stop All** button-e click korun
2. **Start All** button-e click korun

---

### **Step 5: Browser-e Verify Kora**<br>

Browser open kore URL bar-e visit korun:

```text
http://spz.test
```

*(Purono browser cache thakle keyboard theke `Ctrl + F5` ba `Ctrl + Shift + R` press kore hard reload din)*
