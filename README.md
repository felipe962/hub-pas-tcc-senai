# PAS - Painel de Acesso à Saúde
 
 Um software inovador desenvolvido para superlotação hospitalar que possibilita a visualização do tempo médio de espera em unidades de saúde públicas. O objetivo é redistribuir a alocação de pacientes para dinamizar o atendimento da população.
 
 ## 📋 Documentação
  
  [TAP](#) |
   [Design](https://www.figma.com/design/FA6ByQPNz5zXQ3ex26yvPE/prototipo-pas?node-id=0-1&p=f&t=oC4CAhsPI0ckmX3e-0) |
    [Requisitos](https://sesisenaispedu-my.sharepoint.com/:w:/r/personal/nicolas_santos31_portalsesisp_org_br/Documents/Levantamento%20de%20Requisitos%20Funcionais.docx?d=wb5f8f46b8edf445bacda58460ee3baa3&csf=1&web=1&e=TrSzZs) |
     [Documentação Técnica](#)
 
## 👥 Equipe

### Orientadores
  - **Professor Marcel**
  - **Professor Celso**
  - **Professora Yuri**
  - **Professor Fernando**

### Autores
  - **Nicolas Silva de Almeida Santos** — [Nicolas silva](https://github.com/niiccholas)
  - **Letícia Beatriz Martins** — [Leticia Beatriz](https://github.com/lehmartinss)
  - **Felipe Bahia Correa** — [Felipe Bahia](https://github.com/felipe962)
  - **Vitor Paes Rodrigues** — [Vitor Paes](https://github.com/whospaes)
  - **Ana Júlia Silva Macedo** — [Ana Macedos](https://github.com/anamacedos)

### Desenvolvimento
  - **Backend**: [Ana Júlia Silva Macedo](https://github.com/anamacedos)
  - **Frontend**: [Vitor Paes Rodrigues]()https://github.com/whospaes/senai-tcc-pas
  - **Mobile**: [Letícia Beatriz Martins](https://github.com/lehmartinss/tcc_pas)
  - **Banco de Dados**: [Felipe Bahia Correa](https://github.com/felipe962)
  - **Gerente de Projetos**: [Nicolas Silva de Almeida Santos](https://github.com/niiccholas)

## 🎯 Objetivo do Projeto

Desenvolver um software que seja capaz de calcular a média de tempo de espera de todas as unidades públicas de saúde, com o objetivo de redistribuir a alocação de pacientes para dinamizar o atendimento da população.

## 📱 Plataformas Suportadas
  - **Mobile**
  - **Desktop Web Responsiva**
## ✨ Funcionalidades Principais

- ✅ Login, cadastro e recuperação de senha com conta GOV
- ✅ Busca de unidades de saúde públicas
- ✅ Filtros avançados (especialidade, proximidade, tipo de unidade, disponibilidade 24h)
- ✅ Visualização de campanhas de saúde
- ✅ Visualização de tempo de espera geral e por especialidade
- ✅ Verificação de distância entre instituição e usuário
- ✅ Visualização de dados detalhados das unidades de saúde
- ✅ Mapa interativo com unidades próximas (Google Maps API)
- ✅ Mudança de temas (claro e escuro)
- ✅ Contato com suporte via e-mail


## 🔍 Como Funciona a Coleta de Dados

O tempo de espera é coletado através do horário de retirada e baixa da senha do paciente. Os dados são recebidos via **POST** em um endpoint fornecido pela aplicação. A cada atualização, o sistema:

1. Calcula o tempo de atendimento de cada paciente
2. Soma todos os tempos
3. Divide pela quantidade de pacientes
4. Atualiza a média em tempo real

## 🔐 Segurança

- **Autenticação**: Integração com conta GOV
- **Política de Senha**: Mínimo 8 caracteres com letras maiúsculas, números e caracteres especiais
- **Termos de Uso**: Aceite obrigatório na primeira autenticação
- **Privacidade**: Dados coletados conforme LGPD

## 🏥 Informações das Unidades

Cada unidade de saúde cadastrada contém:

- Tipo de unidade (Hospital Geral, UPA, UBS, etc.)
- Endereço completo
- Telefone de contato
- Especialidades disponíveis
- Tempo de espera geral
- Tempo de espera por especialidade
- Disponibilidade 24h

## 🔎 Filtros de Busca

- **Por Especialidade**: Pediatria, Ortopedia, Cardiologia, etc.
- **Por Proximidade**: Define um raio limite de distância
- **Por Tipo de Unidade**: Hospital Geral, UPA, UBS, etc.
- **Por Disponibilidade**: Unidades com atendimento 24h
- **Por Nome**: Busca convencional pelo nome da unidade


**Nota**: Todas as funcionalidades estão disponíveis em ambas as plataformas.

## 🗺️ Tecnologias Utilizadas

- **Frontend**: React, Responsive Design
- **Mobile**: Kotlin
- **Backend**: Node.js 
- **Banco de Dados**: MYSQL
- **APIs Externas**: Google Maps API
- **Autenticação**: GOV.br

## 📋 Fluxo de Autenticação

1. Usuário acessa a aplicação
2. Tela de login com opção de autenticação GOV
3. Opção de criar conta GOV (redirecionamento externo)
4. Opção de continuar sem login (consulta rápida)
5. Aceite dos termos de uso e responsabilidade obrigatório
6. Redirecionamento para tela inicial após autenticação

## 👤 Perfil do Usuário

### Informações Pessoais (Não Editáveis)

- Nome
- CPF
- Naturalidade
- Data de nascimento
- Nome da mãe

### Dados de Cadastro (Editáveis)
- E-mail
- Foto de perfil
- Endereço
- Telefone

## ⚙️ Configurações

- Alternar tema (claro/escuro)
- Mudar idioma
- Contato com suporte
- Visualizar termos de uso
- Visualizar informações sobre o aplicativo
- Desconectar da conta

## 📜 Termos de Uso

Os termos de uso cobrem:

- Finalidade de Serviço
- Coleta e Tratamento de Dados
- Compartilhamento de Dados
- Responsabilidades do Usuário
- Responsabilidades do Governo Federal
- Atualizações do Termo
- Aceite

## 📊 Dados das Campanhas

As campanhas de saúde são gerenciadas via **Mock API**, permitindo um método escalável e fácil de atualizar.

## 🚀 Instalação

Clone o repositório:

```bash
git clone [URL_DO_REPOSITORIO]
cd pas-projeto
```

Instale as dependências:

```bash
npm install
```

## 🔧 Configuração do Ambiente

Crie um arquivo `.env` na raiz do projeto:

```env
REACT_APP_GOV_AUTH_URL=https://auth.gov.br
DATABASE_URL=sua_url_de_conexao
```

## 🏃 Rodando Localmente

```bash
# Frontend
npm run dev

# Backend
npm start

```

## 🧪 Testes

```bash
npm test
```

## 📁 Estrutura do Projeto

```
pas-projeto/
├── frontend/              # Aplicação web responsiva
├── mobile/                # Aplicação móvel
├── backend/               # API e lógica do servidor
├── database/              # Scripts e configurações do BD
├── docs/                  # Documentação do projeto
├── README.md              # Este arquivo
└── .env.example           # Exemplo de variáveis de ambiente
```
## REFERENCIAS
 [Next.js](https://github.com/nextjs)
 [Node.js](https://github.com/nodejs)
 [MYSQL](https://github.com/mysql)
