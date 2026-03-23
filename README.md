# 🛡️ Mòdul de Seguretat: Rols i JWT

Aquest mòdul gestiona l'autenticació i l'autorització dels usuaris mitjançant JSON Web Tokens (JWT) i el control d'accés basat en rols (RBAC).

## 📺 Vídeo de l'exercici
Pots veure la demostració de la seguretat i l'explicació del codi aquí:
👉 **[Veure vídeo de l'exercici](https://www.youtube.com/watch?v=7Dqnf_b1mFQ)**

## 🚀 Implementació Tècnica

### **Backend (Node.js & MongoDB)**
* **Definicions de Rol:** Inclusió del camp `role` (admin/user) al model d'usuari de Mongoose per segmentar permisos.
* **Middleware de Control:** Creació d'un filtre de seguretat (`checkRole`) per bloquejar rutes de l'API segons el permís extret del token.
* **Tokens Segurs:** Configuració del JWT perquè transporti la identitat de l'usuari i el seu rol de forma xifrada i signada.

### **Frontend (Angular)**
* **Protecció de Rutes:** Implementació de l' `authGuard` per evitar que usuaris no autoritzats entrin visualment a la zona d'administració.
* **Gestió d'Estat:** Servei d'autenticació actualitzat per llegir les dades del token i adaptar la interfície segons l'usuari connectat.

---

## 🤖 Declaració d'ús d'IA Generativa
**IA Generativa:** ChatGPT / Gemini (Google)

**Parts del codi assistides per IA:**

* **Generació i verificació del Token (Backend):**
    * **Configuració de Seguretat:** M'ha ajudat a configurar tant els tokens d'accés com els de refresc per assegurar que la informació de l'usuari viatgi correctament en el payload.
    * **Validació de dades:** M'ha servit de guia per comprovar que les dades extretes del token siguin vàlides al servidor abans de permetre qualsevol accés a les rutes de l'API.

* **Middleware de Control d'Accés i Rutes (Frontend/Backend):**
    * **Filtre de seguretat (CheckRole):** Vaig demanar a la IA com escriure el codi del middleware que comprova si un usuari té el permís necessari (per exemple, si és administrador) per entrar en una ruta específica.
    * **Gestió d'errors:** M'ha ajudat a programar els missatges d'error com el "403 Accés denegat" per quan algú intenta fer una petició a una zona on no té permís.
    * **Estructura de rutes:** M'ha servit per organitzar quines rutes han de ser privades i quines públiques, ajudant-me a configurar l' `authGuard` d'Angular per bloquejar l'accés a nivell de navegació.



