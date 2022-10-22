
# build
build:
	@docker build -t williameliasalves/conversao-temperatura:desafio2 conversao-temperatura/src
run:

#target push: push image to dockerhub
push:
	@docker push  williameliasalves/conversao-temperatura:desafio2
	@docker push  williameliasalves/conversao-temperatura:latest
#target apply: apply deployment kubernets
apply:
	@kubectl apply -f ./k8s/conversor.deployment.yml
	@kubectl apply -f ./k8s/conversor.service.yml
#target forward: execute a por-forward kubectl that point service port to localhost:8080
forward:
	@kubectl port-forward service/conversor-svc 8000:8000