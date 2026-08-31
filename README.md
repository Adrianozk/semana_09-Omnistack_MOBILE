# AirCnC Mobile — Semana OmniStack 9

Aplicativo mobile do projeto desenvolvido durante a Semana OmniStack 9, da Rocketseat. Esta parte permite encontrar espaços por tecnologia, solicitar reservas e receber a resposta da empresa em tempo real.

> **Contexto:** projeto de estudo criado em 2019 com Expo SDK 35 e React Native. As versões foram preservadas como registro do curso.

## Funcionalidades

- Entrada por e-mail
- Armazenamento local da sessão e das tecnologias de interesse
- Listagem de espaços filtrados por tecnologia
- Solicitação de reserva por data
- Notificação de aprovação ou rejeição com Socket.IO
- Navegação entre Login, Listagem e Reserva

## Tecnologias

- React Native
- Expo
- React Navigation
- Axios
- Socket.IO Client
- AsyncStorage
- Yarn

## Repositórios relacionados

- [Backend](https://github.com/Adrianozk/semana_09-Omnistack_BACKEND)
- [Frontend web](https://github.com/Adrianozk/semana_09-Omnistack_FRONTEND)

## Configuração da API

O celular ou emulador precisa alcançar o computador que executa o backend. Substitua o endereço antigo pelo IP atual da máquina na rede local em:

- `src/services/api.js`
- conexão Socket.IO em `src/pages/List.js`

Exemplo:

```javascript
baseURL: 'http://192.168.1.100:3333'
```

Usar `localhost` em um celular físico apontaria para o próprio aparelho, não para o computador.

## Como executar

1. Inicie o backend e confirme que a porta `3333` está acessível na rede local.
2. Instale as dependências:

```bash
yarn install
```

3. Inicie o Expo:

```bash
yarn start
```

Também estão disponíveis:

```bash
yarn android
yarn ios
yarn web
```

## Estrutura

```text
src/
├── assets/       # imagens do aplicativo
├── components/   # lista reutilizável de espaços
├── pages/        # Login, Listagem e Reserva
├── services/     # cliente HTTP
└── routes.js     # navegação
```

## Observação sobre compatibilidade

O Expo SDK 35 e as dependências utilizadas são legados. A execução em ferramentas atuais pode exigir uma versão antiga e compatível do Node.js ou uma atualização do projeto.
