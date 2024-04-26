# Środowiska Udostępniania Usług

## Temat projektu - Argo

### Autorzy

- Gabriel Kaźmierczak
- Dariusz Piwowarski
- Wojciech Przybytek
- Przemysław Roman

### Spis treści

1. [Podstawy teoretyczne](#podstawy-teoretyczne)
2. [Podział pracy w zespole](#podział-pracy-w-zespole)
3. [Koncepcja Demo](#koncepcja-demo)
4. [Technologie realizacji Demo](#technologie-realizacji-demo)
5. [Opis konfiguracji](#opis-konfiguracji)
6. [Postępy prac](#postępy-prac)
7. [Prezentacja Demo](#prezentacja-demo)

### Podstawy teoretyczne

**[Kubernetes](https://kubernetes.io/)** to oprogramowanie open source służące do automatyzacji wdrażania, skalowania i
zarządzania aplikacjami kontenerowymi. Zostało zaprojektowane przez Google, a obecnie jest utrzymywane przez Cloud
Native Computing Foundation. Kubernetes dostarcza platformę do uruchamiania aplikacji w kontenerach na dużą skalę,
zarządzając infrastrukturą i zapewniając funkcje, takie jak self-healing (automatyczne restartowanie kontenerów),
odkrywanie usług i load balancing, przechowywanie danych, skalowanie i wiele innych.

**[Argo](https://argoproj.github.io/)** jest projektem open source, który dostarcza narzędzia do tworzenia, uruchamiania i
zarządzania pracami w kontenerach Kubernetes. Składa się z podprojektów, w których skład wchodzą Argo Workflows, Argo
CD, Argo Rollouts oraz Argo Events.

**[Argo Workflows](https://argoproj.github.io/workflows/)** to silnik do tworzenia i uruchamiania prac w kontenerach.
Pozwala na definiowanie złożonych przepływów pracy (workflow), które mogą obejmować wiele zadań uruchamianych w różnych
kontenerach, z możliwością kontroli przepływu, takiej jak równoległe lub sekwencyjne uruchamianie zadań, decyzje
warunkowe, pętle i inne. Argo Workflows jest szczególnie przydatne w środowiskach takich jak przetwarzanie danych, czy
uczenie maszynowe, gdzie istnieje potrzeba koordynacji wielu zadań.

**[Argo CD](https://argoproj.github.io/cd)** to narzędzie do ciągłej dostawy (Continuous Delivery, CD), które
implementuje podejście GitOps do zarządzania infrastrukturą. W modelu GitOps, żądane stany systemów są zapisywane w
repozytorium Git, a narzędzia automatycznie aktualizują systemy, aby dopasować je do stanu zapisanego w Git. Argo CD
monitoruje repozytorium i automatycznie wdraża zmiany na środowiska Kubernetes, gdy stan w Git się zmienia.

Oba omawiane podprojekty Argo są zintegrowane z Kubernetes i wykorzystują jego funkcje, takie jak API, schematy autoryzacji i mechanizmy
skalowania. Dzięki temu są one naturalnym rozszerzeniem ekosystemu Kubernetes i mogą być łatwo zintegrowane z innymi
narzędziami w tym ekosystemie.

### Podział pracy w zespole

Ponieważ w ramach tego projektu omawiamy dwa zastosowania Argo zdecydowaliśmy na podział zespołu na dwa podzespoły, każdy omawiający jedno z zastosowań.
Docelowo praca obu podzespołów ma zostać połączona, tworząc integralną całość.

#### Podzespół 1 - Argo CD

Osoby: Dariusz Piwowarski, Przemysław Roman

Cele: Stworzenie klastra Kubernetes na AWS oraz uruchomienie w nim Argo CD i zintegrowanie go z repozytorium aplikacji

#### Podzespół 2 - Argo Workflows

Osoby: Gabriel Kaźmierczak, Wojciech Przybytek

Cele: Zapoznanie się z API Argo Workflows, napisanie aplikacji wykorzystującej to API oraz udostępniającej własny interfejs

### Koncepcja Demo

Demo będzie zawierać aplikację działającą w klastrze Kubernetes, która zaprezentuje możliwości narzędzi Argo Workflows oraz Argo CD.

Aplikacja będzie służyć jako punkt wejścia do uruchamiania zadań w Argo Workflows. Użytkownik będzie mógł wysyłać
żądania HTTP do aplikacji uruchamiające odpowiednie workflowy za pomocą API do Argo Workflows.

Każda zmiana w repozytorium przechowującym kod aplikacji będzie automatycznie wykrywana przez Argo CD, które następnie zaktualizuje działającą aplikację na klastrze.

### Technologie realizacji Demo

- Amazon Elastic Kubernetes Service - AWS EKS zapewni infrastrukturę na której będzie działał klaster Kubernetes
- GitHub - przechowywanie repozytorium Git z kodem źródłowym aplikacji
- Python 3 - język implementacji aplikacji
- [Couler](https://github.com/couler-proj/couler) - biblioteka do komunikacji z API Argo

### Opis konfiguracji
![suu_env_conf drawio](https://github.com/SUU-Argo/.github/assets/46900653/65708f37-c412-4f7b-8d0c-fc4cf38f8fb8)



### Postępy prac

### Prezentacja Demo
