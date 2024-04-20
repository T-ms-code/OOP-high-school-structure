# **Aplicatie pentru gestionarea ierarhiei unui liceu** : elevi, profesori si clase. De la clasa Elev s-a obtinut prin derivare subclasa Bursier, iar de la Profesor s-a obtinut Diriginte. De asemenea, Elev si Profesor sunt clase copil ale clasei abstracte Persoana, iar cele 4 materii din prima tema au fost eliminate in virtutea generalitatii prin adaugarea clasei Materie, care reda relatia ce compunere in raport cu clasa ce contine atat elevi, cat si profesori: "superclasa" Clasa. Functionalitatile initiale au fost extinse, meniul avand acum trei nivele de adancime. Printre noile optiuni se numara capacitatea de a acorda bursa, de a adauga o materie noua unei clase, cea de a face un istoric al persoanelor care au avut contact cu liceul, dar si altele.

## Cerințe obligatorii 

Nerespectarea duce la nepunctarea proiectului

- programul va fi scris în C++
- programul va avea un meniu interactiv (doar pentru ilustrarea funcționalității)
- programul nu are erori de compilare
- programul nu are warning-uri (folosind -Wall)
- existența a minim un punct din fiecare cerință
- fară variabile globale
- datele membre private
- fara headere specifice unui sistem de operare (<windows.h>)
- teste unitare pentru cerințele implementate (unde se poate, dacă nu apar probleme cu setup-ul de teste 😅)
- folosirea a funcționalităților limbajului fără sens
- folosirea a funcționlităților limbajului cu scopul de a încălca "legal" o altă regulă
    - folosirea excesivă a claselor friend
    - folosirea excesviă a elementelor statice  

## Tema 1

#### Cerințe
- [ ] definirea a minim **2-3 clase** care sa interactioneze in cadrul temei alese (fie prin compunere, agregare sau doar sa apeleze metodele celeilalte intr-un mod logic) (5p)
  - pentru o clasă:
    - [ ] constructori de inițializare
    - [ ] constructor supraîncărcat
    - [ ] constructori de copiere
    - [ ] `operator=` de copiere
    - [ ] destructor
    - [ ] `operator<<` pentru afișare (std::ostream)
    - [ ] `operator>>` pentru citire (std::istream)
    - [ ] alt operator supraîncărcat ca funcție membră
    - [ ] alt operator supraîncărcat ca funcție non-membră
  - pentru celelalte clase se va definii doar ce e nevoie
- [ ] implementarea a minim 3 funcții membru publice pentru funcționalități specifice temei alese, dintre care cel puțin 1-2 funcții mai complexe (3p)
- nu doar citiri/afișări sau adăugat/șters elemente într-un/dintr-un vector 
- [ ] scenariu de utilizare a claselor definite (1p):
  - crearea de obiecte și apelarea tuturor funcțiilor membru publice în main
  - vor fi adăugate în fișierul `tastatura.txt` DOAR exemple de date de intrare de la tastatură (dacă există); dacă aveți nevoie de date din fișiere, creați alte fișiere separat
- [ ] opțiune pentru citirea și afișarea a n obiecte (1p)

### Tema 2

