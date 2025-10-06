# 🧠 Projeto Quiz 

Desenvolvido por:  
👩‍💻 Ana Júlia Almeida Lima
👨‍💻 Miguel Gomes Maia


📺 Referência: O projeto foi desenvolvido com base no vídeo linkado abaixo:    
[Como criar um quiz simples com HTML, CSS e JavaScript | Coding With Luiz](https://youtu.be/KXvONdomGos?si=i1sIXWvYtdzivHtJ)

⸻

### 📋 Descrição do Projeto
Este projeto é um quiz desenvolvido com HTML, CSS e JavaScript. O objetivo é testar conhecimentos do usuário por meio de perguntas e respostas de múltipla escolha. O Quiz mostra visualmente se a resposta está certa ou errada. Ao final, o sistema exibe a pontuação total e uma mensagem de feedback.

⸻

#### 🧩 Tecnologias Utilizadas
•	HTML → Estrutura da página (criação dos elementos do quiz)  
•	CSS → Estilização (cores, layout, botões e responsividade)  
•	JavaScript → Lógica do jogo (funções, eventos e manipulação de dados)  

⸻

### 🧠 Explicação do Código

1. HTML (index.html)

O arquivo HTML contém a estrutura básica do quiz.
Principais elementos:
```html
	•	<div id="question"> → onde aparece a pergunta atual.
	•	<div id="answers"> → onde são exibidas as opções de resposta.
	•	<button id="next-button"> → botão para passar para a próxima pergunta.
	•	<div id="score-container"> → mostra o resultado final após o quiz.
```
⸻

2. CSS (style.css)

O CSS foi usado para deixar o quiz visualmente agradável e organizado.
Principais recursos:
	•	Flexbox → para centralizar o conteúdo.
	•	Efeitos de hover → destaque ao passar o mouse sobre as opções.
	•	Cores e espaçamento → para melhor legibilidade e estética.
	•	Transições suaves → para o feedback visual ao selecionar respostas.

⸻

3. JavaScript (script.js)

O JavaScript é responsável pela interatividade do quiz.
Aqui estão as principais partes do código:

🔹 Declaração das perguntas

As perguntas foram criadas em um array de objetos, contendo:
```js
const questions = [
  {
    question: "Qual é a tag usada para criar um link em HTML?",
    answers: [
      { text: "<a>", correct: true },
      { text: "<link>", correct: false },
      { text: "<href>", correct: false }
    ]
  },
  ...
];
```
Cada objeto tem:  
	•	question: o texto da pergunta.  
	•	answers: um conjunto de alternativas, cada uma com text e correct (true/false).

⸻

🔹 Função startQuiz()  
Essa função inicia o quiz, zerando o placar e mostrando a primeira pergunta.

⸻

🔹 Função showQuestion()  
Responsável por mostrar a pergunta atual e suas respostas na tela.  
Usa a manipulação do DOM para criar dinamicamente os botões das alternativas:  
```button.addEventListener("click", selectAnswer);```  

Cada botão escuta o evento de clique, que aciona a função selectAnswer().

⸻

🔹 Função selectAnswer(event)  
Verifica se a resposta clicada é correta ou incorreta.  
	•	Se correta → incrementa a pontuação.  
	•	Em seguida → mostra as cores de feedback (verde/vermelho).  
	•	Habilita o botão “Próxima”.  

Usa condicionais (if/else) para essa verificação.

⸻

🔹 Função handleNextButton()
Controla o avanço do quiz.  
	•	Passa para a próxima pergunta se ainda houver perguntas.  
	•	Caso contrário, chama showScore() para mostrar o resultado final.  

⸻

🔹 Função showScore()  
Exibe a pontuação final do jogador:  
```scoreContainer.innerHTML = Você acertou ${score} de ${questions.length}!;```  

Usa template strings para inserir variáveis diretamente no texto.

⸻

🔹 Eventos Utilizados  
	•	click → usado para detectar quando o usuário seleciona uma resposta ou clica em “Próxima”.  

⸻

🔹 Manipulação do DOM  

Foram usados métodos como:  
	•	document.getElementById() → para acessar elementos HTML.  
	•	document.createElement() → para criar novos botões.  
	•	appendChild() → para adicionar os botões na tela.  
	•	```classList.add() e classList.remove()``` → para alterar o estilo dinamicamente.  

⸻

🧾 Conceitos de Programação Aplicados
	•	Arrays e Objetos → para armazenar perguntas e respostas.
	•	Funções → para organizar o código em partes reutilizáveis.
	•	Condicionais (if/else) → para verificar respostas certas ou erradas.
	•	Laços de repetição → (implícitos em alguns métodos como forEach).
	•	Eventos → para detectar ações do usuário.
	•	Template Strings → para inserir valores dentro de textos com ${}.

⸻

🧠 Resultado Final

O usuário responde uma sequência de perguntas e, ao final, o sistema mostra quantas ele acertou.
Todo o processo é interativo, com feedback visual imediato e pontuação final dinâmica.

⸻

💡 Aprendizados

Durante o desenvolvimento, aprendemos a:
	•	Ligar o HTML, CSS e JavaScript de forma integrada.
	•	Usar funções e eventos para deixar a página interativa.
	•	Manipular o DOM para alterar elementos dinamicamente.
	•	Entender a importância da organização do código e da lógica de programação.
	
