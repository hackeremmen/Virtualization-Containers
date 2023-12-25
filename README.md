# Virtualization-Containers
TryHackMe - Virtualization and Containers


Task 2  What is Virtualization
==============================

Bəs virtuallaşdırma niyə lazımdır? Əksər təşkilatlar və fərdlər üçün virtuallaşdırma aşağıdakılara ehtiyacdan irəli gəlir:


Xərcləri azaldın: Fiziki serverlər bahalı ola bilər və virtuallaşdırma serverlərin və ya digər avadanlıqların sayını azalda və ya hətta fiziki avadanlıqları şirkətin infrastrukturundan tamamilə silə bilər.
Məqsəd: Düzgün tətbiq edilmədən DevOps, şirkət üçün resursları aşağıdakı kimi miqyaslaşdırmaq çətin ola bilər. server istifadəsi artır. Virtuallaşdırma bu prosesi asanlaşdırır və istifadəyə əsasən serverin resurslarını virtual maşınlara həvalə edə bilər.
Effektivlik: Məqsədləşmə kimi, virtuallaşdırma da azaldılmış istifadə olduqda virtual maşına ayrılan resursları azaltmağı asanlaşdıra bilər.

Decrease expenses: Fiziki serverlər bahalı ola bilər və virtuallaşdırma serverlərin və ya digər avadanlıqların sayını azalda və ya hətta fiziki avadanlıqları şirkətin infrastrukturundan tamamilə silə bilər.
Scale: Məqsəd: Düzgün tətbiq edilmədən DevOps, şirkət üçün resursları aşağıdakı kimi miqyaslaşdırmaq çətin ola bilər. server istifadəsi artır. Virtuallaşdırma bu prosesi asanlaşdırır və istifadəyə əsasən serverin resurslarını virtual maşınlara həvalə edə bilər.
Efficiency: Effektivlik: Məqsədləşmə kimi, virtuallaşdırma da azaldılmış istifadə olduqda virtual maşına ayrılan resursları azaltmağı asanlaşdıra bilər.



Virtualization Technology
-------------------------

Bu nöqtədə virtuallaşdırmanın necə mümkün olduğunu soruşa bilərsiniz; Bu mürəkkəb sual olsa da, bu otaqda biz müxtəlif texnologiyaları və platformaları parçalayacağıq, onların əsas host əməliyyat sistemi ilə necə qarşılıqlı əlaqədə olduğuna qısaca baxacağıq.

Yuxarıdakı suala cavab vermək üçün virtuallaşdırmanın tərifini genişləndirməliyik. Formal olaraq, virtuallaşdırma kompüter avadanlığı üzərində abstraksiya qatını abstraksiya edir və ya yaradır. Abstraksiya təbəqəsi bir cihazı virtual maşınlar (VM) kimi də tanınan çoxsaylı virtual kompüterlərə bölməyə imkan verir.

Daha sadə dillə desək, bu o deməkdir ki, virtual maşının məntiqi resurslara <-dən uzaqlaşdırılan girişi olacaq. a i=3>fiziki resurslar.

Virtualization Structure
------------------------

Virtuallaşdırma mühərrik-maşın formatından istifadə etməklə həyata keçirilir, bu o deməkdir ki, proqram və ya sistem abstraksiya qatı yaradır və resursları ayırır, əməliyyat sistemi və ya proqram isə bu virtuallaşdırılmış mühitin üzərinə quraşdırıla bilər. Virtual maşında quraşdırılmış əməliyyat sistemi -dən fərqli olaraq qonaq OS kimi tanınır. Virtualizasiya mühərrikinin işlədiyi  .ƏShost


Is scalability a primary benefit of virtualization? (Y/N)
Answer: Yes

What is the operating system of a virtual machine often referred to as?
Answer: guest OS



Task 3  Hypervisors
===================

Əvvəlki tapşırıqda biz virtuallaşdırma anlayışını yüksək səviyyədə təqdim etdik və virtuallaşdırmanın strukturunu qısaca müzakirə etdik. Bu tapşırıqda biz ilk virtuallaşdırma mühərrikimizi təqdim edəcəyik: hipervizorlar.

