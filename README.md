# 🛠️ Active Directory & SIEM Monitoring avec Splunk

## 📌 Description

Ce projet met en place une infrastructure **Active Directory** simulée à l'aide de **GNS3**, en intégrant des machines sous **Windows Server 2022**, **Windows 10**, **Kali Linux**, **Ubuntu Server**, ainsi que des outils de surveillance **SIEM** tels que **Splunk**, **Sysmon**, et **Splunk Universal Forwarder**. Le réseau est également sécurisé avec un **routeur MikroTik** pour la gestion des flux réseau et la configuration des VLANs.

Le but est de créer une infrastructure de sécurité robuste permettant de surveiller les événements d'Active Directory et de détecter les menaces grâce à l'intégration de **Splunk SIEM**.

## 🏗️ Architecture du projet

- **🔹 GNS3** : Simulation du réseau, incluant un **routeur MikroTik** pour la gestion du trafic et des VLANs  
- **🖥️ Windows Server 2022** : Contrôleur de domaine Active Directory  
- **💻 Windows 10** : Poste client Windows dans le domaine  
- **🐧 Kali Linux** : Machine de test pour les simulations d'attaque  
- **📦 Ubuntu Server** : Héberge **Splunk** pour la collecte et l’analyse des logs  
- **📡 Splunk Universal Forwarder** : Collecte des logs systèmes depuis les machines Windows et Kali  
- **📊 Sysmon** : Surveillance et enregistrement détaillé des événements Windows  
- **🌐 MikroTik Router** : Gère la connectivité réseau et l’isolation des segments de réseau  

## 🎯 Objectifs du projet

✅ Mettre en place un **domaine Active Directory** avec un **Windows Server 2022**  
✅ Ajouter un **Windows 10** comme poste client membre du domaine  
✅ Utiliser **Kali Linux** pour effectuer des tests d'attaque (ex. Brute-force, Pass-the-Hash)  
✅ Installer **Splunk** sur **Ubuntu Server** pour collecter et analyser les logs système  
✅ Configurer **Splunk Universal Forwarder** pour envoyer les logs de **Sysmon** et **Active Directory** vers **Splunk**  
✅ Configurer un **routeur MikroTik** pour gérer le routage et la segmentation du réseau  
✅ Surveiller les événements du réseau et d'Active Directory pour détecter les menaces en temps réel  

## 🚀 Installation et Configuration

### 1️⃣ **Installation du réseau dans GNS3**
- Télécharger et installer **GNS3**  
- Créer une topologie réseau simulée comprenant un **routeur MikroTik** pour gérer les VLANs et le routage  
- Connecter les machines **Windows Server 2022**, **Windows 10**, **Kali Linux**, et **Ubuntu Server**

### 2️⃣ **Configurer Active Directory (Windows Server 2022)**
- Installer le rôle **Active Directory Domain Services (AD DS)**  
- Créer un domaine **(ex: ad.local)**  
- Ajouter le **Windows 10** au domaine en tant que poste client  

### 3️⃣ **Configurer le routeur MikroTik**
- Configurer les **VLANs** pour segmenter le réseau  
- Mettre en place des règles de **sécurité de routage** pour limiter les attaques réseau  
- Configurer le **NAT** et le **firewall** pour sécuriser le réseau  

### 4️⃣ **Déployer Splunk SIEM sur Ubuntu Server**
- Installer **Splunk Enterprise** sur **Ubuntu Server**  
- Configurer les **sources de données** pour collecter les logs de Windows et des autres machines  
- Créer des **dashboards personnalisés** pour surveiller les logs d’Active Directory et les événements système  

### 5️⃣ **Installer et Configurer Sysmon et Splunk Universal Forwarder**
- Installer **Sysmon** sur les machines **Windows 10** et **Windows Server 2022** pour enregistrer les événements système détaillés  
- Installer le **Splunk Universal Forwarder** sur les machines **Windows** et **Kali Linux** pour envoyer les logs vers **Splunk**  
- Configurer le **forwarder** pour envoyer les logs de **Sysmon** et des événements AD vers **Splunk**

## 📊 Tableaux de bord et alertes

- **Tableaux de bord** personnalisés dans **Splunk** pour analyser les logs d'Active Directory, les connexions utilisateurs et les actions suspectes  
- **Alertes en temps réel** pour la détection des attaques réseau et des tentatives d’intrusion  
- **Détection des activités malveillantes**, telles que les tentatives de Brute-force, les élévations de privilèges, et les accès non autorisés  

## 📸 Capture d’écran

_Ajoutez ici des captures d'écran de la topologie GNS3, des dashboards Splunk et de l'interface MikroTik_  

## 📄 Ressources utiles

- [GNS3 - Documentation Officielle](https://docs.gns3.com/)  
- [Splunk - Getting Started](https://docs.splunk.com/Documentation/Splunk)  
- [Sysmon - Microsoft Docs](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon)  
- [MikroTik - Documentation Officielle](https://wiki.mikrotik.com/wiki/Main_Page)  

## 🤝 Contribuer

Les contributions sont les bienvenues ! Pour suggérer des améliorations ou signaler des problèmes, veuillez ouvrir une **issue** ou une **pull request**.

---

📌 **Auteur** : [Votre Nom]  
📆 **Date** : Mars 2025  
📜 **Licence** : MIT  
