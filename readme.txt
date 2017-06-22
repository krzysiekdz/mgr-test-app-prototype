Aplikacja testowa 

Badane frameworki: angular1, angular2, react oraz czysty javascript

Funkcjonalnosci i wyglad kazdej aplikacji s� identyczne. R�ni� si� natomiast wewn�trzn� struktur� kodu, a wiec sposobem w jaki realizuja te same zadania. Mierzony jest czas wykonywania poszczegolnych operacji. 
Interfejs aplikacji jest prosty, bez dodatkowych efekt�w wizaulnych (bogatsze ostylowanie wyd�u�a czas renderingu), aby uwydatni� wplyw dzia�ania danego frameworka (czyli czas dzia�ania kodu javascript) na wydajno�� mierzonych operacji. W sk�ad interfejsu wchodzi boczny panel menu (po lewej) gdzie mamy dost�p do wszystkich funkcjonalnosci. Po prawej w g�ownej cz�sci znajduje si� tabela w kt�rej b�d� wy�wietlane dane. Pojedy�czy obiekt danych to zwykly obiekt javascript posiadajacy wlasciwosci: id, imie, nazwisko, praca, zarobki. Dzia�ania s� wykonywane na du�ym zbiorze danych (1-2 tys element�w w modelu danych).


Funckjonalno�ci aplikacji - metody testowe (patrz folder 'screens'):

1.initial-view.png 
aplikacja - widok po za�adowaniu (na przykladzie aplikacji angularjs);

2.init1k.png
utworzenie 1tys elementow (losowych) - wpisanie ��danej liczby eleent�w do utworzenia i klikni�cie przycisku "init"

3.add_1kf.png 
uworzenie, czyli de facto dodanie (add) 1tys element�w (1k) - to samo co wyzej, ale w alternatywny sposob (tak�e losowych)

4.add_1m_1k.png 
dodanie (add) jednego elementu w �rodek (1m - 1 "middle") przy istniej�cym ju� 1 tysiacu element�w (1k) (utworzonym poprzez metod� opisan� w  2. lub 3.); pomiedzy elementy 500 a 501 pojawi� sie element o id=1001

5.add_1L_1k.png 
dodanie (add) 1 elementu na pozycj� ostatni� (1L - 1 "last") przy istniej�cym ju� 1tys elementow (1k); za elementem o id 1000 pojawil sie element id=1001

6.replace_3f_1k.png
replace - utworzenie nowych obiekt�w i zast�pienie nimi starych; 3f - 3 elementy na pocz�tku ("first") przy 1tys istniej�cych; zamiast obiekt�w o id=1,2,3 pojawily sie nowe o id=1001,1002,1003
analogicznie replaceII oznacza "wymian�" obiekt�w na srodku, a replaceIII na ko�cu

7.update_3f_1k.png 
update - aktualizacja istniej�ych obiekt�w nowymi danymi (czyli nie usuwamy obiekt�w i tworzymy nowe, ale zmieniamy tylko wartosci wlasciwosci tych obiekt�w); 3f - pierwsze 3, przy istniejacym 1tys element�w (1k); wizaulnie operacja daje to samo co operacja 6.
updateII i updateIII analogicznie w srodku i na koncu

8.update_evr3_1k.png 
aktualizacja co trzeci element (evr3) przy istniejacym 1tys elementow

9.swap_2f_1k.png 
swap - zamiania miejscami, dwoch s�siadujacych na pocz�tku (2f) element�w przy istniej�cym 1tys element�w (1k); widac ze elementy 1 i 2 zamienily sie miejscami
swapII, swapIII - analogicznie w srodku i na koncu

10.fetch_1k.png
fetch - pobranie, 1tys (1k) danych z serwera; dane te s� sta�e (zosta�y raz wygenerowane i zapisane w pliku)

11.input_1k.png 
wpisywanie danych do pola typu input, przy 1tys danych (1k)

12.edit_1k.png 
edycja pierwszej kom�rki w pierwszym wierszu danych, przy 1tys danych (1k); wpisanie w pole tekstowe ci�gu "aaa" - ten sam pojawil sie w kom�rce w pierwszym wierszu

13.filter_1k.png
filtrowanie danych - wyswietlanie tylko tych, kt�re maja wlasciwosc "id" podzieln� przez 10 (reszta jest ukrywana)

14.search_i_1k.png 
search - wyszukiwanie, znaku 'i' (i) przy 1tys (1k) istnejacyh elementow; wyszukane wyrazy sa podswietlane na ��to; wyszukiwanie badane jest gdy dane s� identyczne w kazdej aplikacji - a wiec pobrane metod� fetch (opisana w punkcie 10.); przygotowane dane maj� wlasciwosc, ze pewne znaki pojawiaja sie okreslona liczb� razy: z - 0,   b,y - 3   i,o-13   a,e - 26

15.remove_1f_1k.png
remove - usuni�cie, pierwszego elementu (1f) przy istniej�cych 1tys elementow (1k); pierwszy element zosta� usuniety (widac element o id=2 jako pierwszy)

16.select_1f_1k.png  
select - wybranie/klikniecie na pierwszy element (1f) przy istniejacym 1tys (1k) elementow

17.clear_1k.png 
clear- usuniecie/wyczyszczenie 1tys (1k) elementow 
