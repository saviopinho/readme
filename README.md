# Rotas desprotegidas

  - POST /people

    Objetivo: Realizar a criação de uma pessoa.

    Requisitos:
      - O documento deve ser único por pessoa, deve ser um CPF ou um CNPJ.
      - O documento deve ser validado na [API de Compliance](https://compliance-api.cubos.io/docs/), você deve realizar a integração com ela. Para a pessoa ser cadastrada, é necessário que o status do documento seja `1`.
      - O documento deve ser retornado sem formatação.

    Request:
    ```json
    {
      "name": "Carolina Rosa Marina Barros",
      "document": "569.679.155-76",
      "password": "senhaforte"
    }
    ```

    Response:
    ```json
    {
      "id": "4ca336a9-b8a5-4cc6-8ef8-a0a3b5b45ed7",
      "name": "Carolina Rosa Marina Barros",
      "document": "56967915576",
      "createdAt": "2022-08-01T14:30:41.203653",
      "updatedAt": "2022-08-01T14:30:41.203653"
    }
    ```
