
deploy:
	@echo "🚀 Deploying Kubernetes PostgreSQL + Web Server setup..."
	kubectl apply -f 01-secret.yaml
	kubectl apply -f 02-configmap.yaml
	kubectl apply -f 07-init-sql-configmap.yaml
	kubectl apply -f 03-pvc.yaml
	kubectl apply -f 04-postgres.yaml
	kubectl apply -f 05-postgres-service.yaml
	kubectl apply -f 06-web-content-configmap.yaml
	kubectl apply -f 08-webserver-service.yaml
	kubectl apply -f 11-data-source-pvc.yaml
	kubectl apply -f 10-data-source.yaml
	kubectl wait --for=condition=Ready pod/data-source
	kubectl cp music/. data-source:/songs/
	kubectl apply -f 09-webserver-deployment.yaml
	kubectl apply -f 12-hpa.yaml
	@echo "✅ Deployment complete."

steak:
	@echo "🧹 Cleaning up Kubernetes PostgreSQL + Web Server setup..."
	-kubectl delete -f 12-hpa.yaml
	-kubectl delete -f 10-data-source.yaml
	-kubectl delete -f 11-data-source-pvc.yaml
	-kubectl delete -f 09-webserver-deployment.yaml
	-kubectl delete -f 08-webserver-service.yaml
	-kubectl delete -f 06-web-content-configmap.yaml
	-kubectl delete -f 05-postgres-service.yaml
	-kubectl delete -f 04-postgres.yaml
	-kubectl delete -f 03-pvc.yaml
	-kubectl delete -f init-sql-configmap.yaml
	-kubectl delete -f 02-configmap.yaml
	-kubectl delete -f 01-secret.yaml
	@echo "✅ Cleanup complete."
