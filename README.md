# Utilização da API Meu Boleto

### **1º - Solicitar credenciais de acesso**

Solicitar à Sami as seguintes credenciais de acesso: IDUsuario, IdParceiro e SIGLA.


### **2º - Adicionar Script de configuração para o botão flutuante.**

Inserir, antes do fechamento da tag BODY do site, a chamada para as configurações.


# Utilização da API
Endpoint direcionado para recuperar link de boleto via CPF/CNPJ. 


#### **Dados**
```php
URL: https://wapi.samierp.com.br/IdParceiro/financeiro/boleto
```

##### **Header**
```json
Content-Type: application/json
```

##### **Body**
```json
{ 
        "sigla":"SIGLA",
        "cpf_cnpj":"12345678900",
        "validar_senha":true,
        "senha":"012345"
}
```


# Botão flutuante com Chat

Como adicionar um botão flutuante de chat para que o usuário consiga recuperar link de boleto via CPF/CNPJ pelo chat.

### Exemplo:

```js
<script src="https://wapi.samierp.com.br/js/meu-boleto/index.js"></script>
<script>

        meuBoleto({
            'config' : {
                'usuario' : 'inserir aqui a IDUsuario',
                'parceiro' : 'inserir aqui a IdParceiro',
                'sigla' : 'inserir aqui a SIGLA',
                'senha' : true // Informe false caso não seja preciso solicitar senha ao usuário
            },
            'botao' : {
                'cor' : 'rgb(0 5 199)', 
                'titulo' : 'Meu Boleto',
                'posicao': 'left', // left/right
            },
            'chat' : {
                'cor' : 'rgb(0 5 199)',
                'titulo' : 'Meu Boleto',
                'posicao': 'left', // left/right
            }
        });

</script>
```



