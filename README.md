# web2

## Changelog - Avaliação parte 2
* *Implementar controle de likes/deslikes dos comentários*: Adicionadas/Atualizas as rotas
  * [/content/:id/like](https://github.com/Tashima42/web2/blob/main/src/routes/content/like.js)
  * [/content/:id/dislike](https://github.com/Tashima42/web2/blob/main/src/routes/content/dislike.js)
* *listar os comentários pelo saldo dos likes (positivos - negativos)*: Atualizada a rota de filtrar, adicionando função de sorting
  * [/content/filter](https://github.com/Tashima42/web2/blob/main/src/routes/content/filter.js)
* *Implementar uma rota para buscar a pizza com o maior número de likes*: Adicionada rota
  * [/content/order/likes](https://github.com/Tashima42/web2/blob/main/src/routes/content/order/likes.js)

## Postman Collection
Importe a collection do postman utilizando o arquivo `Pizza.postman_collection.json`    
Essa collection possui exemplos de requests e responses, e já tem um token de autorização configurado para facilitar as requests.

**obs**: O envio de imagens pode ser feito usando base64 encoding, porém o tamanho do arquivo é limitado a ~70kb

## Usuario de teste
username: admin@example.com    
password: secret1


## Autorizacao
Existem dois métodos de autorização, enviando um header de autorização ou enviando um cookie.

**Header**:
```
Authorization: Bearer (substituir pelo jwt retornado no login)
```
**Cookie**:
Ao fazer o login, um cookie com o nome `session` é enviado na resposta, esse cookie pode ser usado como alternativa ao header `Authorization`

## Rodando o repositorio

**Com docker**:    
```
docker-compose up
```

**Sem docker**:    
É necessário ter uma instância do MongoDB configurado no arquivo `.env`
```sh
npm install
npm run dev
```

**Rodando testes**:    
```
docker-compose up -d mongo
npm run test
```