#### Cerințe
- [x] separarea codului din clase în `.h` (sau `.hpp`) și `.cpp` [(0.5p)](https://github.com/Ionnier/poo/tree/main/proiect/P01#separarea-implement%C4%83rii-metodelor-din-clase)
  * fiecare clasa un fișier separat (sau cum considerați mai corect, însă codul să fie cât mai modular)
- [x] cât mai multe `const` [(0.5p)](https://github.com/Ionnier/poo/tree/main/labs/L04#reminder-const-everywhere)
- [x] moșteniri [(5p)](https://github.com/Ionnier/poo/tree/main/labs/L04#exemplu):
  - [x] minim o clasă de bază și **2 clase derivate**
  - [x] încercați să derivați o clasă creată anterior
    - dacă nu reușiți
      - creați o altă clasă care poate fi integrată cu clasele anterioare
      - menționați de ce nu ați reușit și ce ați încercat
  - [x] ilustrați [upcast](https://github.com/Ionnier/poo/tree/main/labs/L04#solu%C8%9Bie-func%C8%9Bii-virtuale-late-binding)-ul și [downcast](https://github.com/Ionnier/poo/tree/main/labs/L04#smarter-downcast-dynamic-cast)-ul folosind funcții virtuale și pointeri la clasa de bază
    - aceasta va fi făcută prin **2-3** metode specifice temei alese
    - funcțiile pentru citire / afișare sau destructorul nu sunt incluse deși o să trebuiască să le implementați 
  - [x] apelarea constructorului din clasa de bază din [constructori din derivate](https://github.com/Ionnier/poo/tree/main/labs/L04#comportamentul-constructorului-la-derivare)
  - [x] suprascris [cc](https://github.com/Ionnier/poo/tree/main/labs/L04#comportamentul-constructorului-de-copiere-la-derivare)/op= pentru copieri/atribuiri corecte
  - [x] destructor [virtual](https://github.com/Ionnier/poo/tree/main/labs/L04#solu%C8%9Bie-func%C8%9Bii-virtuale-late-binding)
- [x] funcții și atribute `static` (în clase) [(1p)](https://github.com/Ionnier/poo/tree/main/labs/L04#static)
- [x] excepții [(1p)](https://github.com/Ionnier/poo/tree/main/labs/L04#exception-handling)
  - porniți de la `std::exception`
  - ilustrați propagarea excepțiilor
  - ilustrati upcasting-ul în blocurile catch
  - minim folosit într-un loc în care tratarea erorilor în modurile clasice este mai dificilă
- [x] folosirea unei clase abstracte (fie la exceptii, fie la moșteniri) [(0.5p)](https://github.com/Ionnier/poo/tree/main/labs/L04#clase-abstracte)
- [x] actualizarea meniului & scenariului de utilizare [(0.5p)](https://github.com/Ionnier/oop-template-t1/blob/main/main.cpp#L16)
- [x] citirea și afișarea a n obiecte [(0.5p)](https://github.com/Ionnier/oop-template-t1/blob/main/main.cpp#L13)
  - poate fi combinat cu demonstrarea upcasting-ului & downcast-ului printr-un vector către o clasă de bază
  - poate fi făcut oriunde (dacă aveți deja o clasă cu un vector, de exemplu o clasă Coș cu un vector<Produs>)
- [x] existența unui pull request către branch-ul în care lucrați ce include adăugarea unei noi derivate ce evidențiază că modificările aduse sunt minimale (0.5p)
  - derivata nu poate fi una ștearsă și rescrisă
  - derivata va avea date membre noi + o modificare de comportament pe una dintre funcțiile virtuale

### Tema 3

#### Cerințe
 - Clase template (3p)
   - [ ] crearea unei ierarhii de clase template cu minim 2 clase
   - [ ] ilustrarea RTTI pe clase template
   - [ ] instanțieri cu logică a claselor create
 - STL (2p)
   - [ ] utilizarea a două structuri (containere) din (fără <vector>)
   - [ ] utilizarea a unui algoritm cu funcție lambda (de exemplu, sort, transform)
 - Design Patterns (2p)
   - [ ] utilizarea a două șabloane de proiectare
 - Prezentare (3p)
   - [ ] răspunsuri la întrebări din cod / generale C++
   - [ ] explicarea a unei alte structuri sau a altui algoritm neutilizat (STL)
   - [ ] explicarea a altor două șabloane de proiectare


## Recomandare Tema

* rezolvați tema 1 cu niște itemi generali ca să puteți extinde tema cu ușurință la următoarele teme.
  - coș de cumpărături + produse
  - sistem de validare a documentelor + documente de identitate
  - sistem de gestionare a biletelor + bilet 
* funcționalitatea creată să folosească metode ale obiectului generic 
* ar fi bine ca relația de agregare să fie făcută cu un obiect general în stilul celor de mai sus ^
* branch-uri + commit-uri punctuale
