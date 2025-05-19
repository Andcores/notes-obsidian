# [[Ruta]]
## 📍 **Etapa 1: Fundamentos de Sistemas y Redes**

### 🔧 Sistemas Operativos (Linux y Windows)

-  Comandos básicos de Linux (`ls`, `cd`, `grep`, `chmod`, `chown`, `ps`, `top`, etc.)
    
-  Estructura del sistema de archivos de Linux y Windows
    
-  Usuarios, grupos y permisos (ACLs)
    
-  Gestión de servicios y procesos (`systemctl`, `services.msc`)
    
-  Registro de eventos (Event Viewer, `journalctl`, `/var/log`)
    
-  Instalación de software (`apt`, `dnf`, `.msi`, `.exe`)
    

### 🌐 Redes y Comunicaciones

-  Modelo OSI y capas de red (7 capas)
    
-  Dirección IP, máscara de subred, gateway
    
-  NAT, DHCP, DNS
    
-  TCP vs UDP (diferencias, usos, estructura)
    
-  Comandos básicos de red (`ping`, `traceroute`, `nslookup`, `ipconfig`, `ifconfig`, `netstat`, `route`, `arp`)
    
-  Puertos comunes y servicios:
    
    - 21 (FTP), 22 (SSH), 23 (Telnet), 25 (SMTP), 53 (DNS), 80 (HTTP), 443 (HTTPS), 445 (SMB), 3389 (RDP)
        

---

## 🧱 **Etapa 2: Fundamentos de Ciberseguridad**

### 🔐 Principios Básicos

-  Modelo CIA (Confidencialidad, Integridad, Disponibilidad)
    
-  Qué es una amenaza, vulnerabilidad, riesgo y ataque
    
-  Ataques comunes:
    
    - Phishing
        
    - Brute Force
        
    - DDoS
        
    - Man-in-the-Middle (MitM)
        
    - SQL Injection
        
    - XSS (Cross-Site Scripting)
        
    - Malware: virus, gusanos, troyanos, ransomware, spyware
        
-  Autenticación vs Autorización
    
-  Concepto de política de seguridad
    

### 🔒 Seguridad General

-  ¿Qué es un firewall y cómo funciona?
    
-  ¿Qué es un IDS/IPS y diferencias?
    
-  ¿Qué es una VPN y para qué sirve?
    
-  ¿Qué es un proxy?
    
-  ¿Qué son los honeypots?
    

---

## 🧪 **Etapa 3: Laboratorio Práctico**

### 🧰 Herramientas de Análisis y Pentesting

-  Instalar y configurar Kali Linux
    
-  Escaneo de puertos y servicios con **Nmap**
    
-  Captura y análisis de paquetes con **Wireshark**
    
-  Uso de **Metasploit Framework** para pruebas básicas de explotación
    
-  Escaneo de vulnerabilidades con **Nikto**, **OpenVAS** o **Nessus (Free Tenable.io)**
    
-  Análisis de cabeceras HTTP con **Burp Suite**
    
-  Uso básico de **Hydra** para fuerza bruta
    

### 🧪 Prácticas en laboratorio

-  Crear entorno con VirtualBox: Kali + Windows + Metasploitable
    
-  Escaneo interno de red
    
-  Simular ataque de fuerza bruta (Hydra)
    
-  Capturar tráfico en red falsa (Wireshark)
    
-  Explorar vulnerabilidad simple en Metasploitable
    

---

## 🧠 **Etapa 4: Seguridad en Sistemas Operativos**

### 🛡️ Hardening de Linux

-  Configurar `ufw` o `iptables`
    
-  Deshabilitar servicios innecesarios
    
-  Configurar `/etc/hosts.allow` y `/etc/hosts.deny`
    
-  Revisar y proteger permisos de archivos
    
-  Implementar fail2ban o similar
    

### 🛡️ Hardening de Windows

-  Crear GPOs para seguridad (políticas de contraseñas, bloqueo de cuentas)
    
-  Activar firewall de Windows
    
-  Desactivar servicios no utilizados (SMBv1, Telnet, etc.)
    
-  Aplicar parches y actualizaciones
    
-  Revisar logs en Event Viewer
    

### 🧩 Gestión de Usuarios y Autenticación

-  Crear políticas de contraseñas seguras
    
-  Implementar autenticación en 2 pasos (2FA)
    
-  Control de accesos por roles (RBAC)
    

---

## 🚀 **Etapa 5: Exploración de Especialidades (Elegir 1 o 2)**

### 🥷 Hacking Ético / Pentesting

-  Reconocimiento: Whois, DNSenum, Gobuster
    
-  Escaneo y enumeración (Nmap avanzado, SMBenum, SNMPwalk)
    
-  Explotación con Metasploit
    
-  Post-explotación básica (migración de procesos, recolección de credenciales)
    
-  Reporte de hallazgos
    

### 🛡️ Blue Team / Defensa

-  Introducción a SIEM (Splunk, Wazuh, ELK)
    
-  Revisión de logs de red y host
    
-  Alertas y correlación de eventos
    
-  Detección de actividad sospechosa (LOLBins, scripts Powershell)
    
-  Reglas YARA básicas
    

### 🧬 Forense Digital

-  Preservación de evidencias (hash, write blocker)
    
-  Análisis de discos con Autopsy o FTK Imager
    
-  Extracción de artefactos: navegación, USB, ejecución de programas
    
-  Análisis de memoria RAM con Volatility
    

### 🧬 Análisis de Malware

-  Clasificación de malware
    
-  Estático vs dinámico
    
-  Análisis de PE files (.exe)
    
-  Entornos sandbox: Cuckoo
    
-  Herramientas: Ghidra, x64dbg, strings
    

### ☁️ Cloud Security (AWS, Azure, GCP)

-  Principios de IAM
    
-  Seguridad en S3, EC2, RDS
    
-  Configuración de alertas en AWS GuardDuty / CloudTrail
    
-  Análisis de seguridad con ScoutSuite, Prowler
    
-  Autenticación federada y multifactor (MFA)
    

---

## 🎓 Certificaciones Iniciales

-  ✅ **CompTIA Security+**
    
-  ✅ **Cisco CyberOps Associate**
    
-  ⬜ **CEH (Certified Ethical Hacker)**
    
-  ⬜ **OSCP (Ofensiva – más avanzada)**
    

---

## 🧑‍💻 Plataformas de Práctica

-  TryHackMe – Rutas: _Pre Security_, _Complete Beginner_, _Cyber Defense_
    
-  Hack The Box – _Starting Point_, _Academy_
    
-  OverTheWire – _Bandit_, _Narnia_
    
-  CyberDefenders – retos Blue Team
    
-  RangeForce – simuladores profesional