

1. Flaky tests
    - https://dl.acm.org/doi/fullHtml/10.1145/3476105
    - https://www.youtube.com/watch?v=NcjS8HBZL_M
    - https://dhiller.dev/presentation.html 
    - mfeathers article
    - ...

2. Basic everyday tools!
    - fzf
    - yazi
    - ghostty

3. Refactor with IDE ;) 

4. Concurrent / Parallel / Structured?

5. k8s: autoscaling! - "Skalowanie aplikacji Java w Kubernetes" – automatyczne skalowanie aplikacji w oparciu o zasoby, konfiguracja Horizontal Pod Autoscaler i Load Balancing.

6. "Użycie Kubernetes Operatorów dla aplikacji Java" – jak tworzyć i korzystać z Kubernetes Operatorów w celu zarządzania cyklem życia złożonych aplikacji Java w środowiskach chmurowych.

7. Security by Design - together with - DOP (Data oriented programming) -> show some nice demo, based on the two presentations and Nicolai - https://www.youtube.com/watch?v=miUbs3mqPJE

8. Wheel of misfortune



Rozwinięcie:

Rozwinięcie tematu nr 3: "Skalowanie aplikacji Java w Kubernetes"
W tym temacie omówimy, jak skalować aplikacje Java wdrożone w klastrze Kubernetes. Skalowanie jest kluczowym elementem umożliwiającym dynamiczne dostosowanie zasobów aplikacji do zmiennego obciążenia, zapewniając optymalną wydajność i efektywne wykorzystanie zasobów.

Główne zagadnienia:
Podstawy skalowania w Kubernetes:

Co to są Pody i jak działają jako podstawowe jednostki w Kubernetes.
Replikacja: Jak działają Deploymenty i ReplicaSet w Kubernetes do automatycznego skalowania liczby Podów w zależności od wymagań aplikacji.
Różnica między skalowaniem poziomym (dodawanie/redukcja Podów) a skalowaniem pionowym (zmiana zasobów przypisanych jednemu Podowi).
Horizontal Pod Autoscaler (HPA):

Jak konfigurować HPA w Kubernetes, aby automatycznie dostosowywał liczbę Podów w odpowiedzi na obciążenie.
Metryki CPU i pamięci: Jak Kubernetes wykorzystuje te metryki do skalowania aplikacji.
Przykład konfiguracji HPA dla aplikacji Java, np. wykorzystując „kubectl autoscale” oraz pliki YAML z limitami zasobów.
Cluster Autoscaler:

Jak Cluster Autoscaler może dodawać nowe węzły do klastra, gdy potrzeba więcej zasobów, lub usuwać węzły, gdy są one nieużywane.
Związek między HPA a Cluster Autoscaler w kontekście skalowania aplikacji Java.
Load Balancing:

Rola load balancerów w Kubernetes. Jak Kubernetes automatycznie równoważy ruch do Podów przy pomocy Service.
Liveness i Readiness Probes – jak pomagają w zdrowym zarządzaniu Podami i w decydowaniu, które Pody są gotowe do obsługi ruchu.
Ustawienia zasobów CPU i pamięci:

Jak ustawiać requests i limits dla zasobów w aplikacjach Java, aby uniknąć nadmiernego przydziału lub niedoboru zasobów.
Przykłady ustawień dla aplikacji Spring Boot wdrożonej w klastrze Kubernetes.
Skalowanie aplikacji stanowiskowych:

Różnice w podejściu do skalowania aplikacji stanowiskowych, takich jak bazy danych czy usługi oparte na stanach, z użyciem StatefulSets.
Zaawansowane metryki do skalowania:

Jak integrować dodatkowe metryki, takie jak liczba żądań HTTP, czas odpowiedzi lub niestandardowe metryki z narzędziami monitorującymi (np. Prometheus) do bardziej zaawansowanego skalowania.
Przykładowe narzędzia i technologie:
Prometheus i Grafana – do monitorowania stanu aplikacji i podejmowania decyzji o skalowaniu.
Spring Boot Actuator – do zbierania niestandardowych metryk z aplikacji Java.
Kubernetes Metrics Server – aby dostarczać metryki używane przez HPA.


--

Rozwinięcie tematu nr 9: "Użycie Kubernetes Operatorów dla aplikacji Java"
Operatorzy Kubernetes to zaawansowany mechanizm automatyzacji, który umożliwia zarządzanie cyklem życia złożonych aplikacji, takich jak aplikacje Java, w środowiskach Kubernetes. W tej prezentacji skoncentrujemy się na tym, jak tworzyć, używać i zarządzać Operatorami Kubernetes dla aplikacji Java.

Główne zagadnienia:
Czym jest Kubernetes Operator?:

Wprowadzenie do Operatorów: rozszerzenia API Kubernetes, które pozwalają na zarządzanie skomplikowanymi aplikacjami w Kubernetes w sposób zautomatyzowany.
Operator Pattern – w jaki sposób Operatorzy umożliwiają automatyzację zadań, takich jak instalacja, aktualizacja, backup i monitoring aplikacji.
Rola Custom Resource Definitions (CRD), które umożliwiają definiowanie niestandardowych zasobów aplikacji Java.
Dlaczego warto używać Operatorów?:

Automatyzacja codziennych zadań operacyjnych: na przykład zarządzanie cyklem życia aplikacji Java (np. mikroserwisów lub baz danych).
Umożliwienie prostego zarządzania złożonymi zależnościami między usługami (np. aplikacjami składającymi się z wielu komponentów Java, baz danych, cache itp.).
Przykład tworzenia Operatora dla aplikacji Java:

Praktyczny przykład: tworzenie prostego Operatora Kubernetes dla aplikacji Java przy użyciu frameworku Java Operator SDK.
Struktura projektu Operatora – Controller i Custom Resource.
Implementacja logiki kontrolera: zarządzanie cyklem życia aplikacji Java (np. wdrażanie nowej wersji aplikacji w odpowiedzi na zmiany CRD).
Jak operator może monitorować stan aplikacji Java (np. używając Prometheus).
Użycie istniejących Operatorów:

Przykłady gotowych Operatorów dla aplikacji Java, takich jak Strimzi Kafka Operator (dla Kafka) lub PostgreSQL Operator dla baz danych wykorzystywanych przez aplikacje Java.
Integracja aplikacji Java z Operatorami do zarządzania komponentami infrastruktury.
Cykl życia Operatora:

Automatyzacja wdrożeń i aktualizacji aplikacji Java.
Wsparcie dla Canary Deployments i Blue/Green Deployments – jak Operator może zarządzać bezpiecznymi aktualizacjami aplikacji.
Rollback – jak Operator może zautomatyzować przywracanie poprzednich wersji aplikacji w przypadku awarii.
Zarządzanie zasobami w aplikacjach Java przy pomocy Operatorów:

Jak Operatorzy mogą dynamicznie zarządzać zasobami (np. skalowanie w oparciu o niestandardowe metryki lub zarządzanie stanem aplikacji).
Zarządzanie backupami i disaster recovery dla aplikacji Java.
Bezpieczeństwo Operatorów:

Jak Operatorzy mogą obsługiwać polityki bezpieczeństwa dla aplikacji Java, takie jak aktualizacje certyfikatów SSL, zarządzanie tajemnicami (Secrets) i politykami RBAC.
Przykładowe narzędzia i technologie:
Java Operator SDK – biblioteka ułatwiająca tworzenie Operatorów w Javie.
Kubernetes Client Java – do komunikacji z API Kubernetes z aplikacji Java.
Helm – współpraca Operatorów z Helm do zarządzania skomplikowanymi wdrożeniami.
