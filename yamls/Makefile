run:
	kubectl apply -f back-secret.yaml
	kubectl apply -f back-service.yaml
	kubectl apply -f back-deployment.yaml
	kubectl apply -f data-sc.yaml
	kubectl apply -f data-pvc.yaml
	kubectl apply -f data-secret.yaml
	kubectl apply -f data-service.yaml
	kubectl apply -f data-deployment.yaml
	kubectl apply -f front-service.yaml
	kubectl apply -f front-deployment.yaml

fill-db:
	kubectl apply -f data-script-secret.yaml
	kubectl apply -f data-script-deployment.yaml

stop:
	kubectl delete -f back-secret.yaml
	kubectl delete -f back-service.yaml
	kubectl delete -f back-deployment.yaml
	kubectl delete -f data-secret.yaml
	kubectl delete -f data-service.yaml
	kubectl delete -f data-deployment.yaml
	kubectl delete -f front-service.yaml
	kubectl delete -f front-deployment.yaml

clean: stop
	kubectl delete -f data-sc.yaml
	kubectl delete -f data-pvc.yaml

