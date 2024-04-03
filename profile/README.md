# Środowiska Udostępniania Usług

## Temat projektu - Argo

### Autorzy

- Gabriel Kaźmierczak
- Dariusz Piwowarski
- Wojciech Przybytek
- Przemysław Roman

### Spis treści

1. [Podstawy teoretyczne](#podstawy-teoretyczne)
2. [Koncepcja Demo](#koncepcja-demo)
3. [Technologie realizacji Demo](#technologie-realizacji-demo)
4. [Opis konfiguracji](#opis-konfiguracji)
5. [Postępy prac](#postępy-prac)
6. [Prezentacja Demo](#prezentacja-demo)

### Podstawy teoretyczne

**[Kubernetes](https://kubernetes.io/)** to oprogramowanie open source służące do automatyzacji wdrażania, skalowania i
zarządzania aplikacjami kontenerowymi. Zostało zaprojektowane przez Google, a obecnie jest utrzymywane przez Cloud
Native Computing Foundation. Kubernetes dostarcza platformę do uruchamiania aplikacji w kontenerach na dużą skalę,
zarządzając infrastrukturą i zapewniając funkcje, takie jak self-healing (automatyczne restartowanie kontenerów),
odkrywanie usług i load balancing, przechowywanie danych, skalowanie i wiele innych.

[Argo](https://argoproj.github.io/) jest projektem open source, który dostarcza narzędzia do tworzenia, uruchamiania i
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

Oba narzędzia są zintegrowane z Kubernetes i wykorzystują jego funkcje, takie jak API, schematy autoryzacji i mechanizmy
skalowania. Dzięki temu są one naturalnym rozszerzeniem ekosystemu Kubernetes i mogą być łatwo zintegrowane z innymi
narzędziami w tym ekosystemie.

### Koncepcja Demo

### Technologie realizacji Demo

### Opis konfiguracji

### Postępy prac

### Prezentacja Demo