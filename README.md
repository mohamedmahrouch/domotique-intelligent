# Smart Home Ecosystem 🏠

Une solution IoT complète pour la gestion centralisée d'une maison connectée avec contrôle vocal local et interfaces multiplateforme.

## 📋 Vue d'ensemble

Ce projet propose un écosystème complet de maison connectée comprenant :
- **Application mobile** cross-platform (Flutter)
- **Interface web** progressive (Angular)
- **Backend API** robuste (FastAPI)
- **Système de reconnaissance vocale** local (Whisper)
- **Réseau de microcontrôleurs** embarqués (ESP32/Arduino)

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐
│   Mobile App    │    │    Web App      │
│    (Flutter)    │    │   (Angular)     │
└─────────┬───────┘    └─────────┬───────┘
          │                      │
          └──────────┬───────────┘
                     │
          ┌─────────────────┐
          │   Backend API   │
          │   (FastAPI)     │
          └─────────┬───────┘
                    │
    ┌───────────────┼───────────────┐
    │               │               │
┌───▼────┐    ┌────▼────┐    ┌────▼────┐
│ ESP32  │    │ Arduino │    │ Whisper │
│Capteurs│    │Actuateurs│   │  Voice  │
└────────┘    └─────────┘    └─────────┘
```

## ✨ Fonctionnalités principales

### 🎯 Contrôle centralisé
- Gestion unifiée de tous les équipements connectés
- Dashboard temps réel avec monitoring des capteurs
- Automatisations et scénarios personnalisables
- Historique et analytics des données

### 🗣️ Reconnaissance vocale
- Traitement vocal 100% local (préservation de la confidentialité)
- Intégration OpenAI Whisper pour une reconnaissance précise
- Commandes vocales personnalisables
- Support multilingue

### 📱 Interfaces utilisateur
- **Mobile** : Interface native optimisée pour smartphones/tablettes
- **Web** : PWA responsive accessible depuis tout navigateur
- Design adaptatif et intuitif
- Synchronisation temps réel entre plateformes

### 🔧 Architecture technique
- **Microservices modulaires** pour une scalabilité optimale
- **Communication temps réel** via WebSocket
- **Protocoles IoT** (MQTT/CoAP) pour les microcontrôleurs
- **Base de données** optimisée pour l'IoT
- **API RESTful** documentée avec Swagger

## 🚀 Installation

### Prérequis
- Python 3.8+
- Node.js 16+
- Flutter SDK 3.0+
- ESP32/Arduino IDE

### Backend (FastAPI)
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

### Frontend Web (Angular)
```bash
cd frontend-web
npm install
ng serve
```

### Application Mobile (Flutter)
```bash
cd mobile-app
flutter pub get
flutter run
```

### Microcontrôleurs
1. Ouvrir les sketches Arduino dans l'IDE
2. Configurer les paramètres WiFi
3. Téléverser sur les ESP32/Arduino

## 📡 Configuration

### Variables d'environnement
```bash
# Backend
DATABASE_URL=sqlite:///./smart_home.db
MQTT_BROKER=localhost:1883
WHISPER_MODEL=base

# Frontend
API_BASE_URL=http://localhost:8000
WEBSOCKET_URL=ws://localhost:8000/ws
```

### Configuration réseau
- Configurer le broker MQTT
- Définir les adresses IP des microcontrôleurs
- Paramétrer les credentials WiFi

## 🔌 Équipements supportés

### Capteurs
- Température et humidité (DHT22)
- Luminosité (LDR)
- Mouvement (PIR)
- Qualité de l'air (MQ-135)

### Actuateurs
- Éclairage LED (PWM)
- Relais pour appareils électriques
- Servomoteurs pour volets/stores
- Buzzer pour notifications

## 📊 API Documentation

La documentation complète de l'API est disponible à :
- Swagger UI : `http://localhost:8000/docs`
- ReDoc : `http://localhost:8000/redoc`

### Endpoints principaux
```
GET    /devices           # Liste des équipements
POST   /devices           # Ajouter un équipement
PUT    /devices/{id}      # Modifier un équipement
DELETE /devices/{id}      # Supprimer un équipement

GET    /sensors/data      # Données des capteurs
POST   /voice/command     # Traitement commande vocale
WS     /ws               # WebSocket temps réel
```

## 🔒 Sécurité

- **Chiffrement** des communications (TLS/SSL)
- **Authentification** JWT pour les API
- **Traitement local** de la reconnaissance vocale
- **Isolation réseau** des microcontrôleurs
- **Validation** stricte des entrées utilisateur

## 🧪 Tests

```bash
# Tests backend
cd backend
pytest

# Tests frontend web
cd frontend-web
ng test

# Tests mobile
cd mobile-app
flutter test
```

## 📈 Monitoring

- **Logs centralisés** avec rotation automatique
- **Métriques** de performance en temps réel
- **Alertes** en cas de dysfonctionnement
- **Dashboard** de monitoring système

## 🤝 Contribution

1. Fork le projet
2. Créer une branche feature (`git checkout -b feature/nouvelle-fonctionnalite`)
3. Commit les changements (`git commit -m 'Ajout nouvelle fonctionnalité'`)
4. Push sur la branche (`git push origin feature/nouvelle-fonctionnalite`)
5. Ouvrir une Pull Request

## 📝 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## 👥 Équipe

- **Développement Backend** : FastAPI, Whisper, MQTT
- **Développement Frontend** : Angular, Flutter
- **Développement Embarqué** : ESP32, Arduino
- **Architecture** : Microservices, IoT, Temps réel

## 🔗 Ressources

- [Documentation FastAPI](https://fastapi.tiangolo.com/)
- [Guide Flutter](https://flutter.dev/docs)
- [Documentation Angular](https://angular.io/docs)
- [ESP32 Reference](https://docs.espressif.com/)
- [OpenAI Whisper](https://github.com/openai/whisper)

## 📞 Support

Pour toute question ou problème :
- Créer une issue GitHub
- Consulter la documentation
- Contacter l'équipe de développement

---

**Version actuelle** : 1.0.0  
**Dernière mise à jour** : Août 2025