Hipervizor aparat və proqram təminatı arasında abstraksiya qatını yaratmaq imkanı verir. Bir hipervizor, həmçinin virtual maşınlar yaratmaq və ya yükləmək üçün son istifadəçi ilə abstraksiya təbəqəsi arasında interfeys təmin etmək üçün ümumiyyətlə idarəetmə tətbiqi və ya proqram təminatının bəzi formasını ehtiva edəcəkdir.

Hipervisorlar aparata nisbətən mövqelərinə görə təyin olunan iki kateqoriyaya bölünür. Onlar ya hipervizor olan avadanlığın üstündə birbaşa yüngül əməliyyat sistemi yarada, ya da əvvəlcədən mövcud olan əməliyyat sisteminin üzərinə tətbiq kimi hipervizor əlavə edə bilərlər.


Type 1 Hypervisors
------------------

1-ci tip hipervizorlar, həmçinin çılpaq metal hipervizorlar kimi tanınır, birbaşa aparat arasında abstraksiya qatı yaradır. və onların arasında ümumi əməliyyat sistemi olmayan virtual maşınlar. Bunun əvəzinə, hipervizor əməliyyat sistemidir və çox vaxt başsız olur, yalnız uzaqdan əldə edilən veb əsaslı idarəetmə portalı var. Bu hipervizorlar miqyas üçün və eyni anda çoxlu sayda virtual maşını yerləşdirmək üçün nəzərdə tutulmuşdur. Ən çox resursları virtual maşınlara həsr etmək üçün onlar olduqca yüngüldür. Aşağıda tip 1 hipervizor arxitekturasının diaqramı verilmişdir.


Type 2 Hypervisors
------------------

2-ci tip hipervizorlar, həmçinin hostlaşdırılmış hipervizorlar kimi tanınır, proqram tətbiqindən abstraksiya qatı yaradır. əvvəlcədən mövcud olan əməliyyat sisteminin üzərində qurulmuşdur. 1-ci tip hipervizorlardan fərqli olaraq, tip 2 hipervizorlar çox vaxt GUI vasitəsilə birbaşa proqramdan idarə olunur. Bu hipervizorlar çox vaxt son istifadəçilər və ya tərtibatçılar kimi fərdlər üçün nəzərdə tutulub və ciddi şəkildə miqyasda çoxlu sayda virtual maşını işə salmaq üçün nəzərdə tutulmayıb. Aşağıda tip 2 hipervizor arxitekturasının diaqramı verilmişdir.


What type of hypervisor is VirtualBox considered?
Answer: type 2

What are type 1 hypervisors also known as?
Answer: bare metal hypervisor



Task 4  Containers
==================

Hipervizorlar çoxlu sayda istifadə halları üçün gözlənildiyi kimi işləyir, lakin yüngül tətbiqləri miqyaslandırarkən problemlərlə qarşılaşmağa başlayır. Mikroservislər bizə hipervizordan yerləşdirildikdə problemlərlə qarşılaşan proqram arxitekturasının yaxşı nümunəsini verir. Mikroservis miqyaslana bilən və yüngül protokol və funksiyalardan istifadə edən daha kiçik xidmətlərə bölünən proqram strukturudur. Arxitekturanın yüngül təbiəti hər biri yüksək resurs istifadə edən çoxlu sayda virtual maşın tələb edən hipervizorlar üçün aşkar problemlər yaradır.


Containers - miqyasda hipervizorlarla qarşılaşılan problemlərin cari həllidir.

What are Containers
-------------------



Konteynerlərin virtual maşınlarla çoxlu ortaq cəhətləri var, lakin ana əməliyyat sistemindən tamamilə mücərrəd olmaq əvəzinə, konteynerlər bəzi xassələri host əməliyyat sistemi ilə bölüşürlər. Konteynerlərin öz fayl sistemi, hesablama resurslarının bir hissəsi (CPU, RAM), proses sahəsi və s. 

