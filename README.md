# Specjalistyczne Platformy Programistyczne - Demo repo

## wykonano zadania na 5.0 

aby odpalić całość wystarczy komenda:
kubectl apply -f .

do sprawdzenia można posłużyć się komeną:
kubectl get all -n student-259257

PS C:\Users\piotr\OneDrive\Pulpit\SPP\devops-demo-pk> kubectl get all -n student-259257 
NAME                                       READY   STATUS    RESTARTS   AGE
pod/backend-deployment-5d7ccd8587-gfwjp    1/1     Running   0          43s
pod/backend-deployment-5d7ccd8587-h66fm    1/1     Running   0          44s
pod/frontend-deployment-54db568d5b-9b6bx   1/1     Running   0          43s
pod/frontend-deployment-54db568d5b-vskbf   1/1     Running   0          43s
pod/mongodb-0                              1/1     Running   0          43s
pod/mongodb-1                              1/1     Running   0          36s
pod/mongodb-2                              1/1     Running   0          33s

NAME                         TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)     AGE
service/backend-service      ClusterIP   10.110.243.221   <none>        80/TCP      43s
service/mongodb-headless     ClusterIP   None             <none>        27017/TCP   43s
service/mongodb-ro-service   ClusterIP   None             <none>        27017/TCP   43s
service/mongodb-rw-service   ClusterIP   None             <none>        27017/TCP   43s

NAME                                  READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/backend-deployment    2/2     2            2           44s
deployment.apps/frontend-deployment   2/2     2            2           44s

NAME                                             DESIRED   CURRENT   READY   AGE
replicaset.apps/backend-deployment-5d7ccd8587    2         2         2       44s
replicaset.apps/frontend-deployment-54db568d5b   2         2         2       44s

NAME                       READY   AGE
statefulset.apps/mongodb   3/3     43s

NAME                         SCHEDULE         SUSPEND   ACTIVE   LAST SCHEDULE   AGE
cronjob.batch/mongo-backup   30 */2 * * 1-5   False     0        <none>          43s
PS C:\Users\piotr\OneDrive\Pulpit\SPP\devops-demo-pk> kubectl get all -n student-259257