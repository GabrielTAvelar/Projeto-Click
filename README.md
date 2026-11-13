Jogo de Cliques
Projeto desenvolvido para a disciplina CCP150 – Desenvolvimento de Aplicativos Móveis, da FEI, utilizando React Native e Expo Snack.

A proposta é um jogo simples de reflexos, o jogador precisa clicar em um sol que aparece em posições aleatórias para acumular pontos antes que o tempo acabe.
Funcionalidades
- Cadastro: criação de conta com nome, e-mail e senha.
- Login: autenticação de usuários pelo Firebase Authentication.
- Menu principal: acesso ao jogo, ranking e configurações.
- Jogo: um sol muda de posição a cada clique e soma 1 ponto.
- Cronômetro: a partida dura 30 segundos.
- Fim de jogo: exibe a pontuação final e salva o recorde.
- Ranking: apresenta as 10 maiores pontuações registradas no Firebase Realtime Database.
- Configurações: permite ativar ou desativar a vibração ao clicar no sol (em dispositivos compatíveis).
Tecnologias utilizadas
- JavaScript
- React Native
- Expo Snack (SDK 53)
- React Navigation
- Firebase Authentication
- Firebase Realtime Database
A comunicação com o Firebase é feita por meio de suas APIs REST, utilizando fetch(). Essa abordagem foi adotada para evitar problemas de compatibilidade entre o SDK JavaScript do Firebase e o ambiente do Expo Snack utilizado no projeto.
Organização dos arquivos
App.js
components/
  cadastro.js
  login.js
  PaginaLogado.js
  jogo.js
  fimDeJogo.js
  rank.js
  configuracoes.js
config/
  config.js
  ajustes.js
  ranking.js
- App.js: configura a navegação entre as telas.
- components/: contém as telas do aplicativo.
- config/config.js: realiza a autenticação por API REST.
- config/ranking.js: salva e consulta pontuações.
- config/ajustes.js: guarda a preferência de vibração durante a execução do app.
Como executar
1. Abra o projeto no Expo Snack com o SDK 53.
2. Confira os arquivos e as dependências de navegação do projeto.
3. No Firebase Console, habilite Authentication → Email/Senha e crie um Realtime Database.
4. Configure apiKey e databaseURL em config/config.js com os dados do seu projeto Firebase.
5. Execute a prévia no navegador ou em um dispositivo com Expo Go compatível.
6. Cadastre um usuário, faça login e clique em Jogar.
A vibração deve ser testada em um celular compatível; a prévia Web não reproduz a vibração. As configurações de vibração e a sessão de login não são persistidas após reiniciar o aplicativo.

Observações
Este é um projeto acadêmico. O ranking é atualizado pelo próprio aplicativo e não possui verificação de pontuação no servidor. Caso o Realtime Database esteja com leitura e escrita públicas para testes, essas regras devem ser restringidas antes de publicar o aplicativo para uso real.