Yüngül olmağın aşkar üstünlükləri ilə yanaşı, konteynerlər həm də portativ və sağlamdır çünki onlar tam mücərrəd deyillər. 

Konteyner mühərrikləri virtuallaşdırmanın ikinci növüdür. Virtual maşınlar virtuallaşdırma üçün abstraksiya qatı yaratmaq üçün hipervizordan istifadə etdiyi kimi, konteynerlər də məntiqi resurslardan istifadə edərək abstraksiya qatı yaratmaq üçün konteyner mühərrikindən istifadə edir.


Are containers completely abstracted from the host operating system? (Y/N)
Answer: N


Task 5  Docker
==============

Kimsə konteynerlərlə tanışdırsa, ağıla ilk gələn ad Docker ola bilər. Docker, Docker "şəkilləri" işlətmək üçün istifadə edilən konteyner platforması və mühərrikidir. qablar kimi.

Hər bir Docker təsviri konteynerlərdə istifadə üçün xüsusi olaraq qurulmuş və yüngül olan Alp və ya Ubuntu kimi əsas təsvirdən qurulmuşdur. Docker təsvirini yaratmaq üçün konteynerin əsas təsvirini və icra ediləcək hər hansı əmrləri təyin edən Dockerfile yaradılmalıdır.

Docker haqqında ətraflı məlumat üçün Docker-a Giriş otağına baxın.

https://tryhackme.com/room/introtodockerk8pdqk



What flag is obtained at 10.10.189.207:5000 after running the container?
$ curl 10.10.189.207:5000
curl: (7) Failed to connect to 10.10.189.207 port 5000: Connection refused
$ docker images
REPOSITORY                 TAG       IMAGE ID       CREATED         SIZE
cryillic/thm_example_app   latest    9a03ff5b0fbb   10 months ago   59.6MB
$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
$ docker run -p 5000:5000 -d cryillic/thm_example_app 
e0b79ee3e7010c2cfcb025afec1efb9978f5d04d87a32e3c64f5312330492116
$ curl http://10.10.189.207:5000/
<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Flask Docker</title>
</head>
<body>
    <center><h1>THM{this_is_running_in_docker}</h1></center>
</body>
</html>$ 
Answer: THM{this_is_running_in_docker}



Task 6  Kubernetes
==================

Hipervizorların və konteynerlərin istifadəsi ilə qiymət və . Bu hələ də sualı tərk edir, əgər bizə daha sürətli və daha genişlənə bilən bir həll lazımdırsa necə? Yəni, yüklənmə və ya digər meyarlar dəyişdikcə, tətbiqə və ya xidmətə ayrılan resurslar və ya nümunələrin sayı ehtiyac olduqda tez artır və ya azalır.

Kubernetes, həmçinin "K8s kimi qısaldılmış," orkestr platforması kimi tanınan belə bir həlldir. Orkestr platforması Docker kimi digər məhsullara inteqrasiya etmək və onların imkanlarını genişləndirmək və ya "sinxronlaşdırmaq" onları digər məhsullar və ya proqramlar ilə.

Kubernetes hipervizorlar və konteynerlər kimi bu ənənəvi virtuallaşdırma modellərinə əsaslanır və onların istifadəsini, xüsusiyyətlərini və imkanlarını genişləndirir.

Bu imkanlara və xüsusiyyətlərə aşağıdakılar daxildir:

Horizontal scaling: Unlike traditional "vertical" scaling, "horizontal" scaling refers to adding devices or machines to handle increased workload, rather than adding logic resources such as CPU or RAM.
Extensibility: Clusters can be modified dynamically without affecting containers outside of the intended group.
Self-healing: K8s can automatically restart, replace, reschedule, and kill containers that are not properly functioning based on user-defined health checks.
Automated rollouts and rollbacks: K8s can progressively roll out changes to containers. As changes are made, it will monitor the application's health and decide whether to continue the rollout or rollback. This ensures the constant uptime of your cluster even if some containers fail.


Hands-On Application
--------------------

