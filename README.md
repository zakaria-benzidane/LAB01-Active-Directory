# LAB-01 – Infrastructure Windows Server 2022 | TECHCORP

## Présentation du projet

Ce laboratoire consiste à concevoir, déployer et administrer une infrastructure informatique d'entreprise basée sur Windows Server 2022.

L'objectif est de mettre en place un environnement centralisé permettant la gestion des utilisateurs, des postes clients, des services réseau, des stratégies de sécurité et du partage de fichiers.

## Objectifs

- Déployer un contrôleur de domaine Active Directory.
- Configurer les services DNS et DHCP.
- Gérer les utilisateurs, groupes et unités organisationnelles.
- Appliquer des stratégies de groupe (GPO).
- Mettre en place un serveur de fichiers avec des permissions NTFS.
- Auditer les accès aux fichiers et dossiers.
- Configurer une sauvegarde et effectuer une restauration.
- Administrer le serveur à distance avec PowerShell.
- Réaliser des tests de connectivité et de dépannage réseau.

## Environnement technique

| Composant | Configuration |
|---|---|
| Hyperviseur | VMware Workstation 17 |
| Serveur | Windows Server 2022 |
| Client | Windows 10 Pro 22H2 |
| Domaine | corp.local |
| Nom du serveur | SRV-DC01 |
| Nom du client | CLIENT-01 |
| Réseau | 192.168.10.0/24 |
| Adresse serveur | 192.168.10.10 |
| Adresse client | 192.168.10.100 |
| DNS | 192.168.10.10 |
| DHCP | 192.168.10.100 – 192.168.10.200 |

## Architecture réseau

- Un serveur Windows Server 2022 configuré comme contrôleur de domaine.
- Un poste client Windows 10 intégré au domaine.
- Un réseau virtuel isolé VMware Host-only (VMnet1).
- Des services centralisés pour l'authentification, la résolution DNS et l'attribution des adresses IP.

## Travaux réalisés

### 1. Installation et configuration du serveur
- Installation de Windows Server 2022.
- Configuration du nom du serveur : SRV-DC01.
- Configuration d'une adresse IPv4 statique.

### 2. Active Directory Domain Services
- Installation et promotion du serveur en contrôleur de domaine.
- Création du domaine corp.local.
- Création des unités organisationnelles (OU).
- Création des utilisateurs et groupes de sécurité.

### 3. Services DNS et DHCP
- Configuration du DNS.
- Création d'une zone de recherche inversée.
- Configuration du serveur DHCP.
- Création et activation d'une étendue IPv4.
- Configuration des options DNS et du suffixe de domaine.

### 4. Group Policy (GPO)
- Configuration des stratégies de sécurité.
- Restriction de l'accès au Panneau de configuration.
- Mise en place d'une stratégie de restriction des supports de stockage amovibles.
- Vérification de l'application des GPO.

### 5. File Server et permissions
- Création des dossiers partagés IT, HR et Finance.
- Configuration des permissions NTFS.
- Gestion des accès selon les groupes de sécurité.
- Vérification des accès autorisés et refusés.

### 6. File Server Auditing
- Activation de l'audit du système de fichiers.
- Configuration des stratégies d'audit.
- Surveillance des accès aux fichiers et dossiers.
- Analyse des événements de sécurité, notamment l'Event ID 4663.

### 7. Windows Server Backup
- Installation de Windows Server Backup.
- Configuration d'une sauvegarde de l'état du système.
- Réalisation d'une sauvegarde de fichiers.
- Test de restauration d'un fichier supprimé.

### 8. Administration distante avec PowerShell
- Activation de PowerShell Remoting.
- Vérification du service WinRM.
- Connexion distante au serveur.
- Consultation des informations système et des services réseau.

### 9. Monitoring et Troubleshooting
- Tests de connectivité avec Test-Connection.
- Vérification DNS avec Resolve-DnsName.
- Diagnostic du domaine avec nltest.
- Vérification du canal sécurisé avec Test-ComputerSecureChannel.
- Contrôle de l'état des services DNS, DHCP et Active Directory.

## Tests et validation

| Test | Résultat |
|---|---|
| Connectivité serveur/client | Réussi |
| Résolution DNS | Réussi |
| Attribution DHCP | Réussi |
| Intégration au domaine | Réussi |
| Application des GPO | Vérifiée |
| Permissions du partage IT | Réussi |
| Restriction HR et Finance | Réussi |
| Audit des fichiers | Événement 4663 détecté |
| Sauvegarde | Réussie |
| Restauration | Réussie |
| Administration PowerShell distante | Réussie |

## Captures d'écran

Les captures d'écran documentent les différentes étapes de configuration, les tests réalisés et les résultats obtenus.

Consulter le dossier `screenchots/` pour les preuves techniques.

## Compétences développées

- Administration Windows Server 2022.
- Gestion d'Active Directory.
- Administration DNS et DHCP.
- Gestion des stratégies de groupe.
- Gestion des permissions NTFS.
- Audit et sécurité des fichiers.
- Sauvegarde et restauration.
- Administration distante avec PowerShell.
- Diagnostic et dépannage réseau.

## Conclusion

Ce laboratoire m'a permis de mettre en pratique les compétences fondamentales de l'administration des systèmes et réseaux dans un environnement virtualisé simulant une infrastructure informatique d'entreprise.

**Projet personnel – Portfolio technique**
