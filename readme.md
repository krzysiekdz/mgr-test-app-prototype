Aplikacja testowa - prototyp.
=======================

[powrót do strony głównej](https://github.com/krzysiekdz/mgr-main)


Funkcjonalnosci i wyglad kazdej aplikacji są identyczne. Różnią się natomiast wewnętrzną strukturą kodu, a wiec sposobem w jaki realizuja te same zadania. Mierzony jest czas wykonywania poszczegolnych operacji. Interfejs aplikacji jest prosty, bez dodatkowych efektów wizaulnych (bogatsze ostylowanie wydłuża czas renderingu), aby uwydatnić wplyw działania danego frameworka (czyli czas działania kodu javascript) na wydajność mierzonych operacji. W skład interfejsu wchodzi boczny panel menu (po lewej) gdzie mamy dostęp do wszystkich funkcjonalnosci. Po prawej w główej czesci znajduje się tabela w której będą wyświetlane dane. Pojedyńczy obiekt danych to zwykly obiekt javascript posiadajacy wlasciwosci: {id, imie, nazwisko, praca, zarobki}. Działania są wykonywane na dużym zbiorze danych (1-2 tys elementów w modelu danych).


### Funkcjonalności aplikacji

1.Widok po załadowaniu (na przykladzie aplikacji angularjs);
![](http://i.imgur.com/uqpmzpA.png)

2.init_1k
\nUtworzenie 1tys elementow (losowych) - wpisanie żądanej liczby elementów do utworzenia i kliknięcie przycisku "init".
![](http://i.imgur.com/kYL11FO.png)

3.add_1kf.png 
Uworzenie, czyli de facto dodanie (add) 1tys elementów (1k) - to samo co wyzej, ale w alternatywny sposob (także losowych).
![](http://i.imgur.com/5UhIecu.png)

4.add_1m_1k.png 
Dodanie (add) jednego elementu w œrodek (1m - 1 "middle") przy istniej¹cym ju¿ 1 tysiacu elementów (1k) (utworzonym poprzez metodê opisan¹ w  2. lub 3.); pomiedzy elementy 500 a 501 pojawi³ sie element o id=1001
![](http://i.imgur.com/vFsmeNK.png)

5.add_1L_1k.png 
dodanie (add) 1 elementu na pozycjê ostatni¹ (1L - 1 "last") przy istniej¹cym ju¿ 1tys elementow (1k); za elementem o id 1000 pojawil sie element id=1001
![](http://i.imgur.com/6R0q6mp.png)

6.replace_3f_1k.png
replace - utworzenie nowych obiektów i zast¹pienie nimi starych; 3f - 3 elementy na pocz¹tku ("first") przy 1tys istniej¹cych; zamiast obiektów o id=1,2,3 pojawily sie nowe o id=1001,1002,1003
analogicznie replaceII oznacza "wymianê" obiektów na srodku, a replaceIII na koñcu
![](http://i.imgur.com/fSvVLsl.png)

7.update_3f_1k.png 
update - aktualizacja istniej¹ych obiektów nowymi danymi (czyli nie usuwamy obiektów i tworzymy nowe, ale zmieniamy tylko wartosci wlasciwosci tych obiektów); 3f - pierwsze 3, przy istniejacym 1tys elementów (1k); wizaulnie operacja daje to samo co operacja 6.
updateII i updateIII analogicznie w srodku i na koncu
![](http://i.imgur.com/8BGAuIl.png)

8.update_evr3_1k.png 
aktualizacja co trzeci element (evr3) przy istniejacym 1tys elementow
![](http://i.imgur.com/pGAJNMR.png)

9.swap_2f_1k.png 
swap - zamiania miejscami, dwoch s¹siadujacych na pocz¹tku (2f) elementów przy istniej¹cym 1tys elementów (1k); widac ze elementy 1 i 2 zamienily sie miejscami
swapII, swapIII - analogicznie w srodku i na koncu
![](http://i.imgur.com/NwGr9u8.png)

10.fetch_1k.png
fetch - pobranie, 1tys (1k) danych z serwera; dane te s¹ sta³e (zosta³y raz wygenerowane i zapisane w pliku)
![](http://i.imgur.com/xJchvgo.png)

11.input_1k.png 
wpisywanie danych do pola typu input, przy 1tys danych (1k)
![](http://i.imgur.com/GgXPoSc.png)

12.edit_1k.png 
edycja pierwszej komórki w pierwszym wierszu danych, przy 1tys danych (1k); wpisanie w pole tekstowe ci¹gu "aaa" - ten sam pojawil sie w komórce w pierwszym wierszu
![](http://i.imgur.com/wx8H2kC.png)

13.filter_1k.png
filtrowanie danych - wyswietlanie tylko tych, które maja wlasciwosc "id" podzieln¹ przez 10 (reszta jest ukrywana)
![](http://i.imgur.com/BZ5pjx3.png)

14.search_i_1k.png 
search - wyszukiwanie, znaku 'i' (i) przy 1tys (1k) istnejacyh elementow; wyszukane wyrazy sa podswietlane na ¿ó³to; wyszukiwanie badane jest gdy dane s¹ identyczne w kazdej aplikacji - a wiec pobrane metod¹ fetch (opisana w punkcie 10.); przygotowane dane maj¹ wlasciwosc, ze pewne znaki pojawiaja sie okreslona liczbê razy: z - 0,   b,y - 3   i,o-13   a,e - 26
![](http://i.imgur.com/7HOYeyj.png)

15.remove_1f_1k.png
remove - usuniêcie, pierwszego elementu (1f) przy istniej¹cych 1tys elementow (1k); pierwszy element zosta³ usuniety (widac element o id=2 jako pierwszy)
![](http://i.imgur.com/dmqOOL2.png)

16.select_1f_1k.png  
select - wybranie/klikniecie na pierwszy element (1f) przy istniejacym 1tys (1k) elementow
![](http://i.imgur.com/5Zwvuoi.png)

17.clear_1k.png 
clear- usuniecie/wyczyszczenie 1tys (1k) elementow 
![](http://i.imgur.com/1n6jG01.png)
