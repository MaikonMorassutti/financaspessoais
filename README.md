Minha Gestão Financeira - App Completo

🎯 Sobre o Projeto
Minha Gestão Financeira é uma aplicação web completa, desenvolvida como um projeto de portfólio para demonstrar habilidades em desenvolvimento front-end, integração com back-end (BaaS) e visualização de dados. O sistema permite ao usuário gerenciar suas finanças pessoais de forma detalhada, incluindo contas bancárias, cartões de crédito, investimentos e outros ativos.

A aplicação foi construída com foco em uma interface limpa, responsiva e funcional, oferecendo dashboards interativos para uma análise aprofundada da saúde financeira do usuário.

➡️ Acesse a demonstração ao vivo: Link para o seu App no GitHub Pages ou Vercel

✨ Funcionalidades Principais
A aplicação oferece um conjunto robusto de funcionalidades para um gerenciamento financeiro completo:

Autenticação: Login anônimo e seguro com Firebase Authentication, garantindo que os dados de cada usuário sejam privados.

Dashboard Principal:

Visão geral com cards de resumo (Receitas, Despesas, Saldo do Mês, Saldo em Contas, etc.).

Filtros dinâmicos por mês e ano.

Gestão de Contas:

Criação, edição e exclusão de contas correntes/poupança.

Controle de saldo inicial, limites e empréstimos.

Gestão de Cartões de Crédito:

Cadastro de cartões com limite, data de fechamento e vencimento.

Lançamento de despesas e estornos.

Visualização e pagamento de faturas.

Gestão de Investimentos:

Cadastro de diversos tipos de ativos (Ações, FIIs, Renda Fixa).

Registro de aportes e resgates.

Atualização do valor de mercado e cálculo de rentabilidade.

Outros Ativos:

Cadastro de ativos imobilizados e outros bens para compor o patrimônio total.

Transações:

Lançamento detalhado de receitas e despesas.

Sistema de transferência entre contas.

Categorização de transações.

Dashboard de Análise:

Gráficos interativos (Pizza, Linha, Barras) para análise de:

Receitas e Despesas por categoria.

Evolução do saldo mensal.

Composição da carteira de investimentos.

Rentabilidade mensal dos investimentos.

Tabelas detalhadas e projeção de saldo futuro.

Interface Responsiva: Design totalmente adaptável para desktops, tablets e smartphones.

🛠️ Tecnologias Utilizadas
Este projeto foi construído com as seguintes tecnologias e bibliotecas:

HTML5 e CSS3: Estrutura e estilização base.

JavaScript (ES6+): Toda a lógica da aplicação, manipulação do DOM e interatividade.

Tailwind CSS: Framework CSS para uma estilização rápida, moderna e responsiva.

Firebase: Utilizado como Back-end as a Service (BaaS) para:

Firestore: Banco de dados NoSQL em tempo real para armazenar todos os dados do usuário.

Firebase Authentication: Para o sistema de autenticação anônima.

Chart.js: Biblioteca para a criação dos gráficos e dashboards interativos.

Google Fonts: Para a fonte 'Inter', garantindo uma tipografia limpa e legível.

🚀 Como Executar o Projeto Localmente
Para executar este projeto no seu ambiente local, siga os passos abaixo.

Pré-requisitos
Um navegador web moderno (Chrome, Firefox, Edge).

Uma conta no Firebase para configurar o seu próprio back-end.

Configuração do Firebase
Crie um Projeto no Firebase:

Acesse o Console do Firebase.

Clique em "Adicionar projeto" e siga as instruções.

Adicione um App Web ao seu Projeto:

No painel do seu projeto, clique no ícone da web (</>) para registrar um novo aplicativo da web.

Dê um nome ao seu app e clique em "Registrar app".

O Firebase fornecerá um objeto de configuração firebaseConfig. Copie este objeto.

Configure a Autenticação:

No menu lateral, vá para Authentication.

Na aba Sign-in method, ative o provedor Anônimo.

Configure o Firestore Database:

No menu lateral, vá para Firestore Database.

Clique em "Criar banco de dados" e inicie no modo de produção.

Após a criação, vá para a aba Regras e cole as seguintes regras para permitir que usuários autenticados leiam e escrevam seus próprios dados. Isso é crucial para a segurança.

rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    // Permite que usuários autenticados acessem apenas seus próprios dados
    match /artifacts/{appId}/users/{userId}/{document=**} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
  }
}

Instalação
Clone o Repositório:

git clone https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git

Navegue até o Diretório do Projeto:

cd NOME-DO-REPOSITORIO

Configure as Credenciais do Firebase:

Abra o arquivo index.html.

Localize a seção <script type="module"> no final do arquivo.

Encontre o objeto firebaseConfig e substitua os valores de placeholder pelos valores que você copiou do seu console do Firebase.

const firebaseConfig = {
    apiKey: "SUA_API_KEY",
    authDomain: "SEU_AUTH_DOMAIN",
    projectId: "SEU_PROJECT_ID",
    storageBucket: "SEU_STORAGE_BUCKET",
    messagingSenderId: "SEU_MESSAGING_SENDER_ID",
    appId: "SEU_APP_ID"
};

Abra o index.html no seu Navegador:

Você pode simplesmente abrir o arquivo index.html diretamente no seu navegador, ou usar uma extensão como o "Live Server" no VS Code para uma melhor experiência de desenvolvimento.

E pronto! A aplicação estará rodando no seu ambiente local, conectada ao seu próprio back-end do Firebase.

📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

📬 Contato
Maikon Morassutti

LinkedIn: https://www.linkedin.com/in/maikon-morassutti-42972132/
GitHub: https://github.com/MaikonMorassutti

Email: maikon.morassutti@hotmail.com
