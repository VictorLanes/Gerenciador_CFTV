Este é um Painel Operacional Full Stack desenvolvido para centralizar o controle de manutenção, inventário de hardware e gestão de acessos de unidades operacionais. O sistema permite o monitoramento de câmeras, configurações de rede, status de alarmes e o fluxo de ordens de serviço (OS) em tempo real.

O projeto utiliza uma arquitetura leve onde o Frontend (HTML5/CSS3/JS) se comunica com um Backend processado via Google Apps Script, utilizando o Google Sheets como banco de dados escalável e acessível.

🚀 Principais Funcionalidades
1. Gestão de Unidades
Inventário Detalhado: Cadastro de IP, Cloud NVR, senhas de câmeras, MAC de alarmes e sensores.

Controle de OS: Monitoramento do status da Ordem de Serviço (Aberta, Em andamento, Concluída, etc.) e data de abertura.

Status Operacional: Classificação visual por cores para unidades Ativas, em Manutenção, Vandalizadas ou Offline.

Ações Rápidas: Botões de cópia em um clique para logins, IPs e senhas, otimizando o tempo do técnico.

2. Controle de Acesso (RBAC)
Perfis Distintos: Diferenciação entre perfil Administrador e Técnico.

Permissões Granulares: Controle individual de quem pode Visualizar, Incluir, Editar ou Excluir dados.

Filtro por UF: Restrição de visibilidade baseada na unidade federativa (Estado) atribuída ao usuário.

3. Ferramentas de Produtividade
Busca Inteligente: Filtros combinados por OS, Nome da Unidade, UF e busca geral por texto.

Exportação: Geração de relatórios em formato Excel (.xls) baseados nos filtros aplicados.

Interface Adaptável: Suporte nativo a Modo Escuro e layout totalmente responsivo para tablets e smartphones.

🛠️ Tecnologias Utilizadas
Frontend:

HTML5 e CSS3 (Variáveis CSS, Flexbox, Grid Layout).

JavaScript Vanilla (ES6+) para manipulação de DOM e consumo de API.

Backend:

Google Apps Script (GAS) atuando como API REST.

Banco de Dados:

Google Sheets (Integração nativa com GAS).

📂 Estrutura do Código
O arquivo index.html é autocontido e organizado da seguinte forma:

Variáveis Root CSS: Facilita a manutenção de cores e a troca de temas.

Layout Grid: Separação clara entre a lista de unidades (scroll principal) e formulários de edição (fixos na lateral).

Lógica de Normalização: O sistema trata diferentes nomes de colunas vindos da planilha para garantir que os dados não quebrem a interface.

Segurança: Validação de permissões no lado do cliente (UI) e expectativa de validação no lado do servidor (API).

⚙️ Como Configurar
Certifique-se de que a API_BASE no JavaScript aponta para a URL de implantação (Web App) do seu Google Apps Script.

A planilha do Google Sheets deve conter as abas UNIDADES e USUARIOS com os cabeçalhos correspondentes.

O acesso inicial depende do cadastro prévio de um usuário com perfil admin na base de dados.

🛡️ Licença e Uso
Este projeto foi desenvolvido para uso em operações de manutenção técnica, visando a centralização de informações críticas de infraestrutura de TI e Segurança Eletrônica.
