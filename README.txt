GIT NAVOD

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
Pokud vydis toto:
"On branch master
Your branch is up-to-date with 'origin/master'.

nothing to commit, working tree clean"

pak je vse ok a mas nejaktualnejsi verzy masteru,
muzes si vytvorit svoji vlastni branch a pracovat v ni. 
(krok 3.)

Pokud vydis toto:
"On branch master
Your branch is up-to-date with 'origin/master'.

Changes not staged for commit:
.... atd.."

znamena to ze mas na lokale nejake neulozene,
ne-komitle, zmeny. Mas dve moznosti jak to spravit: 
a) Muzes tyto zmeny komitnout
a pushnout na remote (repozitar na gitHubu).
(krok 5.)

b) Muzes tyto zmeny na tvrdo smazat.
Musis si ale uvedomit, ze tim prijdes o nejakou praci.
Pokud nevis co jsi naposled delal,
porovnej svuj kod s kodem na remote.
Git ti kazdopadne poradi o jake soubory se jedna.
Ve vystupu prikazu 'git status' by jsi mel videt,
ze tam sviti cervene nejake soubory. 
V tech je prave rozdil oproti remote serveru.
Prikazy na smazani:
'git reset --hard' > resetuje zmeny na upravenych souborech
'git clean -fd' > smaze nove pridane soubory a slozky


