# 🏋️ MauiAppFit

Aplicativo mobile para registrar atividades físicas, desenvolvido com **.NET MAUI** e banco de dados local **SQLite**.

---

## 📱 O que o app faz

- Cadastrar treinos com descrição, data, peso e observações
- Listar, editar e excluir atividades salvas
- Buscar atividades por descrição
- Dados salvos localmente no dispositivo (sem internet)

---

## 🗂️ Estrutura do Projeto

```
MauiAppFit/
├── Models/           → Classe Atividade (estrutura dos dados)
├── Helpers/          → Conexão e operações com o banco SQLite
├── ViewModels/       → Lógica das telas (cadastro e listagem)
└── Views/            → Telas do app (XAML)
```

---

## 📚 Conteúdos Aprendidos

### MVVM
Padrão de organização que separa o projeto em três partes: **Model** (dados), **View** (tela) e **ViewModel** (lógica). A tela não contém código de negócio — tudo fica no ViewModel.

### Data Binding
Liga um campo da tela diretamente a uma propriedade do ViewModel. Quando o valor muda em um lado, o outro atualiza automaticamente.

### INotifyPropertyChanged
Interface implementada no ViewModel para notificar a tela sempre que uma propriedade é alterada.

### ICommand
Permite conectar botões e ações da tela a métodos do ViewModel, sem escrever lógica no `.xaml.cs`.

### SQLite (sqlite-net-pcl)
Banco de dados local que salva os dados dentro do próprio dispositivo. A classe `SQLiteDatabaseHelper` centraliza todas as operações: inserir, listar, buscar, editar e excluir.

### ObservableCollection
Lista especial que atualiza o `ListView` da tela automaticamente ao adicionar ou remover itens.

### RefreshView
Componente que permite atualizar a lista puxando a tela para baixo, comportamento comum em apps mobile.

### Navegação com Shell e QueryProperty
O Shell gerencia a navegação entre telas. O `QueryProperty` permite receber parâmetros via URL ao navegar (ex: passar o `Id` de um item para a tela de edição).

### Singleton para o Banco de Dados
O banco é instanciado uma única vez em `App.xaml.cs` e compartilhado por todo o app através de `App.Database`.

### async / await
As operações com banco de dados são assíncronas para não travar a interface enquanto os dados carregam.

---

## 🛠️ Tecnologias

- .NET MAUI — framework multiplataforma
- C# — linguagem de programação
- SQLite (sqlite-net-pcl 1.9.172) — banco de dados local
- XAML — linguagem de marcação das telas

---

*Projeto acadêmico — Fatec Jahu, Desenvolvimento de Software Multiplataforma.*
