# Desafio 2 - Projeto conversor

### Sobre o projeto

Seguindo a aula, clonei o repositório conversão temperatura (https://github.com/KubeDev/conversao-temperatura) e criei uma imagem Docker da aplicação seguindo as melhores práticas.


### Comandos 

**Parte 1** - Conversao-temperatura

- construção da imagem: 

        make build_conversor

- push para docker hub: 

        make push_conversor

- criação do deployment e service:   

        make apply_conversor

- apontamento para o localhost: 
        
        make forward_conversor

**Parte 2** - Conversao-temperatura

- construção da imagem: 

        make build_news

- push para docker hub: 

        make push_news

- criação do deployment e service (site e banco de dados):   

        make apply_news

- apontamento para o localhost (rodando na porta 3001): 
        
        make forward_news
