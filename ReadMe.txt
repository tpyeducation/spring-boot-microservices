export JAVA_HOME=/home/murali/.jdks/jbr_dcevm-11.0.16

 docker build -t  pmr27918791/cloud-gateway:MINI_KUBE -f Dockerfile .
 docker build -t  pmr27918791/config-server:MINI_KUBE -f Dockerfile .
 docker build -t  pmr27918791/order-service:MINI_KUBE -f Dockerfile .
 docker build -t  pmr27918791/payment-service:MINI_KUBE -f Dockerfile .
docker build -t  pmr27918791/product-service:MINI_KUBE -f Dockerfile .
docker build -t  pmr27918791/service-registry:MINI_KUBE -f Dockerfile .

docker push pmr27918791/cloud-gateway:MINI_KUBE && docker push pmr27918791/config-server:MINI_KUBE
 && docker push pmr27918791/order-service:MINI_KUBE && docker push pmr27918791/payment-service:MINI_KUBE && docker push pmr27918791/product-service:MINI_KUBE  && docker push pmr27918791/service-registry:MINI_KUBE


minikube service cloud-gateway-svc

POST - {URL}/product/
{
"name" : "iPhone",
 "price" : 100,
"long" : 10,

}

Video says:
p=name as productName (161 session)
{
"productName" : "iPhone",
 "productId" : 100,
"quantity" : 10,
"price" : 10,

}
