# securite-mobile-lab3
## ÉTAPE 1 — Préparer Burp Suite
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/295ae3bc-b566-40c2-ae56-15f3b96d9511" />
## ÉTAPE 2 — Vérifier le Proxy Listener de Burp
<img width="1328" height="637" alt="image" src="https://github.com/user-attachments/assets/3c7dc591-3dcf-4462-a0f8-c08f94ae359c" />
## ÉTAPE 3 — Identifier l'adresse IP de votre machine hôte

<img width="540" height="194" alt="image" src="https://github.com/user-attachments/assets/f4514a80-3a38-40da-98cf-14131fba56f6" />

## ÉTAPE 4 — Configurer le proxy sur l'émulateur Android
<img width="448" height="864" alt="image" src="https://github.com/user-attachments/assets/82bb33f4-dcb2-47a3-b575-0c3b5f556cf1" />
##  Maintenant — Test immédiat 
<img width="448" height="864" alt="image" src="https://github.com/user-attachments/assets/346dba2c-ce11-4282-b2c8-faf5b1681429" />


# Configuration du Proxy Burp Suite

## ✅ Configuration réseau

| Élément | Valeur | Statut |
|---------|--------|--------|
| **Burp Listener** | `127.0.0.1:8081` (All interfaces) | ✅ |
| **IP hôte** | `10.0.2.2` | ✅ |
| **PORT_PROXY** | `8081` | ✅ |
| **Proxy Android** | Manual | ✅ |
| **Firewall Fedora** | port 8081 ouvert | ✅ |

##  Détails de configuration

### Burp Suite
- **Listener** : Toutes les interfaces (`127.0.0.1`)
- **Port** : `8081`

### Connexion Android
- **Adresse IP hôte** : `10.0.2.2`
- **Type de proxy** : Manuel
- **Port** : `8081`

### ÉTAPE 5 — Premier test de capture HTTP
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4e17ed33-7d45-43ed-98b7-844957498340" />

Note du prof — Observez ces détails importants :
Dans la requête ligne 1 (Request panel) vous voyez :
GET / HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0 (Linux; Android 10; K) AppleWebKit...
Accept-Language: en-US
Connection: keep-alive

C'est du HTTP pur — tout est en clair, aucun chiffrement !


✅ Étape 5 validée — La chaîne fonctionne parfaitement !
Émulateur → 10.0.2.2:8081 → Burp → Internet ✅


 
