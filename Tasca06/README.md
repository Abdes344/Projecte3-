# T06: Fonaments del servei DNS

## 📝 Breu descripció
Com membres cada cop més integrats de l'equip tècnic de la consultora EverPia, teniu davant un nou repte. El vostre client, una empresa de màrqueting digital (DigiCore), que experimenta de tant en tant errors de connectivitat a certes aplicacions. El seu equip tècnic creu que la causa principal podria ser una resolució de noms (DNS) incorrecta o lenta.

Se us ha encarregat realitzar una auditoria teòrica i pràctica del servei DNS per tal de formar el personal del client i oferir eines de diagnosi ràpides.

---

## 📚 Fase teòrica: Sessió formativa
Com a part d’aquesta formació, caldrà que elaboreu un material formatiu pel personal del client. Per assegurar la màxima qualitat en els continguts, els vostres directors tècnics han preparat unes sessions prèvies, per tal que tingueu un domini dels conceptes que després haureu d’explicar.

Aproximadament els conceptes que haureu d’explicar seran els següents:

**🌳 Jerarquia i Estructura:** Explicació de l'estructura en arbre del DNS (Root > TLDs > Segon Nivell).  
**🔄 Procés de Resolució:** Com es realitza una consulta iterativa i una recursiva. Què és un servidor d'arrel (Root Server) i un servidor autoritatiu.  
**📂 Tipus de zones:** Directa i inversa. Zona primària i zona secundària.  
**📜 Tipus de Registres Clau (Records):** Descripció de la funció dels registres **A, CNAME, MX, NS i SVR**.  

### Conceptes Essencials
**✅ Resposta Autoritativa:** Què significa i com es pot identificar.  
**⏱️ Time To Live (TTL):** La seva funció i impacte en la propagació i el rendiment.  
**🛠️ Start of Authority (SOA):** Quina informació essencial conté i per què és crítica.  
**🔁 Reenviadors:** Condicionals i incondicionals.  
**🏠 Resolució local:** Mecanismes de resolució sense servidor entre equips clients. Inclou el protocol mDNS.

**🎬 Activitat de la fase teòrica:** Un cop domineu aquests conceptes, caldrà que prepareu la vostra píndola formativa, que consistirà en un vídeo d’entre 10 i 15 minuts, explicant de forma breu però clara aquests conceptes.

---

## 💻 Fase Pràctica: Diagnosi de Noms (Auditoria amb CLI)

Heu de demostrar l'ús de les principals utilitats de diagnosi DNS en els diferents sistemes operatius que utilitza el client (Linux/macOS i Windows).

**Configuració recomanada:** Equip Zorin amb dues interfícies:  
NAT  
Adaptador pont amb IP correctament configurada segons indicacions dels vostres responsables.

### 🖥️ Diagnosi Avançada amb dig (Linux / macOS)

| Comanda | Objectiu | Anàlisi |
|---------|----------|---------|
|
dig xtec.cat A
| Consulta bàsica de registre A | Identifica la IP de resposta, el valor TTL i el servidor que ha respost. |
|
dig tecnocampus.cat NS
| Consulta de servidors de noms | Quins són els servidors de noms autoritatius per a aquest domini? |
|
dig escolapia.cat SOA
| Consulta detallada SOA | Quina és la informació del correu de l'administrador i el número de sèrie del domini? |
|
dig -x 147.83.2.135
| Consulta de resolució inversa | Quina informació sobre els registres s’obté? |

---
