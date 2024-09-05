# NLP - Analise de Sentimento

Para servir um modelo BERT treinado no PyTorch, você pode usar uma combinação de FastAPI e TorchServe, por exemplo. Aqui estão os passos.

## 1-Instale as dependências:
    pip install fastapi
    pip install uvicorn
    pip install torchserve
    pip install transformers
    pip install pinferencia

## 2-Crie um arquivo chamado app.py com o código da app.

## 3-Inicie o servidor FastAPI usando o Uvicorn com o comando abaixo:
    uvicorn app:app --host 0.0.0.0 --port 8000
  Isso iniciará o servidor na porta 8000. Você pode acessar a documentação do FastAPI em http://localhost:8000/docs e testar a API de análise de sentimento.
  
## 4-Para fazer uma solicitação à API usando curl via linha de comando, use:
    curl -X  POST  "http://localhost:8000/sentimento" -H    "accept:  application/json" -H  "Content-Type: application/json" -d "{\"text\":\"Eu amo inteligência artificial!\"}"
    
  Isso retornará um JSON com o sentimento analisado e os scores associados.
  Note que este é apenas um exemplo básico para te ajudar a começar. Dependendo do seu caso de uso, você pode querer adicionar recursos adicionais, como autenticação, registro e tratamento de erros. Além disso, considere usar um servidor de produção como Gunicorn e configurar um proxy reverso com Nginx para expor a API publicamente de forma segura.
