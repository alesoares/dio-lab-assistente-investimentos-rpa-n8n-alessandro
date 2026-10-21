# Assistente de Investimentos com RPA e IA Generativa • Confeitaria Connect

## 🏛️ Descrição do Escopo e Decisões Técnicas
Este projeto implementa um pipeline automatizado de extração de dados e recomendação inteligente de alocação de capital para expansão de franquias e investidores da rede Confeitaria Connect. 

A arquitetura foi projetada com foco em alta eficiência, operando com consumo otimizado de memória RAM para viabilizar a execução em servidores de nuvem gratuitos (MVP estável).

### 🛠️ Camadas da Engenharia do Fluxo:
1. **Extração (RPA):** Script em Python utilizando a biblioteca `BeautifulSoup` para realizar o web scraping dos dados de potenciais investidores diretamente da tabela HTML corporativa. O script foi integrado nativamente para disparar um payload limpo em formato JSON via método `POST` contra o endpoint do N8N.
2. **Orquestração (N8N):** Workflow estruturado a partir de um nó de gatilho do tipo `Webhook`. O motor recebe as variáveis, lê o arquivo relacional `data.csv` contendo as opções de aporte e realiza o cruzamento de perfis de forma síncrona através de nós condicionais.
3. **Geração com IA (LLM):** Integração com o agente de inteligência generativa (Gemini/OpenAI) no N8N para analisar dinamicamente o saldo, o perfil de tolerância a risco do cliente e redigir uma mensagem humanizada, com o escudo de governança do desenvolvedor.

**Bons estudos e mãos à obra** 🚀

Se tiver dúvidas, lembre-se: a melhor forma de aprender é experimentando. Erre, corrija e celebre cada pequena vitória no caminho.
