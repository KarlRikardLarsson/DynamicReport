# Dynamisk rapport
Automatiskt installerar en applikation för dynamisk rapport i Qlik Cloud-miljö.

![image](https://github.com/user-attachments/assets/0cf4b72f-8849-47b9-b2f2-dd38a6eb1646)


## Innehållsförteckning
1. [Info](#info)
2. [Installation](#installation)
3. [Slutförd](#slutförd)

---

## Info
### Hur den väljer ut vilka fält som ska vara dimensioner:
Fält kan inte vara en nyckel eller ett gömt fält.  
Sedan loopar den igenom alla fält och masterdimensioner.  
Efter det kontrolleras om fältet eller masterdimensionerna används i ett objekt eller i en mastervisualisering i ett PUBLICERAT ark. Om det används i ett objekt, läggs det till i rapporten.  
Har fältet taggen `$Date`, läggs det i period.

---

## Installation
### Steg 1
Kör automationen, ingen konfiguration behövs.

![image](https://github.com/user-attachments/assets/531953d9-d75a-447b-aaa3-64ebe2939313)

### Steg 2
Fyll i den efterfrågade informationen: `Appid` för skanning är applikationen som den dynamiska rapporten ska skapas från. Denna information är obligatorisk. `Output name` och `SpaceID` är valfria; om dessa fält lämnas tomma kommer rapporten att installeras i personliga utrymmet med namnet "Dynamisk Rapport."

![image](https://github.com/user-attachments/assets/1f6d4398-90d1-46ff-a49e-4ec6cad2625d)

### Steg 3
Nu visas alla tabeller och huvudmått i appen. Välj vilken tabell som är transaktionstabellen (mått kommer endast att skapas från denna tabell) samt vilka huvudmått i appen som ska inkluderas i rapporten.

![image](https://github.com/user-attachments/assets/8ab1fa44-976c-4730-8f65-28f073ab5203)

---

## Slutförd
Rapporten är nu installerad! Viss konfiguration kan behövas, speciellt för datumdimensioner. Vissa fält kan inte identifieras som datum och då måste de ändras till en annan inline-tabell. Du kan också manuellt lägga till dimensioner, mått och datum.

![image](https://github.com/user-attachments/assets/17a2b65e-1593-4274-88c6-3190f9dbdca4)

