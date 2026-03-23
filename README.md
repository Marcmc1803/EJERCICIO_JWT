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

* **Configuració de Seguretat (JWT):** He utilitzat la IA com a eina de consulta per definir correctament els temps d'expiració dels tokens i per verificar que la informació de l'usuari s'extreu correctament del payload al servidor.
* **Lògica del Middleware i Rutes:** M'ha servit de guia per estructurar el middleware `checkRole` i per assegurar-me que l' `authGuard` d'Angular bloquegés l'accés a les rutes privades de forma eficient segons el rol de l'usuari.
