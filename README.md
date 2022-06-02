## Treść zadania
Firma DataVac, zajmuje się symulowaniem ewolucji wirusów, aby umożliwić  szybszą produkcję szczepionek.  Szalejąca epidemia spowodowała zwiększone  zapotrzebowanie na jej usługi. Firma rozbudowała swoją siedzibę tworząc na sąsiedniej działce dodatkowe budynki.  Dział HR  jest bardzo przywiązany do idei budowania różnorodnych środowisk pracy celem zwiększenia efektywności.  Aby to osiągnąć, dział HR  postanowił,  że poszczególne działy będą podzielone pomiędzy budynkami (każdy dział będzie miał pracowników w dwóch budynkach). Rozwiązanie to ma taką zaletę, że pozwala także zbudować jednolitą kulturę korporacyjną.

Po rozbudowie siedziba firmy usytuowana jest w trzech budynkach: A, B i C. W budynku C znajduje się nowoczesne centrum obliczeniowe. Podział hostów na działy i budynki zaproponowany przez dział HR i zaakceptowany przez zarząd zawiera tabela poniżej.


|Nazwa działu \ budynek | A | B | C (centrum obliczeniowe) |
|-|-|-|-|
|Zarząd | 5 | 5 | - | 
|HR | 10 | 5 | - |
|Dział programistyczny | 20 | 50 |- |
|Administratorzy IT | 1 | 1 | 5 |
| Dział księgowy | 4 | 4 | - |
| Serwery w centrum obliczeniowym | - | - | 1000|



Budynki są okablowane siecią Ethernet i połączone ze sobą siecią światłowodową. Budynki B i C mają bezpośredni dostęp do Internetu, każdy z nich poprzez innego operatora, natomiast budynek A korzysta z łącza internetowego budynku B.

Operatorzy przyznali dla budynku B stały adres IP 124.138.0.12/24 z bramą domyślną 124.138.0.23, natomiast dla budynku C, adres 211.93.11.10/24, z bramą domyślną 211.93.11.224.

## Wymagania ogólne:

1. Należy zapewnić bezpieczny transfer i swobodne współdzielenie danych w obrębie  poszczególnych działów.
2. Należy zapewnić szczególną ochronę podsieci działu zarządu.
3. W każdym budynku należy zapewnić dostęp do Internetu także dla gości firmy (w taki sposób, aby goście nie mieli dostępu do zasobów firmowych).
4. W każdym budynku powinna być zainstalowana sieć przewodowa zbudowana na bazie Ethernetu i sieć bezprzewodowa zbudowana na bazie Wi-Fi.
5. Każdy z działów powinien mieć możliwość udostępniania danych wyłącznie pracownikom swojego działu (dla innych działów te dane nie powinny być dostępne).
6. Powinna być także możliwość udostępniania pewnych danych wszystkim pracownikom firmy w taki sposób, by nie były one dostępne bezpośrednio z sieci zewnętrznej.
7. Firma będzie chciała udostępniać własny serwis WWW .
8. Poszczególne działy firmy potrzebują serwerów z różnego rodzaju oprogramowaniem: systemem zarządzania projektami, bazą danych, repozytorium.

## Oczekiwana zawartość projektu:
1. Rysunek przedstawiający konfigurację sieci, zawierający:
    - Podział na poszczególne sieci i\lub VLAN-y (z naniesionymi adresami IP i maskami przypisanymi do każdej sieci).
    - Schemat rozmieszczenia i połączenia urządzeń fizycznych: komputerów, ruterów, przełączników, punktów dostępowych, itd.
    - Schemat rozmieszczenia i połączenia istotnych urządzeń "logicznych": serwerów (np. WWW, DNS), zapór ogniowych, agentów, itd.
    - Nazwy istotnych interfejsów sieciowych i przydzielone do nich adresy IP.
    - Nazwy domenowe hostów (tych, które mają przydzielone nazwy, np. serwer WWW).
2. Określenie rodzaju i liczby urządzeń sieciowych, które będą potrzebne, czyli np. przełączniki, rutery, maszyny serwerowe itp. (nie ma konieczności określania dokładnego modelu sprzętu).
3. Dla każdego rutera jego tablica tras, gdy wszystkie połączenia działają oraz ich modyfikacja dla sytuacji awaryjnych. Należy wziąć pod uwagę sytuację, gdy jedno z dwóch dostępnych łączy internetowych ulegnie awarii - chcemy, aby wtedy nadal w całej firmie był dostęp do Internetu.
4. Reguły NAT.
5. Schemat przydzielania adresów IP oraz określenie gdzie będą przydzielane statycznie a gdzie dynamicznie.
6. Schemat przydzielania wewnętrznych nazw, sposób rozwiązywania nazw - czy będzie używany wewnętrzny serwer DNS, czy zewnętrzna usługa. Konfiguracja DNS (plik strefy). Należy wziąć pod uwagę, że tylko serwer WWW powinien być widoczny z zewnątrz.
