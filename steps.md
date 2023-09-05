## Clone the application

    git clone https://github.com/LondheShubham153/microservices-k8s.git
    

## login to docker 

    docker login


## Build ,tag and push image

    docker build . -t mnmanish/taskmaster && docker push mnmanish/taskmaster



## Create deployment file for application

    vim taskmaster.yaml

  <img width="339" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/171c6597-8b3c-416c-b0e6-cf463c3b8e1f">


## Create service file for application

    vim taskmaster-svc.yaml

  <img width="339" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/0c59ba6e-4333-4550-b1fa-63e8fe776551">



## Create mongo persistent volume

    vim mongo-pv.yaml

  <img width="305" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/0cbbe8ad-df10-4a87-a560-0384fa5e40b4">


## Create mongo persistent volume claim

    vim mongo-pvc.yaml

  <img width="276" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/b3a4511d-e64e-4ec8-9a1e-fc948fcb0c3f">


## Create mongo deployment file

    vim mongo.yaml

  <img width="388" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/cf113cf9-d232-4bb2-a0fc-8e20c3124c57">


## Create mongo service file

    vim mongo-svc.yaml

  <img width="248" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/2b1daf67-8be0-4500-824d-2e87a018c0d5">


## Apply taskmaster.yaml 

    kubectl apply -f taskmaster.yaml

  <img width="604" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/9968a3fd-a9b9-4112-b31a-01a05582cfbc">


## Apply taskmaster-svc.yaml

    kubectl apply -f taskmaster-svc.yaml

  <img width="600" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/13017d1f-8a2e-4dbe-aebd-76b511e593bf">


## Apply mongo-pv.yaml

    kubectl apply -f mongo-pv.yaml



  ## Apply mongo-pvc.yaml

      kubectl apply -f mongo-pvc.yaml


  ## Apply mongo.yaml

      kubectl apply -f mongo.yaml


  ## Apply mongo-svc.yaml

      kubectl apply -f mongo-pvc.yaml
 
 <img width="598" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/06c413cd-09ad-440e-8bc6-5a36db40c741">



  ## Now, on the worker node, check docker container of mongo and taskmaster is running

      docker ps 

  <img width="601" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/5aff9d83-138e-411c-8d76-22d189cd10c2">

<img width="603" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/ff96a932-f917-41b3-8666-c9c8a204982f">


## Now, edit the security groups.

<img width="603" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/24347cec-c308-49fc-b40e-7a11dfb7bfb9">


## Application is running on worker node

<img width="587" alt="image" src="https://github.com/ManishNegi963/K8s-Microservice-with-flask-app/assets/124788172/2be2e36c-4940-41b3-9265-4ca92f74f0fa">



    
