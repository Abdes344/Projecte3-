Un cop superada la fase de formació ✅, ja esteu preparats per afrontar el repte dels nostres clients. Tal com es va explicar, tenim un nou i important client: el bufet d’advocats **Garriga i Associats** ⚖️, un dels més prestigiosos de la ciutat. Gestionen una gran quantitat d'informació legal sensible, fet que fa que la **integritat**, la **disponibilitat** (alta redundància) i la **facilitat de gestió** del seu emmagatzematge siguin essencials 🔐💼.

La direcció de *Garriga i Associats* ha expressat la necessitat urgent de renovar els seus sistemes de servidors ⚙️, per garantir que la informació estigui protegida davant fallades de disc i que l'espai es pugui ampliar sense interrupcions ➕💾.

Com a tècnics d’**EverPia** 👨‍💻👩‍💻, teniu l’encàrrec de dissenyar i documentar solucions d’emmagatzematge que compleixin aquests requisits, tant en entorns **Linux** com **Windows**. Aquest disseny formarà part de la proposta que presentarem al client.

L’objectiu principal és crear **dues solucions d’emmagatzematge** (una per Linux i una per Windows) que garanteixin:
- 🟢 Alta disponibilitat  
- 🟢 Redundància  
- 🟢 Escalabilitat  

Es tracta d’una **prova de concepte**, així que treballareu amb màquines virtuals de sistemes operatius *clients* per documentar els procediments.

---

## 1️⃣ Part Linux: LVM amb Zorin OS 🐧

S'utilitzarà Zorin OS (o una alternativa Linux compatible) per demostrar l’ús del **Logical Volume Manager (LVM)**.

### ✅ Requisits de la Implementació i Demostració

- **Configuració Inicial**:  
  - Crear un *Volume Group (VG)* i un *Logical Volume (LV)* amb **dos discos de 10 GB**.  
  - Formateu i munteu automàticament el volum modificant `/etc/fstab`.

- **Alta Disponibilitat**:  
  - Implementar un **mirall LVM (lvm_mirror)** per protegir la informació davant la fallada d’un disc.

- **Instantànies (Snapshots)**:  
  - Afegir dos discos de 10 GB al VG.  
  - Crear un volum `lvm_dades`, formatar-lo i muntar-lo.  
  - Afegir arxius (per exemple, imatges d’Internet 📸).  
  - Crear un **snapshot** (`lv_snapshot`) i demostrar com restaurar-lo en cas de corrupció del volum original.

- **Escalabilitat**:  
  - Utilitzar l'espai restant del VG per **ampliar** el volum `lv_dades` ➕.

---

## 2️⃣ Part Windows: Espais d’Emmagatzematge 💻🪟

Es farà servir **Windows 11** per demostrar les configuracions possibles mitjançant **Storage Spaces**.

### ✅ Requisits de la Implementació i Demostració

- **Configuració Inicial**:  
  - Crear un **Storage Pool** amb **tres discos de 10 GB**.

- **Estudi de Configuracions**:
  - **Mirroring (2 discos)**: garantia d’alta disponibilitat 🔁  
  - **Parity (3 discos)**: explicar l’eficiència d’espai en comparació amb el mirall 📊  
  - **Triple Mirroring**: afegir els discos necessaris ➕🧩

- **Gestió i Visualització**:  
  - Mostrar l’estat dels discos i del pool des de la consola de gestió de Windows 🖥️✅.

---

## 🧑‍🤝‍🧑 Com treballareu i què lliurareu?

- El treball és **en grup**.  
- Dividiu-vos en dos equips:  
  - Equip Linux (LVM) 🐧  
  - Equip Windows (Storage Spaces) 🪟  
- Cada membre crearà **el seu propi guió**: comandes, documentació, passos, etc.  
- Les parelles realitzaran la **demostració pràctica**.  
- El grup revisarà la documentació i **cada membre la pujarà al seu repositori**.

### 📂 Documentació

- S’ha de crear una carpeta `tasca03` dins del projecte.  
- Incloure:
  - Documentació en **Markdown**  
  - Imatges, explicacions i captures de pantalla 🖼️  
  - Un `README.md` amb:
    - Descripció de la tasca  
    - Enllaços als dos documents  

🔔 *La nota és conjunta, així que cal una bona coordinació i comunicació.*

### 🎤 Presentació

Posteriorment, presentareu **conjuntament** al client les conclusions del treball realitzat.

---

## 📚 Material de classe (Moodle)

- **LVM Linux**  
- **Espais d’emmagatzematge (Windows)**  


