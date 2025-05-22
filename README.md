# Chekpoint3-kotlin

Ygor Carneiro Arean RM88170

Definições do projeto
Lista de Compras Android
Este é um aplicativo Android desenvolvido em Kotlin que permite aos usuários gerenciar uma lista de compras de forma simples e eficiente. Utilizando arquitetura moderna e componentes do Jetpack, o aplicativo oferece uma experiência fluida e persistência de dados local.

 Tecnologias Utilizadas
Kotlin: Linguagem principal para o desenvolvimento Android.
RecyclerView: Exibição eficiente de listas de itens.
ViewModel & LiveData: Gerenciamento de dados e ciclo de vida da UI.
SQLite: Persistência de dados local.
Gradle: Gerenciamento de dependências.

 Funcionalidades
Adicionar, editar e remover itens da lista de compras.
Visualizar todos os itens em uma lista dinâmica.
Persistência de dados local utilizando SQLite.
Interface intuitiva e responsiva.

 Estrutura do Projeto
bash
Copier
Modifier
android-lista-de-compras/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── carreiras/
│   │   │   │           └── listadecompras/
│   │   │   │               ├── ui/            # Atividades e fragmentos
│   │   │   │               ├── viewmodel/     # ViewModels
│   │   │   │               ├── model/         # Modelos de dados
│   │   │   │               ├── repository/    # Repositórios de dados
│   │   │   │               └── database/      # Acesso ao SQLite
│   │   │   └── res/                          # Recursos (layouts, strings, etc.)
├── build.gradle.kts
├── settings.gradle.kts
└── ...
 Detalhamento das Funcionalidades
RecyclerView
A lista de compras é exibida utilizando o RecyclerView, que permite uma renderização eficiente de listas, mesmo com um grande número de itens. 
Cada item da lista é representado por um ViewHolder, que é reciclado conforme o usuário rola a lista, melhorando o desempenho.

Persistência de Dados com SQLite
Os dados da lista de compras são armazenados localmente utilizando SQLite, garantindo que as informações persistam mesmo após o fechamento do aplicativo. 
Isso é gerenciado através de uma camada de repositório que abstrai as operações de banco de dados.

ViewModel & LiveData
O ViewModel mantém os dados da UI mesmo durante mudanças de configuração, como rotações de tela. 
O LiveData permite que a UI observe mudanças nos dados, atualizando automaticamente a interface quando os dados são modificados.

 Como Funciona
Ao iniciar o aplicativo, o ViewModel carrega os dados da lista de compras do banco de dados SQLite.
O LiveData notifica a UI sobre os dados carregados.
O RecyclerView exibe os itens da lista utilizando um adaptador personalizado.
O usuário pode adicionar, editar ou remover itens, com as mudanças sendo refletidas imediatamente na UI e persistidas no banco de dados.
