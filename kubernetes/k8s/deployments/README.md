# ingress-nginx-deamon.yaml is a daemon from Ingress-Nginx is setted up for provide secure and non-secure access on port 80,443
#
# dashboard-resource-ssl.yaml is a example of expose a service via Ingress-Nginx to the world. 
#
# metallb.yaml is a additional component which provide you a option to have a L2 loadbalancer as in AKS on your baremetal
#	* I use a version 1.10 because newer neither older version doesn't work for me.
#	* https://metallb.universe.tf





########################### Section of dashboard-resource-ssl.yaml ###########################
###          serviceName: kubernetes-dashboard - here is a name of service witch you want to expose
###          servicePort: 80 - here is a port number on which service listen
######### 
### if you want non-secure access from world. You can remove this lines
###   tls:
###    - hosts:
###      - pvkbboard01.mydomain.com
###      secretName: dashboard-cert
###
####### and of course this line
###   annotations:
###    cert-manager.io/cluster-issuer: "mycustom-issuer"