K8-lərlə praktiki təcrübə əldə etmək üçün sizə kubectl ilə konfiqurasiya edilmiş əvvəlcədən yerləşdirilmiş klasterə giriş imkanı verdik. Kubernetes əsas avtomatlaşdırmanın əksəriyyətini defolt olaraq təmin etdiyi üçün K8-lər və ənənəvi virtuallaşdırma platforması arasındakı fərqləri təkbaşına araşdırmanızı istəyirik. Bununla belə, Kubernetes geniş xüsusiyyətlərin siyahısı olan böyük bir platformadır. Sizi DevOps və K8-lərin xüsusiyyətlərini araşdırmağa davam etməyi tövsiyə edirik, çünki biz sizə Kubernetes klasterini kəşf etməyə başlamaq üçün yalnız əsas suallar toplusunu təqdim edəcəyik. .

Klasterə daxil olmaq üçün yaşıl düyməni basaraq bu tapşırığa əlavə edilmiş virtual maşını yerləşdirinMaşını işə salındüyməsinə. Zəhmət olmasa maşının işə salınmasına 3-5 dəqiqə vaxt verin. Maşın bölünmüş görünüşdə başlayacaq; maşın görünməzsə, bu otağın yuxarı sağında yerləşən maviBölünmüş Görünüşü Göstər düyməsinə klikləyə bilərsiniz. Alternativ olaraq, aşağıda verilmiş etimadnamələrdən istifadə edərək SSH ilə maşına daxil ola bilərsiniz.   

Maşın IP: 10.10.4.214 İstifadəçi adı: thmuser Parol: TryHackMe!

Kubectl-dən istifadə etməkdə sizə kömək etmək üçün burada tapılan onlayn istinaddan istifadə edə bilərsiniz. Suallara cavab verərkən sizə istiqamət vermək üçün göstərişlərdən istifadə etməyi tövsiyə edirik.


https://kubernetes.io/docs/reference/kubectl/quick-reference/

$ minikube start

How many pods are running on the provided cluster?
$ kubectl get pods
NAME                              READY   STATUS    RESTARTS      AGE
hello-tryhackme-f79f667fd-lh87b   1/1     Running   1 (86s ago)   227d
Answer: 1


How many system pods are running on the provided cluster?
$ kubectl get pods -A
NAMESPACE     NAME                               READY   STATUS    RESTARTS      AGE
default       hello-tryhackme-f79f667fd-lh87b    1/1     Running   1 (94s ago)   227d
kube-system   coredns-787d4945fb-wqxqr           0/1     Running   1 (94s ago)   227d
kube-system   etcd-minikube                      1/1     Running   1 (94s ago)   227d
kube-system   kube-apiserver-minikube            1/1     Running   1 (94s ago)   227d
kube-system   kube-controller-manager-minikube   1/1     Running   1 (94s ago)   227d
kube-system   kube-proxy-sqwx6                   1/1     Running   1 (94s ago)   227d
kube-system   kube-scheduler-minikube            1/1     Running   1 (94s ago)   227d
kube-system   storage-provisioner                1/1     Running   2 (94s ago)   227d
Answer: 7

What is the pod name on the provided cluster?
Answer: hello-tryhackme-f79f667fd-lh87b

What is the deployment name on the provided cluster?
$ kubectl get deployments                               
NAME              READY   UP-TO-DATE   AVAILABLE   AGE
hello-tryhackme   1/1     1            1           227d
Answer: hello-tryhackme


What port is exposed by the service in question 5?
$ $ kubectl get services

NAME              TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE
hello-tryhackme   NodePort    10.109.213.246   <none>        8080:31449/TCP   227d
kubernetes        ClusterIP   10.96.0.1        <none>        443/TCP          227d
Answer: 8080


How many replica sets are deployed on the provided cluster?
$ kubectl get rs
Answer: 1



What is the replica set name on the provided cluster?
$ kubectl get rs
NAME                        DESIRED   CURRENT   READY   AGE
hello-tryhackme-f79f667fd   1         1         1       227d


What command would be used to delete the deployment from question 5?
$ kubectl delete deployment alpine-dev -n=development
$ kubectl delete deployment hello-tryhackme
deployment.apps "hello-tryhackme" deleted
