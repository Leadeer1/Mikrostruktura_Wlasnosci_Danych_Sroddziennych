# Mikrostruktura_Wlasnosci_Danych_Sroddziennych
**ANALIZA MIKROSTRUKTURY I WŁASNOŚCI DANYCH ŚRÓDDZIENNYCH | 11/2025**

**Narzędzia**
  * R
  * tidyverse
  * ggplot2
  * rugarch
  * forecast
  * moments
  * R Markdown  

**Problem**
Konieczność zbadania własności mikrostrukturalnych danych transakcyjnych dwóch spółek giełdowych o zróżnicowanym poziomie cen i płynności, w tym identyfikacja śróddziennej sezonowości zmienności oraz weryfikacja założeń o rozkładzie stóp zwrotu w kontekście hipotezy efektywności rynku.  

**Rozwiązanie**
  * Przeprowadzono czyszczenie i preprocessowanie danych tick-by-tick z okresu 6 miesięcy, filtrując transakcje pakietowe i pozasesyjne
  * Opracowano funkcje do obliczania statystyk opisowych dla ceny, wolumenu i odstępów między transakcjami
  * Zaimplementowano agregację danych do interwałów 1-sekundowych i 5-minutowych z zastosowaniem metody last-tick
  * Przeprowadzono testy normalności (Jarque-Bera) oraz analizę autokorelacji stóp zwrotu i zmienności (ACF, Ljung-Box)
  * Stworzono profile dzienne (intraday means) dla stóp zwrotu, wolumenu, liczby transakcji i zmienności
  * Zwizualizowano wyniki w formie wykresów: histogramy, QQ-plots, ACF, profile śróddzienne w ggplot2


**Wynik**
  * Zidentyfikowano charakterystyczny kształt "U" dla aktywności handlowej i zmienności w ciągu sesji (szczyty przy otwarciu i zamknięciu, minimum w południe)
  * Potwierdzono leptokurtyczny rozkład stóp zwrotu z grubymi ogonami, odrzucając hipotezę normalności
  * Wykazano silną autokorelację zmienności wskazującą na efekt klastrowania volatility
  * Udokumentowano różnice w płynności
  * Stwierdzono brak systematycznych trendów w śróddziennych stopach zwrotu
  * Projekt zrealizowano w zespole 4-osobowym, z pełną dokumentacją w R Markdown.


