# Calendario

Uma API para controle de rotina do dia a dia 

### Endpoints

- Eventos 
    - Cadastrar
    - Atualizar
    - Listar todos
    - Mostrar detalhes
- Usuário
    - Cadastrar
    - Atualizar
    - Listar todos
    - Mostrar detalhes


### Cadastrar Evento
`POST`/api/evento

|Campo|tipo|Obrigatório|descrição
|------ |------|:-----------: |---------
|Nome|text|sim|Nome do evento para poder indentificar
|Horário| time | sim | Horário em que vai acontecer o evento
|Lembrete| text | não | Mandar uma notificação de quando irá acontecer um determinado evento
|usuário| text | sim | usuário em que vai ficar salvo o evento

**Exemplo de corpo de requisição**
```js
{
  nome: 'Médico',
  data: '09-03-2023',
  horario: '15:30',
  lembrete: '5 minutos antes',
  user: 'rm95628@fiap.com.br'
}

```


**Exemplo de corpo da respota**

**Cógigos de respota**

|código| descrição
| - | -
|201 | evento cadastrado com sucesso
|400 | os campos enviados sao invalidos



### Detalhar Evento
`GET`/api/evento/{id}       
```js
{
  nome: 'Médico',
  data: '09-03-2023',
  horario: '15:30',
  lembrete: '5 minutos antes',
  conta: {
          conta_id: 1,
          conta_email: 'rm95628@fiap.com.br'
  }
}
```

**Cógigos de respota**

|código| descrição
| - | -
|200 | dados retornados com sucesso
|404 | não existe evento com o id informado









### Cadastrar Usuário
`POST`/api/usuario

|Campo|tipo|Obrigatório|descrição
|------ |------|:-----------: |---------
|Nome de Usuario|text|sim|Nome que identicará o usuário e também poderá ser utilizado para login
|Email| text | sim | email do usuário para efetuar o login
|Senha| text | sim | senha do usuário para efetuar o login

**Exemplo de corpo de requisição**
```js
{
  user: 'Fernando.Cesar',
  email: 'rm95628@fiap.com.br',
  senha: '12345abc'
}

```


**Exemplo de corpo da respota**

**Cógigos de respota**

|código| descrição
| - | -
|202 | conta cadastrada com sucesso
|401 | os campos enviados sao invalidos



### Detalhar usuário
`GET`/api/usuario/{id}       
```js
{
  user: 'Fernando.Cesar',
  email: 'rm95628@fiap.com.br',
  senha: '12345abc'
}
```

**Cógigos de respota**

|código| descrição
| - | -
|200 | dados retornados com sucesso
|402 | não existe usuário com o id informado







