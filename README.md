# My CIS-92 Project 

This repository has the starter code for CIS-92. 

This is my project.


# Configuration

### The variables from `config.yaml`

| Variable Name | Default Value | Description |
| --- | --- | --- |
| Port | 8000 | The port number used for the application |
| Student_Name | Luis | Name of the user |
| Site_Name | "*" | Name of the site |
| Debug | "1" | Debug is enabled |

### The variables from `secret.yaml`

| Variable Name | Default Value | Description |
| --- | --- | --- |
| SECRET_KEY | Abc123** | Text key to secure signed data |
| POSTGRES_USER | mysiteuser | PostgreSQL username |
| POSTGRES_PASSWORD | this-is-a-bad-password | PostgreSQL password |
| POSTGRES_DB | mysite | Name of PostgreSQL database |
| POSTGRES_DB_PASSWORD | this-is-a-bad-password | Password for PostgreSQL database |

## Database Postgres

### Primary Resources Requests

| Resource | Default Value | Description |
| --- | --- | --- |
| memory | 512Mi | Minimum memory |
| cpu | 500m | Minimum CPU |
| ephemeral-storage | 100Mi | Minimum storage |

<br/>
<br/>
<br/>





## Create your workspace!

cd **to desire directory**

##

git clone git@github.com:RadioKame/cis-92.git

## make sure your cluster is up and running ###

kubectl get all



## Start up commands
kubectl apply -f deployment/

## Initilize Database and set username password(we open a shell in the pod)
kubectl exec --stdin --tty pod/django-pod -- /bin/bash




## run in it:

python manage.py migrate

python manage.py createsuperuser

exit

If failing, basic troubleshoot is ok, just don't stress the system or try troubleshoot outside

# HELM and postgres testing

helm install postgres oci://registry-1.docker.io/bitnamicharts/postgresql --values values-postgres.yaml 

kubectl get all 

kubectl get pvc 

Install the Postgres Client
sudo apt install postgresql-client

kubectl port-forward service/postgres-postgresql 5432:5432 
on a new shell:

psql -h localhost -U mysiteuser mysite

### check the app using the external IP

:D

### password is already set up as "locust"

# clean up

helm uninstall postgres

kubectl delete pvc/data-postgres-postgresql-0


### Delete the Kubernetes pod (keep the bill low)
kubectl delete -f deployment/

### try

kubectl get all




This repository has the starter code for CIS-92. 

By: Luis Garcia




Author: Luis Garcia, CIS-92 starts now 02/14/24
