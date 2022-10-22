
# build
build:
	@docker build -t williameliasalves/conversao-temperatura:desafio2 conversao-temperatura/src
run:

#push
push:
	@docker push  williameliasalves/conversao-temperatura:desafio2
	@docker push  williameliasalves/conversao-temperatura:latest

apply:
	kubect apply -f conversor.pod.yml

forward:
	kubect port-forward pod/conversor 8080:8080