# Dynamisk rapport
En automation som automatiskt installerar en dynamisk rapport i din Qlik Cloud-miljö.

![image](https://github.com/user-attachments/assets/0cf4b72f-8849-47b9-b2f2-dd38a6eb1646)

![image](https://github.com/user-attachments/assets/200e6468-59de-43c1-a6f7-d573b489040c)


## Innehållsförteckning
1. [Info](#info)
2. [Installation](#installation)
3. [Slutförd](#slutförd)

---

## Info
### Urval av dimensioner:
- Fält kan inte vara en nyckel eller ett dolt fält.
- Applikationen loopar igenom alla fält och masterdimensioner.
- Den kontrollerar om fältet eller masterdimensionerna används i ett objekt eller en mastervisualisering i ett PUBLICERAT ark. Om fältet används, inkluderas det i rapporten.
- Om fältet har taggen `$Date`, klassificeras det som en perioddimension.

### Urval av mått:
- Fältet måste finnas i transaktionstabellen.
- Fältet måste vara ett numeriskt värde.
- Fältet måste ha mer än ett distinkt värde.
- Mastermått läggs till baserat på användarens manuella val.

---

## Installation
### Steg 1
Ladda ner och installera JSON-filen från repositoryt och ladda upp den till din workspace.

![image](https://github.com/user-attachments/assets/52a54133-7824-4a2d-be11-0e55aae2215a)

### Steg 2
Kör automationen – ingen ytterligare konfiguration behövs.

![image](https://github.com/user-attachments/assets/531953d9-d75a-447b-aaa3-64ebe2939313)

### Steg 3
Fyll i den efterfrågade informationen:
- `Appid` är obligatoriskt och identifierar applikationen som ska skannas för att skapa den dynamiska rapporten.
- `Output name` och `SpaceID` är valfria. Om dessa fält lämnas tomma installeras rapporten i ditt personliga utrymme med namnet "Dynamisk Rapport."

![image](https://github.com/user-attachments/assets/1f6d4398-90d1-46ff-a49e-4ec6cad2625d)

### Steg 4
Välj transaktionstabellen (endast fält från denna tabell används för att skapa mått) och de mastermått som ska inkluderas i rapporten.

![image](https://github.com/user-attachments/assets/8ab1fa44-976c-4730-8f65-28f073ab5203)

---

## Slutförd
Rapporten är nu installerad! Viss justering kan behövas, särskilt för datumdimensioner. Om ett datumfält inte identifieras korrekt kan det ändras till en annan inline-tabell. Du kan även manuellt lägga till dimensioner, mått och datum om det behövs.

![image](https://github.com/user-attachments/assets/17a2b65e-1593-4274-88c6-3190f9dbdca4)


