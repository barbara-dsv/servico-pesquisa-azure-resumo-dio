# 📚 Módulo: Serviços de Pesquisa e Inteligência de Documentos com IA no Azure

Este módulo explora dois grandes grupos de funcionalidades de IA no Azure:

- **Inteligência de Documentos**, com foco na extração automatizada de dados a partir de formulários, imagens e PDFs.
- **Azure Cognitive Search**, que permite indexar grandes volumes de dados e enriquecê-los com inteligência artificial para facilitar consultas inteligentes.

---

## 🧠 Inteligência de Documentos com Azure

### Serviços de Inteligência de Documentos de IA do Azure

- Problema comum: formulários ou notas fiscais podem ser danificados, ilegíveis ou extraviados.
- A IA do Azure pode ler esses documentos e extrair automaticamente as informações relevantes.
- A análise de documentos:
  - Retorna representações estruturadas dos dados.
  - Detecta regiões de interesse e seus relacionamentos (usando modelos pré-definidos ou personalizados).
  - Pode ser feita em dois modos: gratuita (limitada) ou paga (mais completa).

### Análise com Document Intelligence e o Estúdio

- Extrai informações de formulários digitalizados em imagem ou PDF.
- Pode utilizar:
  - **Modelos pré-treinados** para documentos comuns (ex: faturas, recibos, contratos).
  - **Modelos personalizados** treinados com os próprios documentos da empresa.
- Não se limita a OCR (leitura de texto); realiza reconhecimento **semântico** dos campos.
- A interface é **no-code**, com exemplos práticos disponíveis.

---

## 🔎 Azure Cognitive Search e Mineração de Conhecimento

### O que é Mineração de Conhecimento?

- Muitas empresas armazenam informações valiosas em documentos não estruturados (PDFs, imagens, anotações manuais).
- A mineração de conhecimento usa IA para **indexar e extrair informações úteis** desses documentos.
- Elementos essenciais:
  - Mecanismo de pesquisa por palavras-chave.
  - Indexação inteligente de conteúdo.
  - Sintaxe de busca estruturada.

### Solução Azure Cognitive Search

#### Ingestão de Dados

- Fontes de ingestão compatíveis:
  - Azure Blob Storage
  - Azure Data Lake Storage Gen2
  - Azure Table Storage

#### Enriquecimento com IA

- Permite interpretação mais profunda dos dados usando:
  - Visão computacional
  - Processamento de linguagem natural (NLP)
- Habilita funcionalidades como:
  - Reconhecimento de entidades
  - Tradução de texto
  - Análise de sentimentos
- O conteúdo enriquecido é processado por **conjuntos de habilidades** e enviado para o mecanismo de busca para indexação.

#### Exploração e Visualização

- Os dados indexados ficam disponíveis em formato JSON.
- Pesquisas são feitas diretamente nos índices criados.
- Pode ser integrado com aplicativos ou dashboards personalizados.


---

## 💡 Etapas Realizadas e Configurações

Durante a prática do módulo, foram criados os serviços necessários para habilitar a solução de mineração de conhecimento com IA:

### 1. Criação do Serviço Cognitivo (Azure AI)

- **Tipo de preço:** Standard S0  
- Justificativa: oferece os recursos necessários para uso com o Document Intelligence e é o mínimo exigido para indexação cognitiva.

### 2. Criação do Serviço de Pesquisa (Azure Cognitive Search)

- **Plano:** Básico  
- **Localização:** East US (região mais econômica)

### 3. Criação da Conta de Armazenamento

- **Desempenho:** Standard  
- **Redundância:** LRS (Locally-redundant storage, mais econômico)
- Após a criação:
  - Em **Configurações**, habilitar **"Permitir acesso anônimo ao Blob"**.
  - Criar um **container**:
    - O nome precisa ser único.
    - Em **Nível de acesso anônimo**, selecionar:  
      **Contêiner (acesso de leitura anônimo para contêineres e blobs)**.

Essas configurações permitiram que os dados armazenados fossem usados no pipeline de ingestão do Azure Cognitive Search com enriquecimento por IA.

---

✅ **Resultado:** foi possível estruturar uma solução completa de inteligência de documentos e pesquisa cognitiva com IA no Azure, unindo teoria e prática.



## ✅ Conclusão

Este módulo mostra como o Azure permite que dados não estruturados sejam transformados em **informações pesquisáveis e úteis**, com suporte de IA para compreensão semântica. Uma solução poderosa para qualquer cenário que envolva grandes volumes de documentos!

