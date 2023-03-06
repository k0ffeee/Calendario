# Calendario

Uma API para controle de rotina do dia a dia 

### Endpoints

- Eventos 
    - Cadastrar
    - Atualizar
    - Listar todos
    - Mostrar detalhes
- Contas
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
|Conta| text | sim | Conta em que vai ficar salvo o evento

**Exemplo de corpo de requisição**
```js
{
  nome: 'Médico',
  data: '09-03-2023',
  horario: '15:30',
  lembrete: '5 minutos antes',
  conta: 'rm95628@fiap.com.br'
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










