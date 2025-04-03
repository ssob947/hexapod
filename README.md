# Exapod

Questo repository documenta lo sviluppo di un esoscheletro robotico a 6 zampe progettato per camminare in modo fluido e trasportare oggetti delicati come bicchieri pieni di birra. Il progetto è modulare, ingegnerizzato per robustezza, compensazione meccanica e adattabilità.

---

##  Roadmap di sviluppo

###  FASE 1 – Camminata base (versione leggera)
 *Far camminare il robot in avanti in modo fluido e stabile*

- Stampare i **piedini in TPU** per assorbire micro-imprecisioni
- Ottimizzare il **ciclo del passo** con spline, easing e raccordi morbidi
- Test su **una gamba** o su **camminata intera tripode**
- Validare fluidità, stabilità e corretto caricamento dei servo (anche a vuoto)
- *(Niente microswitch per passo completato, in vista della futura camminata curva)*

###  FASE 2 – Prototipo con servo Miuzei 15kg/cm
 *Testare tutto il sistema con componenti reali e prime simulazioni di carico*

- Fare una **lista componenti completa**
- Ordinare **tutto per UNA zampa** → montarla e testarla
- Se va bene, procedere con ordine per  tutte le zampe
- Realizzare una **bozza di telaio centrale** con **vano di carico**
- Impostare un primo **layout cablaggio** completo già pronto per la versione definitiva
  *(layout ordinato ed estetico solo dopo il prototipo; **dissipatori** da considerare già ora)*

###  FASE 3 – Ottimizzazione software e calibrazione hardware
 *Correggere angoli reali, allineare coordinate e preparare il sistema per versioni future*

- Spostare il **frame centrale** al baricentro del robot
- Scrivere routine per **calibrazione offset servo**
- Pensare (tempo permettendo) a **switch o sensori per calibrazione automatica**
- Implementare la **camminata curva**
- Aggiungere un **sensore a ultrasuoni** e iniziare:
  - rilevamento ostacoli
  - strategia di evitamento in base alla direzione

###  FASE 4 – Passaggio al sistema definitivo
 *Implementare il robot finale con brushless, struttura robusta e rifinitura software completa*

- Sostituire servo con **brushless 40kg/cm**
- Verificare **struttura, dissipazione e assorbimenti**
- Finalizzare cablaggio, telaio, PCB e layout completo
- Validare camminata su piano, curva, con carico e in ambienti reali

---

##  Checklist operativa Fase 1 – Camminata base

###  Preparazione hardware
- [ ] Stampare i tip in TPU (flessibilità)
- [ ] stampare Tibia con alloggio switch del tip
- [KO] ammortizzamento tibia. NO: ammortizzamento oltre 2mm vanifica sline e raccordi se non cinematica stessa, spostare eventualmente in progetto finale in piastra di alloggio vano di carico centrale
- [ ] Verificare fissaggio piedino su tibia
- [ ] Montare una gamba singola per test (J1–J2–J3)

###  Software
- [ ] Ottimizzare ciclo del passo con **spline e easing**
- [ ] test singola zampa
- [ ] Verificare fluidità, senza vibrazioni o strattoni

###  Test e validazione
- [ ] Testare camminata in avanti (ciclo completo)
- [ ] Controllare temperatura servo dopo vari cicli
- [ ] Logging angoli/calcoli via `Serial` (per debug futuro), per ora commentati

---

##  Note
