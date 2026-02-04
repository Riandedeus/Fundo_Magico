
# 🎨 Projeto Fundo Mágico - Dev em Dobro

Um gerador de gradientes dinâmicos que utiliza Inteligência Artificial para transformar descrições em linguagem natural em código CSS real, renderizado instantaneamente na tela.

## 🚀 Sobre o Projeto

O objetivo deste projeto é demonstrar a integração entre tecnologias web e ferramentas de automação (n8n), utilizando a API do Gemini para processar prompts e retornar código estruturado.

<img width="1301" height="822" alt="image" src="https://github.com/user-attachments/assets/9e4442b2-57f7-4a02-8b09-0d3300ae235e" />


O fluxo funciona da seguinte forma:

1. O usuário descreve o gradiente (ex: *"Um pôr do sol em Marte com tons de roxo e laranja"*).
2. O **JavaScript** envia essa string para um webhook do **n8n**.
3. O **n8n** consulta o **Gemini AI**, que gera o código CSS correspondente.
4. O **n8n** retorna o código para o frontend.
5. O site aplica o estilo dinamicamente ao DOM, alterando o fundo e exibindo o código gerado.

---

## 🛠️ Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3 e JavaScript.
* **Automação:** n8n.
* **IA:** Google Gemini API.

---

## 🏗️ Arquitetura do Sistema

1. **Interface:** Captura o input do usuário.
2. **Webhook (n8n):** Recebe o POST do navegador.
3. **Prompt Engineering:** O n8n formata o pedido para a IA, garantindo que ela responda apenas com o JSON contendo o CSS.
4. **Resposta:** O JavaScript recebe o JSON e o utiliza para atualizar a página.

---

## ⚙️ Configuração

### 1. n8n (Workflow)

Para que o projeto funcione, você precisa criar um workflow no n8n com os seguintes nós:

* **Webhook Node:** Método `POST`.
* **Google Gemini Node:** Configuração das credenciais para o uso da API do Gemini.
* *Prompt Sugerido:* utilize o arquivo "prompt-gerador"
* **Code in JavaScript:** Formata a resposta fornecida pela IA para o padrão desejado. 
* **Respond to Webhook:** Retorna o resultado da IA.
  
  <img width="1202" height="455" alt="image" src="https://github.com/user-attachments/assets/e7c7c5e5-02e1-4ad3-a898-090a16fa0c84" />


## 📝 Exemplo de Uso

1. Abra o `index.html` no seu navegador.
2. Digite no campo de texto: `"Um gradiente oceânico profundo com toques de bioluminescência neon"`.
3. Clique em **Gerar Background Mágico**.
4. O fundo da página mudará automaticamente para o estilo criado pela IA.

---
