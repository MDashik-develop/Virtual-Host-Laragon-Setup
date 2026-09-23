# Virtual-Host-Laragon-Setup
Markdown# Laragon-Virtual-Host-Setup

Laragon-e external drive (jemon D Drive) theke Laravel project othoba custom virtual host configure korar step-by-step guideline.

---

### **Step 1: Project Path Check Kora**<br>
Prothome D Drive-e apnar Laravel project-er public folder path thik ache kina check kore nin:
```text
D:/projects/spz/public
Step 2: Virtual Host Configuration File Toiri KoraLaragon-er Apache config folder path:PlaintextC:\laragon\etc\apache2\sites-enabled\
Ekhane ekti notun file toiri korun:Plaintextspz.test.conf
(File extension jeno .conf hoy, .txt na hoy)File-ti open kore nicher code copy kore paste kore save korun:Apache<VirtualHost *:80>
    DocumentRoot "D:/projects/spz/public"
    ServerName spz.test
    ServerAlias *.spz.test
    <Directory "D:/projects/spz/public">
        Options Indexes FollowSymLinks MultiViews
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
Step 3: Windows Hosts File-e Domain Map KoraWindows hosts file path:PlaintextC:\Windows\System32\drivers\etc\hosts
(Othoba Laragon window-te right click kore Laragon -> Hosts file open korun)   File-er ekdom seshe nicher line-ti paste kore save korun:Plaintext127.0.0.1      spz.test
Step 4: Apache Server Restart KoraLaragon dashboard theke server restart korun:Stop All button click korun   Start All button click korun   Step 5: Browser-e Verify KoraBrowser open kore URL bar-e visit korun:Plaintext[http://spz.test](http://spz.test)
(Purono cache clean korar jonno keyboard theke Ctrl + F5 ba Ctrl + Shift + R press korun)
