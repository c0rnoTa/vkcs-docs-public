## Kubernetes 1.22.6 <a id="v1-22-6"></a>

**Изменения в сервисе Kubernetes aaS:**

-   На узлах кластера используется операционная система [AlmaLinux](https://wiki.almalinux.org) версии 9.
-   По умолчанию устанавливается [limit range для пространств имен (namespace)](../../../k8s-node-groups/pods).

**Важные изменения в Kubernetes:**

-   Компонент PodSecurityPolicy заменен на [alpha-версию PodSecurity](https://github.com/kubernetes/enhancements/issues/2579).
-   Компонент [Memory Manager](https://github.com/kubernetes/enhancements/issues/1769) переведен в статус beta.
-   Добавлена новая функциональность [API Server Tracing](https://github.com/kubernetes/enhancements/issues/647). Эта функциональность находится в статусе alpha.
-   Добавлена новая функциональность [Generic data populators](https://github.com/kubernetes/enhancements/issues/1495) для постоянных томов (Persistent Volumes). Эта функциональность находится в статусе alpha.
-   Добавлена новая версия формата конфигурации для kubeadm: [v1beta3](https://github.com/kubernetes/enhancements/issues/970).
-   Теперь Kubernetes control plane всегда использует [CronJobs-контроллер версии 2](https://github.com/kubernetes/enhancements/issues/19).
-   Теперь все компоненты Kubernetes control plane на узлах (включая kubelet, kube-proxy и container runtime) [могут быть запущены от имени пользователей, которые не являются суперпользователями (non-root)](https://github.com/kubernetes/enhancements/issues/2033). Эта функциональность находится в статусе alpha.

Подробнее об этих и других изменениях см. в [официальной документации Kubernetes](https://kubernetes.io/blog/2021/08/04/kubernetes-1-22-release-announcement/), посвященной этому релизу.

## Kubernetes 1.21.4 <a id="v1-21-4"></a>

**Изменения в сервисе Kubernetes aaS:** на узлах кластера используется операционная система [AlmaLinux](https://wiki.almalinux.org) версии 8.

**Важные изменения в Kubernetes:**

-   Функциональность [CronJob](https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/) переведена в статус stable.
-   Добавлена поддержка неизменяемых (immutable) [Secret](https://kubernetes.io/docs/concepts/configuration/secret/#secret-immutable) and [ConfigMap](https://kubernetes.io/docs/concepts/configuration/configmap/#configmap-immutable).
-   Добавлена поддержка [IPv4/IPv6 Dual-Stack](https://kubernetes.io/docs/concepts/services-networking/dual-stack/).
-   Добавлена поддержка [Graceful Node Shutdown](https://kubernetes.io/docs/concepts/architecture/nodes/#graceful-node-shutdown).
-   Добавлена поддержка [PersistentVolume Health Monitor](https://kubernetes.io/docs/concepts/storage/volume-health-monitoring).
-   Упрощена процедура поддержки системы сборки Kubernetes.
-   Функциональность PodSecurityPolicy переведена в статус deprecated (устаревшая). Подробнее [здесь](https://kubernetes.io/blog/2021/04/06/podsecuritypolicy-deprecation-past-present-and-future).
-   Параметр topologyKeys для Service переведен в статус deprecated (устаревший).

Подробнее об этих и других изменениях см. в [официальной документации Kubernetes](https://kubernetes.io/blog/2021/04/08/kubernetes-1-21-release-announcement/), посвященной этому релизу.

## Kubernetes 1.20.4 <a id="v1-20-4"></a>

**Изменения в сервисе Kubernetes aaS:**

-   [Среда исполнения](https://kubernetes.io/docs/setup/production-environment/container-runtimes/) (runtime) кластера заменена на [CRI-O](https://cri-o.io/).
-   Изменен [формат хранения логов](../../../../../../additionals/cases/cases-logs/case-fluent-bit).

**Важные изменения в Kubernetes:**

-   Компонент среды исполнения [Dockershim](https://kubernetes.io/blog/2022/05/03/dockershim-historical-context/) переведен в статус deprecated (устаревший).
-   Функциональность [Volume Snapshot](https://kubernetes.io/docs/concepts/storage/volume-snapshots/) Operations переведена в статус stable.
-   Функциональность [API Priority and Fairness](https://kubernetes.io/docs/concepts/cluster-administration/flow-control/) (APF) теперь включена по умолчанию.
-   Команда `kubectl alpha debug` переведена в статус beta и становится `kubectl debug`. Подробнее [здесь](https://kubernetes.io/docs/tasks/debug/debug-application/debug-running-pod/).

Подробнее об этих и других изменениях см. в [официальной документации Kubernetes](https://kubernetes.io/blog/2020/12/08/kubernetes-1-20-release-announcement/), посвященной этому релизу.
