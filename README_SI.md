# Repair Shop Management System – Version 3

මෙම සංස්කරණයේ පරිශීලකයා පෙන්වා දුන් කරුණු තුන සංශෝධනය කර ඇත:

1. **Invoice Repair/Parts Details** – A5 Invoice එකේ එක් එක් Job එකට Item, Reported Fault, Repair Details, Parts Used, Parts Cost සහ Amount පෙන්වයි.
2. **Job Parts ↔ Stock** – Job Editor එකේ Stock එකේ ඇති parts තෝරා quantity දිය හැක. Save කරන විට stock එකෙන් අඩු වේ. කලින් Job එකට ඇතුළත් කළ part quantity වෙනස් කළහොත් වෙනස අනුව stock නැවත ගණනය වේ. Available stock ඉක්මවා ඇතුළත් කළ නොහැක. POS එකද stock අඩු කරයි.
3. **Registered Members ↔ Fields** – Members ලෙස ලියාපදිංචි කළ අය Received By, Inspected By, Repaired/Completed By සහ Cashier fields වලින් තෝරාගත හැක.

අමතරව Job Number එක අනුව status lookup එකේ repair/parts/parts cost/notes/total ද පෙන්වයි.

## Install / Run
- Node.js LTS ස්ථාපනය කරන්න.
- මෙම folder එකේ Command Prompt විවෘත කර `npm install` සහ `npm start` ක්‍රියාත්මක කරන්න.
- Browser එකෙන් `http://localhost:3000` විවෘත කරන්න.

## Job parts භාවිතය
1. Stock / POS හි parts සහ opening stock ලියාපදිංචි කරන්න.
2. Jobs / Receipt හි Job එකක් සාදන්න.
3. Edit Full Job තෝරන්න.
4. Stock list එකෙන් parts tick කර quantity ඇතුළත් කරන්න.
5. Save Job Updates කරන්න. Stock quantity එක ස්වයංක්‍රීයව අඩු වේ.

## Existing database
පැරණි `data.sqlite` ගොනුව මෙම version එකේ folder එකට copy කළ හැක. `job_parts` table එක පළමු ආරම්භයේදී ස්වයංක්‍රීයව සාදනු ලැබේ. මුලින් backup එකක් ගන්න.

## Production / Online
මෙය local starter system එකකි. Internet භාවිතයට deploy කිරීමට පෙර authentication, role-based authorization, HTTPS, audit logs, backups, restore testing සහ security review එක් කළ යුතුය. Stock/Job/Invoice flows ကို production data-க்கு முன் test செய்யவும்.
