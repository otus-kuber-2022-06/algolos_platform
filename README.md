# algolos_platform
algolos Platform repository

Вывод команд:
```
$ kubectl get jobs:

NAME                         COMPLETIONS   DURATION   AGE
backup-mysql-instance-job    1/1           7s         3m31s
restore-mysql-instance-job   1/1           64s        2m20s
```
```
export MYSQLPOD=$(kubectl get pods -l app=mysql-instance -o jsonpath="{.items[*].metadata.name}")
kubectl exec -it $MYSQLPOD -- mysql -potuspassword -e "select * from test;" otus-database```

mysql: [Warning] Using a password on the command line interface can be insecure.
+----+-------------+
| id | name        |
+----+-------------+
|  1 | some data   |
|  2 | some data-2 |
+----+-------------+
```
