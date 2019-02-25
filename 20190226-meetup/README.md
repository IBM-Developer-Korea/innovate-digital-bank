# 2019.2.26 Meetup 자료

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

### support 서비스 생성

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
