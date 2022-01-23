# Crittografica a chiave pubblica
---
Created: 05 dicembre 2021 17:37
Tags: #crittografia 
Reference:

---
## Crittografia a chiave pubblica
### Struttura crittografica a chiave pubblica
La cifratura asimmetrica consiste di 5 parti:
1. Plaintext: testo in chiaro
2. Algoritmo di cifratura: rende il testo cifrato
3. Chiave pubblica + Chiave privata: una chiave cifra e l'altra decifra
4. Testo cifrato: è il messaggio prodotto in output, illeggibile senza decifrazione
5. Algoritmo di decifrazione: prende testo cifrato + chiave e riporta il messaggio in chiaro

### Requisiti per crittografia a chaive pubblica
- Deve essere semplice per i possessori di chiavi cirfrare e/o decifrare i messaggi
- Deve essere computazionalmente impossibile decifrare un messaggio senza chiave
### Algoritmi di crittografia asimmetrica
- **RSA**: algoritmo di cifratura a blocchi il cui testo cifrato è composto da numeri interi da 0 a n. Chiavi lunghe 1024 bit sono considerate sicure.
- **Diffie-Hellman Key Agreement**: algoritmo per lo scambio di chiavi
- **Digital Signature Standard (DSS)**: firma digitale che usa SHA-1