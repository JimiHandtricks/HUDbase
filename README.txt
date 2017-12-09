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

2a.Stahni si vertzy z remote > prikaz 'git pull'.

2. Over si stav repozitare prikazem 'git status'.
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
(krok 4.)

b) Muzes tyto zmeny na tvrdo smazat.
Musis si ale uvedomit, ze tim prijdes o nejakou praci.
Pokud nevis co jsi naposled delal,
porovnej svuj kod s kodem na remote.
Git ti kazdopadne poradi o jake soubory se jedna.
Ve vystupu prikazu 'git status' by jsi mel videt,
ze tam sviti cervene nejake soubory. 
V tech je prave rozdil oproti remote serveru.
Prikazy na smazani:
'git reset --hard' > resetuje zmeny na zmenenych souborech
'git clean -fd' > smaze nove pridane soubory a slozky


Pokud vidis toto:
"On branch master
Your branch is ahead of 'origin/master' by # commit(s).
...."

znamena to, ze nemas pushnute nejake commity.
Pouzij prikaz 'git push origin #branchName',
kde #branchName = jmeno aktualni vetve.

Pokud vidis toto:
"On branch master
Your branch is behind 'origin/master' by # commit(s), and can be
fast-forwarded.
....
"
znamena to ze na lokalu si pozadu,
oproti remote repozitari. 
Pouzij prikaz 'git pull'.

To je snad vse co bys po prikazu 'git status' mel vydet.
Kazdopadne kdyby nahodou, je tu google :D

3. Vytvoreni vetve pro praci na lokale.
Predpokladejme ze je teda tva verze aktualni
a git status ti ukazuje ...Your branch is up-to-date with ....
V tuhle chvili muzes vytvorit vlastni vetev ve ktere budes pracovat.
Na to pouzij prikaz: 
'git checkout -b #nazevBranche',
kde #nazevBranche je nazev nove vetve.
Jakmile zadas tento prikaz, 
misto masteru by ti tam mel modre svitit naze nove vetve.

4. Ulozeni zmen a jejejich pushnuti na remote.
Jakmile jsi skoncil svou praci a nebo uz mas dost,
uloz vsechny zmeny v souborech
a vlez do git bashe (terminal).
Znova pouzij prikaz 'git status',
ja ho pouzivam skoro porad.
Mel by si tam videt, ze mas nejake nekomitle soubory. 
Ty by mely svitit cervene.
Je nutne tyto soubory komitnout.
Nejprve pouzij prikaz:
'git add #nazevSouboru', kde #nazevSouboru = jmeno souboru sviticiho cervene.
Pokud se ti nechce psat nazev souboru,
pouzij prikaz:
'git add -A'

Znovu pouzij 'git status' > zadne soubory by tam svitit nemely.
Nyni mas zaznamenane zmeny, je cas komitnout.
Pouzij prikaz:
'git commit -m "Zprava o komitu > co sem zmenil, co sem dokoncil atp.."'
kde to v "" je nejaky popisek commitu. 
Je dobre tam psat smysluplne veci 
at je jasne co se v danem commitu zmenilo.
Ted uz staci zmeny pushnout na remote.
Pouzij prikaz:
'git push origin #nazevVetve', kde #nazevVetve = nazev aktualni vetve.

Jakmile provedes tento prikaz,
na remote by se mela vytvorit nova vetev 
se stejnym nazvem.

5. Pull Request a sjednoceni tve vetve s master vetvi.
Nyni je nova vetev na remote > gitHubu.
Jdi na gitHub a over si ze tam ta vetev pribyla.
Pro jistotu stranku znova nacti.
Pak rozklikni dropdown 'Branch: mastr'
a mel bys tam videt novou vetev.
Prepni se do nove vetve.
V pravo nahore by melo byt tlacitko "Pull Request".
Klikni nan.
Mel by ses objevit na strance 'Open a pull request'.
Napis tam nejaky popisek toho co jsi dokoncil
 a klikni na "Create pull request".
Timto se vytvori "Pull Request". 
Je dobre si dobre rozmyslet,
zda doopravdy chces aplikovat zmeny do master vetve.
Kdyz je pull request otevren,
ostatni ho muzou videt taky.
Jsou tam videt zmeny oproti master vetvy atp.

Pokud si jsi jisty ze chces zmeny aplikovat,
klikni na "Merge Pull Request".
Pak uz to staci potvrdit a hotovo.
Zmeny jsou v masteru.
Ted uz je mozno vymazat nove vytvorenou vetev.


Jakmile uz mas jednou repozitar naklonovany (krok 1.)
pri dalsi praci uz staci opakovat kroky 2-5.
2. Overit si stav a podle nej reagovat,
typicky pullnout si nove veci prikazem 'git pull'.
3. Vytvorit si novou vetev.
4. Commitni a pushni zmeny.
5. Vytvor pull request a mergni zmeny do master vetve
+ smaz vetev.
