# 2019.2.26 Meetup 자료

## Kubernetes Cluster Public IP 확인하기

``` bash
ibmcloud cs workers <YOUR CLUSTER NAME>
```

* `bank/yaml/configmap.yaml` 파일의 `basePath` 항목에 Public IP를 입력.
* `bank/helm/innovate-bank/values.yaml` 파일의 `basePath` 항목에 Public IP를 입력.

## kubectl을 이용하여 생성하기

### MongoDB 생성

``` bash
kubectl create -f mongodb/yaml
```

### ConfigMap 생성

``` bash
kubectl create -f bank/yaml/configmap.yaml
```

### Accounts 서비스 생성

``` bash
kubectl create -f bank/yaml/accounts
```
### Authentication 서비스 생성

``` bash
kubectl create -f bank/yaml/authentication
```

### Bills 서비스 생성

``` bash
kubectl create -f bank/yaml/bills
```

### Portal 서비스 생성

``` bash
kubectl create -f bank/yaml/portal
```

### Support 서비스 생성

``` bash
kubectl create -f bank/yaml/support
```

### Transactions 서비스 생성

``` bash
kubectl create -f bank/yaml/transactions
```

### Userbase 서비스 생성

``` bash
kubectl create -f bank/yaml/userbase
```

### 삭제

``` bash
kubectl delete -f bank/yaml/accounts
kubectl delete -f bank/yaml/authentication
kubectl delete -f bank/yaml/bills
kubectl delete -f bank/yaml/portal
kubectl delete -f bank/yaml/support
kubectl delete -f bank/yaml/transactions
kubectl delete -f bank/yaml/userbase
```

``` bash
kubectl delete -f mongodb/yaml
```

``` bash
kubectl delete -f bank/yaml/configmap.yaml
```

## Helm을 이용하여 생성하기

### MongoDB 생성

``` bash
helm install --name test-db ./mongodb/helm/mongodb
```

### Bank 서비스 생성

``` bash
helm install --name test-svc ./bank/helm/innovate-bank
```

### 삭제

``` bash
helm delete --purge test-db
helm delete --purge test-svc
```

## Helm 차트 만들기 

### 기본 템플릿 생성

``` bash
cd mongodb/helm
helm create mongodb
```

### Dry Run

``` bash
helm install --dry-run --debug ./mongodb/helm/mongodb
```