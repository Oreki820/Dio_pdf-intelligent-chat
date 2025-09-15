# Chatbot Baseado em Conteúdo de PDFs

## Visão Geral do Projeto

Este projeto tem como objetivo criar um **chatbot interativo** capaz de responder perguntas com base em informações extraídas de documentos PDF. A ideia principal é aplicar técnicas de **Processamento de Linguagem Natural (NLP)** e **Machine Learning**, utilizando **busca vetorial** e **embeddings**, para estruturar um sistema que compreenda e interprete conteúdos específicos, sem depender exclusivamente do conhecimento pré-treinado de modelos gerais de IA.

O desafio surgiu da necessidade de organizar informações de forma eficiente, principalmente quando lidamos com múltiplos documentos, artigos científicos ou textos extensos, permitindo extrair respostas rápidas e contextuais a partir de qualquer pergunta feita pelo usuário.

---

## Objetivos do Projeto

- Carregar arquivos PDF e textos relevantes para estudo ou análise.
- Implementar um sistema de **busca vetorial**, indexando informações para recuperação rápida e eficiente.
- Utilizar **IA generativa** para interpretar perguntas e gerar respostas contextuais.
- Criar um **chat interativo**, permitindo interação em tempo real com base no conteúdo dos PDFs carregados.
- Proporcionar insights e possibilidades para expansão, como integração com interfaces web, chatbots em plataformas de mensagens ou sistemas de suporte inteligente.

---

## Passo a Passo do Desenvolvimento

1. **Preparação dos Dados**  
   - Criação de uma pasta `inputs` para armazenar PDFs e textos de referência.  
   - Extração de conteúdo dos PDFs usando bibliotecas Python como `PyPDF2` ou `pdfplumber`.  
   - Para testes iniciais, uso de arquivos `.txt` com sentenças simples simulando artigos científicos ou anotações.

2. **Criação de Embeddings**  
   - Utilização de **TF-IDF (Term Frequency-Inverse Document Frequency)** para criar vetores representativos de cada documento.  
   - Cada vetor permite medir a **similaridade semântica** entre perguntas do usuário e os conteúdos armazenados.  
   - Essa técnica simplificada é eficaz para encontrar respostas relevantes sem depender de grandes modelos de linguagem.

3. **Sistema de Busca Vetorial**  
   - Implementação de função de **busca por similaridade** usando `cosine similarity`.  
   - A resposta retornada é o trecho ou documento mais próximo semanticamente da pergunta.  
   - Permite respostas contextuais mesmo quando a pergunta não corresponde exatamente ao texto original.

4. **Criação do Chat Interativo**  
   - Estruturação de loop interativo para simular conversa em tempo real.  
   - O usuário digita perguntas e o chatbot retorna respostas baseadas nos documentos carregados.  
   - Comando `"sair"` encerra a interação.

5. **Testes e Validação**  
   - Testes com perguntas variadas relacionadas aos textos carregados.  
   - Perguntas objetivas e relacionadas ao conteúdo geram respostas precisas.  
   - Perguntas ambíguas ou fora do escopo retornam trechos mais genéricos, apontando oportunidades de melhoria.

---

## Insights e Aprendizados

- **Organização do conteúdo**: PDFs e textos limpos facilitam criação de embeddings e melhoram a qualidade das respostas.  
- **Vetorização e NLP**: Transformar documentos em vetores permite busca inteligente por similaridade.  
- **Escalabilidade**: Sistema pode lidar com centenas de PDFs, útil para pesquisa acadêmica ou suporte técnico.  
- **Combinação IA Generativa e Busca Vetorial**: Modelos clássicos (TF-IDF) podem ser combinados com LLMs para respostas mais sofisticadas.  
- **Possibilidades futuras**:  
  - Integração com plataformas web ou apps de mensagem.  
  - Upload dinâmico de PDFs pelo usuário.  
  - Sumarização automática de documentos longos.  
  - Interface gráfica amigável para usuários não técnicos.  
  - Suporte a múltiplos idiomas e contextos especializados.

---

## Tecnologias Planejadas

- **Python** – Linguagem principal.  
- **PyPDF2 / pdfplumber** – Extração de texto de PDFs.  
- **scikit-learn** – Vetorização TF-IDF e cálculo de similaridade.  
- **Machine Learning / NLP** – Para análise semântica e busca de respostas.  
- **GitHub** – Versionamento e portfólio.

---

## Como o Projeto Funciona (Resumo Técnico)

- PDFs são carregados e transformados em texto.  
- Texto é vetorizado usando TF-IDF para criar embeddings.  
- Pergunta do usuário também é vetorizada e comparada com os documentos usando **cosine similarity**.  
- Documento mais semelhante é retornado como resposta.  
- Estrutura de chatbot interativo permite perguntas contínuas e respostas imediatas.

---

## Considerações Finais

Este projeto demonstra a integração prática de **NLP**, **Machine Learning** e **desenvolvimento de chatbots** para resolver problemas reais, como organizar informações de múltiplos PDFs e gerar respostas automáticas.  

Mesmo sendo apenas um README no repositório, ele documenta o planejamento, a lógica de desenvolvimento e os aprendizados adquiridos, servindo como **portfólio técnico completo**.
