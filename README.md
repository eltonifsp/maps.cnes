# CNES Visível: A chave para direitos, reembolsos e uma saúde segura!
Mapa interativo de estabelecimentos de saúde com e sem CNES.
# Projeto: CNES Cidadão

## 🏆 Por que este projeto nasceu?

O projeto surgiu da observação de uma dificuldade recorrente: muitos clientes de planos de saúde descobrem, já após receber atendimento, que seu reembolso será recusado porque a clínica não possui cadastro no CNES. Ainda que essa exigência seja considerada irregular pela ANS, ela continua gerando transtornos, pedidos negados e um processo burocrático desnecessário.

Para tornar esse cenário mais simples e transparente, reunimos dados públicos sobre o CNES e os disponibilizamos visualmente e geolocalizados. Assim, qualquer pessoa pode confirmar o cadastro do estabelecimento antes da consulta e tomar decisões mais seguras. Com isso, ajudamos os usuários a proteger seu direito ao reembolso e incentivamos os estabelecimentos de saúde a manterem suas informações em dia.

Portanto, o projeto nasceu para facilitar a vida do consumidor: oferecer informação confiável, reduzir contratempos e fortalecer a relação de confiança entre pacientes, prestadores de serviços e operadoras de saúde.

## 🎯 Objetivo do Projeto

Este projeto visa inicialmente mapear e analisar a distribuição de estabelecimentos de saúde no município de São José dos Campos (SP), servindo como um piloto para uma solução com potencial de expansão para todo o Brasil. Através da combinação de dados abertos e tecnologias de geolocalização, buscamos:

- **Identificar e mapear** estabelecimentos de saúde, distinguindo aqueles com e sem Cadastro Nacional de Estabelecimentos de Saúde (CNES).
- **Facilitar o acesso à informação** sobre a infraestrutura de saúde local para cidadãos, pesquisadores e gestores públicos.
- **Promover a transparência** e o reuso de dados abertos governamentais na temática de Saúde: Dados sobre estabelecimento de Saúde.
- **Subsidiar a criação de políticas públicas** mais eficazes, permitindo que gestores identifiquem lacunas na oferta de serviços de saúde e planejem intervenções direcionadas.
- **Incentivar a conformidade legal** dos estabelecimentos de saúde com as leis municipais e o Artigo 4º da Portaria nº 1.646, de 2 de outubro de 2015, que dispõe sobre o Cadastro Nacional de Estabelecimentos de Saúde (CNES) e suas implicações jurídicas.
- **Oferecer uma ferramenta de acompanhamento** para a comunidade, planos de saúde e outros setores da sociendade sobre os estabelecimentos de saúde em conformidade com as normativas vigentes e jurisprudências aplicáveis.

## 🚀 Próximos Passos

O trabalho está em contínuo desenvolvimento e para tornar o projeto mais promissor e alinhado à evolução dos dados abertos e das tecnologias emergentes, planejamoso:

- **Integração com agentes de IA e chatbots:** Desenvolver um assistente virtual inteligente, capaz de orientar estabelecimentos sobre regularização, responder dúvidas sobre normativos e gerar checklists personalizados, democratizando o acesso à legislação e promovendo conformidade de forma automatizada e inclusiva.
- **Ampliação do geográfica:** Expandir o mapeamento e a análise para outros municípios e, eventualmente, para todo o território brasileiro.
- **Apresentação visual e acessível:** Melhorar a usabilidade e implantar acessibilidade, permitindo filtros, detalhamento e exportação de informações em múltiplos formatos e geração de relatórios e dashboards inteligentes.
- **Aprimoramento da transparência e participação social:** Incorporar novas funcionalidades e dados que possam surgir a partir do feedback dos usuários e das necessidades identificadas na área da saúde.

## 🗄️ Fontes de Dados

Para a construção deste projeto, foram utilizadas as seguintes bases de dados abertos:

**Cadastro Nacional de Estabelecimentos de Saúde (CNES):**
- **URL:** https://dados.gov.br/dados/conjuntos-dados/cnes-cadastro-nacional-de-estabelecimentos-de-saude
- **A base CNES - Cadastro Nacional de Estabelecimentos de Saúde** foi fundamental para identificar e obter informações detalhadas sobre os estabelecimentos de saúde formalmente registrados no Brasil, incluindo dados como tipo de unidade, serviços oferecidos e localização.

**Cadastro Nacional da Pessoa Jurídica (CNPJ):**
- **URL:** https://dados.gov.br/dados/conjuntos-dados/cadastro-nacional-da-pessoa-juridica---cnpj
- **A base do CNPJ** foi utilizada para complementar as informações dos estabelecimentos, especialmente para aqueles que não possuíam registro no CNES, permitindo a identificação de empresas com atividades relacionadas à saúde.

⚠️ **Nota: dados não catalogados**

É importante ressaltar que, devido à natureza dos dados e aos critérios de filtragem aplicados (baseados nos códigos CNAE de saúde), alguns estabelecimentos que poderiam ter alguma relação com a área da saúde, mas que não se enquadram nos códigos específicos ou não possuem registro formal, podem não ter sido catalogados neste projeto. O foco consistiu nos estabelecimentos diretamente identificáveis como de saúde pelas bases de dados governamentais e pelos códigos CNAE selecionados. Além disso, a precisão da geolocalização para estabelecimentos sem CNES depende da qualidade dos dados de CEP fornecidos pela BrasilAPI.


