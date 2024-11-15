* helm install wordpress --dry-run
* helm uninstall wordpress
* helm upgrade wordpress
* helm rollback wordpress
* helm pull bitnami/wordpress
* helm pull -- untar bitnami/wordpress
* helm install my-release ./wordpress
* helm install nginx-release bitnami/nginx -- version 7.1.0
* helm list
* helm history nginx-release
* helm lint
* helm template 'path to chart' --debug

Helm Objects:
* Release
* Chart
* Capabilities
* Values

Helm Functions:
* String Functions:
	* upper
	* quote
	* replace
	* shuffle