
# "Skalowanie aplikacji Java w Kubernetes" 

W tym temacie omówimy, jak skalować aplikacje Java wdrożone w klastrze Kubernetes. Skalowanie jest kluczowym elementem umożliwiającym dynamiczne dostosowanie zasobów aplikacji do zmiennego obciążenia, zapewniając optymalną wydajność i efektywne wykorzystanie zasobów.

## Główne zagadnienia: Podstawy skalowania w Kubernetes:

Co to są Pody i jak działają jako podstawowe jednostki w Kubernetes. Replikacja: Jak działają Deploymenty i ReplicaSet w Kubernetes do automatycznego skalowania liczby Podów w zależności od wymagań aplikacji. Różnica między skalowaniem poziomym (dodawanie/redukcja Podów) a skalowaniem pionowym (zmiana zasobów przypisanych jednemu Podowi). Horizontal Pod Autoscaler (HPA):

Jak konfigurować HPA w Kubernetes, aby automatycznie dostosowywał liczbę Podów w odpowiedzi na obciążenie. Metryki CPU i pamięci: Jak Kubernetes wykorzystuje te metryki do skalowania aplikacji. Przykład konfiguracji HPA dla aplikacji Java, np. wykorzystując „kubectl autoscale” oraz pliki YAML z limitami zasobów. Cluster Autoscaler:

Jak Cluster Autoscaler może dodawać nowe węzły do klastra, gdy potrzeba więcej zasobów, lub usuwać węzły, gdy są one nieużywane. Związek między HPA a Cluster Autoscaler w kontekście skalowania aplikacji Java. Load Balancing:

Rola load balancerów w Kubernetes. Jak Kubernetes automatycznie równoważy ruch do Podów przy pomocy Service. Liveness i Readiness Probes – jak pomagają w zdrowym zarządzaniu Podami i w decydowaniu, które Pody są gotowe do obsługi ruchu. Ustawienia zasobów CPU i pamięci:

Jak ustawiać requests i limits dla zasobów w aplikacjach Java, aby uniknąć nadmiernego przydziału lub niedoboru zasobów. Przykłady ustawień dla aplikacji Spring Boot wdrożonej w klastrze Kubernetes. Skalowanie aplikacji stanowiskowych:

Różnice w podejściu do skalowania aplikacji stanowiskowych, takich jak bazy danych czy usługi oparte na stanach, z użyciem StatefulSets. Zaawansowane metryki do skalowania:

Jak integrować dodatkowe metryki, takie jak liczba żądań HTTP, czas odpowiedzi lub niestandardowe metryki z narzędziami monitorującymi (np. Prometheus) do bardziej zaawansowanego skalowania. Przykładowe narzędzia i technologie: Prometheus i Grafana – do monitorowania stanu aplikacji i podejmowania decyzji o skalowaniu. Spring Boot Actuator – do zbierania niestandardowych metryk z aplikacji Java. Kubernetes Metrics Server – aby dostarczać metryki używane przez HPA.

## References
- replicas: 
 https://github.com/kubernetes/kubernetes/blob/cdfabdc86e1417dafe5a3202eb8c0a0360af29fe/pkg/controller/podautoscaler/replica_calculator.go#L95
- hpa:
 https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/