## 💻 Tecnologias Utilizadas

Para o desenvolvimento deste projeto, foram empregadas as seguintes tecnologias:

- **Python:** Utilizado para a extração, tratamento, comparação e consolidação dos dados.
- **MySQL:** Banco de dados para armazenamento dos estabelecimentos de saúde extraídos.
- **Leaflet.js:** Biblioteca JavaScript de código aberto para criação de mapas interativos.
- **HTML/CSS/JavaScript:** Para o desenvolvimento da interface web do mapa.
- **BrasilAPI:** API utilizada para obter coordenadas de latitude e longitude a partir de CEPs.

## 📊 Metodologia e Execução

O desenvolvimento do projeto seguiu as seguintes etapas:

1.  **Extração e Armazenamento de Dados de Estabelecimentos de Saúde:**
    *   Um programa em Python foi desenvolvido para ler arquivos de dados e armazenar informações de estabelecimentos de saúde relacionados ao município de São José dos Campos em um banco de dados MySQL.
    *   A identificação de estabelecimentos de saúde foi realizada com base nos seguintes códigos da Classificação Nacional de Atividades Econômicas (CNAE):
        *   `8610101` – Atividades de atendimento hospitalar.
        *   `8621601` – Serviços móveis de atendimento a urgências.
        *   `8622400` – Serviços de remoção de pacientes, exceto os serviços móveis de atendimento a urgências.
        *   `8630501` – Atividades de atenção ambulatorial executadas por médicos.
        *   `8630502` – Atividades de atenção ambulatorial executadas por odontólogos.
        *   `8640201` – Laboratórios clínicos.
        *   `8640202` – Serviços de diagnóstico por imagem com uso de radiação ionizante, exceto tomografia.
        *   `8650001` – Atividades de profissionais da área de saúde, exceto médicos e odontólogos.
        *   `8660700` – Atividades de apoio à gestão de saúde.
        *   `8690901` – Atividades de práticas integrativas e complementares em saúde humana.
        *   `8690999` – Outras atividades de atenção à saúde humana não especificadas anteriormente.
        *   `8711501` – Atividades de assistência a idosos, deficientes físicos, imunodeprimidos e convalescentes prestadas em residências coletivas e particulares.
        *   `8720401` – Atividades de assistência psicossocial e à saúde a portadores de distúrbios psíquicos, deficiência mental e dependência química.

2.  **Extração de Dados do CNES:**
    *   Após a extração inicial, foram obtidos dados de estabelecimentos cadastrados no Cadastro Nacional de Estabelecimentos de Saúde (CNES).
    *   Esses dados foram salvos em um arquivo `.json` para posterior comparação.

3.  **Comparação e Consolidação de Dados:**
    *   Um novo programa em Python foi desenvolvido para comparar os estabelecimentos extraídos (passo 1) com os dados do CNES (passo 2).
    *   Foi gerado um arquivo `.json` final contendo dados definitivos de estabelecimentos, tanto com CNES quanto sem CNES.
    *   **Para estabelecimentos com CNES:** As informações incluem código CNES, CNPJ, nome, e-mail, turno de funcionamento, telefone, tipo de unidade de saúde, e se possuem: atendimento ambulatorial do SUS, centro cirúrgico, centro obstétrico, centro neonatal, atendimento hospitalar, serviço de apoio e atendimento ambulatorial. Além disso, foram incluídas informações de localidade como endereço, bairro, complemento, número, CEP, e, crucialmente, longitude e latitude.
    *   **Para estabelecimentos sem CNES:** As informações incluem nome, CNPJ, CEP, endereço, número, bairro e complemento. Para a obtenção da longitude e latitude, foi utilizada a API [https://brasilapi.com.br/](https://brasilapi.com.br/), que retorna as coordenadas geográficas a partir do CEP.

4.  **Desenvolvimento do Mapa Interativo:**
    *   Com os dados finais consolidados, foi desenvolvida uma interface web utilizando a biblioteca Leaflet.js.
    *   No mapa gerado, os pontos são visualmente diferenciados:
        *   **Pontos vermelhos:** Indicam estabelecimentos sem CNES.
        *   **Pontos azuis:** Indicam estabelecimentos com CNES.
    *   O mapa permite filtrar a visualização para mostrar apenas estabelecimentos com CNES, sem CNES, ou ambos.
    *   Ao clicar em um ponto no mapa, são exibidos todos os dados e informações detalhadas sobre o estabelecimento correspondente.

## 🌐 Como Acessar o Projeto

O projeto está hospedado publicamente e pode ser acessado através do seguinte link:

[https://eltonifsp.github.io/maps.cnes/](https://eltonifsp.github.io/maps.cnes/)

## 👥 Criadores

- **Prof. Elton Oliveira Ferreira** - IFSP - Câmpus São José dos Campos
- **Gustavo Henrique Souza Gimenez** - IFSP - Câmpus São José dos Campos - Discente do Curso Técnico em Automação Industrial.



