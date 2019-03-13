# Kuberntes Dashboard

## Get secret key/token to access dashboard

```
$ kubectl get secret -n kube-system | grep dashboard-token
dashboard-token-nmjkb                            kubernetes.io/service-account-token   3         136d
kubernetes-dashboard-token-hcfdj                 kubernetes.io/service-account-token   3         11m

```

```
$ kubectl describe secret dashboard-token-nmjkb -n kube-system
Name:         dashboard-token-nmjkb
Namespace:    kube-system
Labels:       <none>
Annotations:  kubernetes.io/service-account.name=dashboard
              kubernetes.io/service-account.uid=e13b1017-d9ea-11e8-868f-0209d40de7ee

Type:  kubernetes.io/service-account-token

Data
====
ca.crt:     1042 bytes
namespace:  11 bytes
token:      eyJhbGcifdsfggfdgdfgdfgdfgdfSUzI1NiIsImtpZCI6IiJ9.dsfdsdsfsdfdsfsdzt-jrblQYgTmfK_wUktkOfHfVmDxPQfCY_mSDP-WdYw2wU3t2FWxyaQ13j54kbAYw2_UUMeT2bHbP5k6ArwHtDl1Nxv_kN6zvyzlNGfJAtACSsdOqAJFZt90a9FVq_-guyFpwHFaeRQ0jdPdbKU3qBHu_7i2twmVlhOAHhCDp96dKRlzu56vsfRuLALFhGA2l-abnFxGumtPn9Vb34ifFRzJA-1BDX5ecnbHUJfUPh2jRPFIw8RUPAi8vHYV1vsJ8rdudBdvGBvJUtcauZtQfGKe3Zgylobdy3bXx59LlTAz3b_-tQX_f0KtFsDSp5emoVKT_IfOnT7nRHdPiQQnw

```

## URL to access 

http://api-url/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/#!/login