# Estudo de caso - Pix
Este projeto é um estudo de caso sobre tudo o que diz respeito ao framework Angular.

Iremos trabalhar com RxJs, Observables, NgRx, Clean Code além de definir uma arquitetura básica/padrão para projetos Angular do ponto de vista de organização de código, arquivos e pastas.

Vamos simular o sistema de pagamentos instantâneo do Banco Central do Brasil (BCB), o Pix. O objetivo desse projeto é entender melhor sobre Arquitetura de Projetos/System Design, Gerenciamento de Estado Global da aplicação e Boas Práticas de Desenvolvimento. 

Para isso, nesse README, vamos definir a arquitetura padrão que será usada com base nas recomendações do Style Guide do Angular e vamos separar em branches as implementações usando RxJs e NgRx, afim de documentar e ter exemplos de implementação. 

## System Design
A organização do sistema seguirá o exposto a seguir e, sempre que necessário, passará por atualizações para compreender os itens que forem adicionados ao projeto.

```
src/app
 ├── core/                 # Serviços centrais (auth, interceptors, guards)
 ├── features/
 │    ├── pagamentos/      # Pagamentos via QR Code e Pix Copia e Cola
 │    ├── transferencias/  # Transferências Pix entre contas
 │    ├── chaves/          # Cadastro e gestão de chaves Pix
 │    ├── contatos/        # Lista e gestão de contatos
 │    ├── extrato/         # Histórico e extrato de transações
 │    └── dashboard/       # Tela inicial (resumo do saldo e atalhos)
 ├── shared/
 |    |── components                  # Componentes e utilitários reutilizáveis
 |    |── services                    # Services
 |    |── typings/interfaces          # Arquivos de types ou interfaces
 |    |── enums                       # Enums
 └── app.config.ts         # Rotas e bootstrap da aplicação




```