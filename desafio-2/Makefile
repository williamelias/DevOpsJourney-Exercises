
### Part 1 - Conversor

# build
build_conversor:
	@docker build -t williameliasalves/conversao-temperatura:desafio2 conversao-temperatura/src

#target push: push image to dockerhub
push_conversor:
	@docker push  williameliasalves/conversao-temperatura:desafio2
	@docker push  williameliasalves/conversao-temperatura:latest
#target apply: apply deployment kubernets
apply_conversor:
	@kubectl apply -f ./k8s/conversor.deployment.yml
	@kubectl apply -f ./k8s/conversor.service.yml
#target forward: execute a por-forward kubectl that point service port to localhost:8080
forward_conversor:
	@kubectl port-forward service/conversor-svc 8000:8000

#target delete: delete conversor resources
delete_conversor:
	@kubectl delete -f ./k8s/conversor.deployment.yml -f ./k8s/conversor.service.yml

#### Part 2 - Kube News

# build
build_news:
	@docker build -t williameliasalves/kube-news:desafio2 kube-news/src
run:

#target push: push image to dockerhub
push_news:
	@docker push  williameliasalves/kube-news:desafio2
	@docker push  williameliasalves/kube-news:latest
#target apply: apply deployment kubernets
apply_news:
	@kubectl apply -f ./k8s/news-db.deployment.yml
	@kubectl apply -f ./k8s/news-db.service.yml
	@kubectl apply -f ./k8s/news.deployment.yml
	@kubectl apply -f ./k8s/news.service.yml
#target forward: execute a por-forward kubectl that point service port to localhost:8080
forward_news:
	@kubectl port-forward service/news-svc 3001:3001