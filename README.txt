1. Naklonovani repozitare.
Pokud nemas git bash, tak si ho stahni zde: "https://git-for-windows.github.io/".
Naistaluj ho.
Zapni ho.
Objevi se terminal.
Bokem si vytvor slozku, kde chces mit repozitar.
Nyni se musis v terminalu dostat do pozadovane slozky.
Pokud jsi napr. vytvoril slozku na plose,
dostanes se do ni zadanim tohoto prikazu:
'cd C:/Users/#userName/Desktop', kde #userName = tve uzivatelske jmeno.
Jakmile jses v pozadovane slozce, 
zadej tento prikaz:
'git clone #linkToRepository', kde #linkToRepository je odkaz na repositar,
v tomto pripade "https://github.com/JimiHandtricks/HUDbase.git".
V terminalu by se melo objevit ze se to nejak provedlo.
Ve slozce by se mela vytvorit nova slozka s nazvem "HUDbase".
Dostan se do ni prikazem 'cd HUDbase'.
V terminalu by ti ted mel modre svitit napis "(master)",
coz indikuje to, ze jsi v repozitari na vetvy master.

2. Prace v lokalnim (na tvem komplu) repozitari.
2a. Over si stav repozitare prikaze 'git status'.
