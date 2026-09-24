<div align="center">

# Pokédex

App de Pokédex em Flutter para Android, iOS e web, com busca, status, evoluções e vantagens por tipo.

![Flutter](https://img.shields.io/badge/Flutter-0D0D0D?style=for-the-badge&logo=flutter&logoColor=FF003C)
![Dart](https://img.shields.io/badge/Dart-0D0D0D?style=for-the-badge&logo=dart&logoColor=FF003C)
![Android](https://img.shields.io/badge/Android-0D0D0D?style=for-the-badge&logo=android&logoColor=FF003C)
![iOS](https://img.shields.io/badge/iOS-0D0D0D?style=for-the-badge&logo=apple&logoColor=FF003C)

</div>

## Sobre

Aplicativo mobile que lista os Pokémon em cards coloridos pelo tipo principal e abre uma ficha detalhada de cada um. Os dados vêm de arquivos JSON públicos (lista de Pokémon e tabela de tipos), carregados via HTTP na abertura do app.

## Funcionalidades

- **Lista em cards**: número, nome, ícones dos tipos e imagem de cada Pokémon, com a cor do card definida pelo tipo principal.
- **Busca em tempo real** pelo nome.
- **Barra de rolagem arrastável** para percorrer a lista rapidamente.
- **Cache de imagens** para não baixar as artes de novo a cada rolagem.
- **Ficha do Pokémon** com imagem em alta resolução, espécie, descrição, altura, peso e gênero, organizada em três abas:
  - **Status**: HP, ataque, defesa, ataque especial, defesa especial, velocidade e total, em barras na cor do tipo;
  - **Evolução**: estágio anterior e próximo, ou aviso de que o Pokémon não evolui;
  - **Vantagens**: multiplicadores de efetividade (2, 1 ou 1/2) entre o tipo do Pokémon e cada um dos demais tipos.
- **Ícones SVG** para os 18 tipos e transições de tela no estilo iOS.

## Tecnologias

- [Flutter](https://flutter.dev/) e [Dart](https://dart.dev/) (null safety, SDK `>=2.12 <3.0`)
- [http](https://pub.dev/packages/http): requisições dos dados
- [flutter_svg](https://pub.dev/packages/flutter_svg): ícones dos tipos
- [cached_network_image](https://pub.dev/packages/cached_network_image): cache das imagens
- [draggable_scrollbar](https://pub.dev/packages/draggable_scrollbar): rolagem rápida
- [flutter_launcher_icons](https://pub.dev/packages/flutter_launcher_icons): ícones do app

## Estrutura

O projeto Flutter fica dentro da pasta `pokedex-main/`:

```
pokedex-main/
├── lib/
│   ├── main.dart                   # Tema e ponto de entrada
│   ├── routes/
│   │   ├── home.dart               # Lista, busca e cards
│   │   └── pokemon_detail.dart     # Ficha, status, evolução e vantagens
│   └── services/
│       ├── api.dart                # URLs dos dados em JSON
│       └── functions.dart          # Cores por tipo, barras de status e helpers
└── assets/img/types/               # Ícones SVG dos tipos
```

## Como rodar localmente

Pré-requisito: Flutter com Dart 2.x (até o Flutter 3.7), conforme a restrição de SDK do `pubspec.yaml`.

```bash
git clone https://github.com/Lu1sR0/Pokedex.git
cd Pokedex/pokedex-main
flutter pub get
flutter run
```

Para testar no navegador: `flutter run -d chrome`.

## Créditos

Projeto de estudo baseado no app open source [Pokédex](https://github.com/johnuberbacher/pokedex) de John Uberbacher, com parte da interface traduzida para o português. Os dados vêm do repositório [pokemon_json](https://github.com/johnuberbacher/pokemon_json), do mesmo autor. Pokémon e seus nomes são marcas da Nintendo, Game Freak e The Pokémon Company.

---

<div align="center">
Desenvolvido por <a href="https://github.com/Lu1sR0">Luis Roberto</a> · <a href="https://outframe.dev">Outframe</a>
</div>
