For creating config map for custom index.html
  kubectl create configmap nginx-index-html-configmap --from-file=index.html (index.html is attached)

For deployment of nginx web service 
   kubectl apply -f nginxdeployment.yaml (its attached)

Please note: nginxdeployment.yaml  -- It contains rolling strategy, memory limits configurations 


For creation of SSL certificate and import it:

   openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout mykey -out mycert -subj "/CN=test/O=test

    kubectl create secret tls mycert --key mykey --cert mycert

For setting up of auto scaling based on CPU utilization

  kubectl autoscale deployment nginx-deployment --min=2 --max=5 --cpu-percent=8