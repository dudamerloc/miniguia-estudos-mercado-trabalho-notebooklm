# 🧠 Documentação de Experimento: Segundo Cérebro no NotebookLM para Recém-Formados

Link do NotebookLM: https://notebooklm.google.com/notebook/0fab0429-3518-45d2-a7c5-87067e5d57d2

> **Descrição:** Um guia prático e template de "Segundo Cérebro" no NotebookLM para ajudar recém-formados a melhorarem seu portfólio e serem notados pelo mercado de trabalho.

Este repositório documenta um laboratório prático de Engenharia de Prompts utilizando o NotebookLM. O objetivo é criar uma metodologia para que profissionais em início de carreira possam estruturar seus estudos e gerar conteúdo estratégico de portfólio.

---

## Objetivos de Estudo:

Este material foi desenvolvido com os seguintes propósitos de aprendizado:
1. **Compreensão de RAG (Retrieval-Augmented Generation):** Avaliar como o NotebookLM ancora suas respostas estritamente nos documentos fornecidos, evitando alucinações.
2. **Otimização de Contexto:** Testar os limites de contextualização da IA ao cruzar dados de perfis profissionais (currículos) com tendências de mercado.
3. **Engenharia de Prompt:** Identificar quais padrões de instrução geram respostas acionáveis e quais falham, documentando o processo de correção.

---

## Curadoria de Fontes (Uploads no NotebookLM):

Para que o modelo funcionasse com dados reais e atualizados do ecossistema de recrutamento e tecnologia, foram selecionadas e carregadas algumas das seguintes fontes abertas:

* https://prodest.es.gov.br/como-os-profissionais-de-ti-podem-usar-o-linkedin (Como os profissionais de TI podem usar o LinkedIn
)
* https://www.devmedia.com.br/como-montar-um-portfolio-de-programacao-mesmo-sem-experiencia/44180 (Como Montar um Portfólio de Programação Mesmo Sem Experiência?)
* https://www.opservices.com.br/certificacoes-de-ti/ (Certificações de TI mais requisitadas em 2026: guia por domínio de carreira)
* https://quarkrh.com.br/blog/10-tendencias-de-recrutamento-e-selecao/ (10 Tendências de Recrutamento e Seleção que vão marcar 2026)
* https://docs.github.com/pt/pages/quickstart (Início Rápido para Páginas do GitHub)

---

## Engenharia de Prompts e "Cicatrizes":

Abaixo estão registrados os testes de prompts, as variações aplicadas, os resultados obtidos e as dificuldades técnicas enfrentadas até chegar na resposta ideal.

###  Experimento 1: Análise de Gaps no Portfólio
*   **Prompt Inicial (Falhou):** *"Analise meu currículo e me diga o que falta para eu conseguir uma vaga."*
    *   **Resultado/Problema:** A IA deu respostas genéricas demais ("melhore sua comunicação", "estude mais inglês"), ignorando o contexto técnico dos arquivos carregados.
*   **Prompt Otimizado (Sucesso):** *"Com base estritamente no relatório de tendências do mercado (Fonte 1) e nos projetos do meu currículo (Fonte 4), cruze os dados e liste 3 competências técnicas explícitas que o mercado exige e que meus projetos ainda não demonstram."*
    *   **Cicatrize/Lição Aprendida:** O NotebookLM precisa de comandos de ancoragem explícitos (ex: *"com base estritamente na Fonte X"*) para parar de usar o conhecimento geral da internet e focar nos PDFs do repositório.

###  Experimento 2: Extração de Plataformas Alternativas
*   **Prompt Inicial (Falhou):** *"Quais redes além do LinkedIn posso usar?"*
    *   **Resultado/Problema:** O modelo listou redes óbvias (Instagram, Twitter) sem conectar com o perfil profissional do estudante.
*   **Prompt Otimizado (Sucesso):** *"Atue como um mentor de carreira focado em portfólios digitais. Analisando meus projetos de design/dev nas fontes, identifique 2 plataformas de nicho (ex: Behance/Medium) onde esses projetos teriam maior apelo visual ou de documentação textual. Justifique com base nas diretrizes da Fonte 3."*
    *   **Cicatrize/Lição Aprendida:** Adicionar uma persona restritiva (*"Atue como mentor de carreira"*) mudou o tom da IA de "lista enciclopédica" para "conselho estratégico aplicado".

###  Experimento 3: Storytelling / Post de Aprendizado
*   **Prompt Inicial (Falhou):** *"Escreva um post pro LinkedIn sobre o meu projeto."*
    *   **Resultado/Problema:** O texto gerado parecia propaganda corporativa artificial, cheio de jargões cafonas e hashtags excessivas.
*   **Prompt Otimizado (Sucesso):** *"Utilizando a metodologia da Fonte 2 (Learning in Public), transforme o Desafio X do meu projeto em uma narrativa curta para o LinkedIn. Estrutura rígida: 1 frase curta de impacto, o problema técnico enfrentado, o erro cometido antes de acertar, e a solução. Tom: Jovem, técnico e sem autopromoção exagerada."*

---

##  Resultados Obtidos ao Acessar o Portfólio:

Ao navegar pelos arquivos deste repositório, você encontrará:
*   Os arquivos markdown prontos com os prompts finais validados.
*   Exemplos de saídas de texto estruturadas prontas para adaptação.
*   A lógica de como utilizar ferramentas de IA de forma analítica e crítica, e não como um mero gerador de texto automático.

