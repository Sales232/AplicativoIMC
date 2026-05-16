# 📱 IMCapp — Calculadora de IMC

Projeto criado para a disciplina de **Desenvolvimento de Aplicativos Mobile** do **CENTRO UNIVERSITÁRIO DE DESENVOLVIMENTO DO CENTRO-OESTE**. Um aplicativo mobile desenvolvido em React Native com Expo para cálculo do Índice de Massa Corporal (IMC) e consulta de informações nutricionais de alimentos.

---

## 🎯 Funcionalidades

- **Calculadora de IMC:** Insira peso e altura para calcular seu IMC com classificação visual por cores
- **Tabela Alimentar:** Busque informações nutricionais detalhadas de alimentos em português ou inglês
- **Tradução automática:** Suporte a nomes de alimentos em PT-BR com tradução automática para consulta na API
- **Classificação do IMC:** Tabela completa com faixas de peso (abaixo do peso, normal, sobrepeso, obesidade)
- **Navegação por abas:** Interface com quatro telas organizadas em tabs

---

## 🚀 Tecnologias

- **React Native:** Framework principal para desenvolvimento mobile
- **Expo (SDK):** Plataforma de desenvolvimento e build
- **Expo Router:** Navegação baseada em arquivos
- **TypeScript:** Tipagem estática para maior segurança
- **API Ninjas — Nutrition:** API externa para dados nutricionais dos alimentos

---

## 📋 Pré-requisitos

- Node.js 18 ou superior
- npm ou yarn
- Expo CLI
- Expo Go (no celular) ou emulador Android/iOS

---

## 💾 Instalação

1. Clone o repositório:

```bash
git clone https://github.com/seu-usuario/IMCapp.git
cd IMCapp
```

2. Instale as dependências:

```bash
npm install
```

3. Inicie o servidor de desenvolvimento:

```bash
npx expo start
```

4. Abra o app:
   - **Android/iOS:** Escaneie o QR Code com o aplicativo **Expo Go**
   - **Emulador Android:** Pressione `a` no terminal
   - **Simulador iOS:** Pressione `i` no terminal
   - **Web:** Pressione `w` no terminal

---

## ▶️ Como Usar

1. **Tela Início:** Apresentação do app com botão para começar
2. **Calculadora:** Insira seu peso (kg) e altura (m) e toque em "Calcular" para ver seu IMC e classificação
3. **Tabela Alimentar:** Digite o nome de um alimento (ex: `banana`, `frango`, `arroz`) e toque em "Buscar" para ver informações nutricionais como carboidratos, gorduras, fibras, açúcares e sódio
4. **Sobre:** Tabela de classificação do IMC e informações sobre o app

---

## 📁 Estrutura do Projeto

```
IMCapp/
├── app/
│   ├── (tabs)/
│   │   ├── _layout.tsx          # Configuração das abas de navegação
│   │   ├── TelaHome.tsx          # Tela inicial
│   │   ├── TelaCalculadora.tsx   # Calculadora de IMC
│   │   ├── TelaAlimentos.tsx     # Busca de informações nutricionais
│   │   └── TelaInformacoes.tsx   # Sobre o app e tabela de classificação
│   ├── src/
│   │   └── services/
│   │       └── foodApi.ts        # Integração com a API Ninjas Nutrition
│   ├── +not-found.tsx            # Tela de rota não encontrada
│   └── modal.tsx                 # Tela modal
├── components/
│   ├── Themed.tsx                # Componentes com suporte a tema claro/escuro
│   ├── EditScreenInfo.tsx        # Componente de informações de tela
│   ├── ExternalLink.tsx          # Link externo com in-app browser
│   ├── StyledText.tsx            # Texto com fonte customizada
│   ├── useClientOnlyValue.ts     # Hook para valores client-only
│   └── useColorScheme.ts         # Hook para esquema de cores
├── constants/
│   └── Colors.ts                 # Paleta de cores do app
├── assets/
│   └── images/                   # Ícones e imagens do app
├── app.json                      # Configuração do Expo
└── package.json                  # Dependências do projeto
```

---

## 🌐 Integração com API

O app utiliza a [API Ninjas — Nutrition](https://api-ninjas.com/api/nutrition) para buscar dados nutricionais.

**Endpoint utilizado:**

```
GET https://api.api-ninjas.com/v1/nutrition?query={alimento}
```

**Campos retornados por alimento:**

| Campo | Descrição |
|---|---|
| `name` | Nome do alimento |
| `serving_size_g` | Tamanho da porção (g) |
| `carbohydrates_total_g` | Carboidratos totais (g) |
| `fat_total_g` | Gorduras totais (g) |
| `fiber_g` | Fibras (g) |
| `sugar_g` | Açúcares (g) |
| `sodium_mg` | Sódio (mg) |

---

## 📊 Classificação do IMC

| IMC | Classificação |
|---|---|
| Abaixo de 18,5 | Abaixo do peso |
| 18,5 – 24,9 | Peso normal |
| 25,0 – 29,9 | Sobrepeso |
| Acima de 30,0 | Obesidade |

---

## 🛠️ Scripts Disponíveis

```bash
# Iniciar em modo de desenvolvimento
npx expo start

# Build para Android
npx expo build:android

# Build para iOS
npx expo build:ios

# Executar testes
npm test

# Verificar tipos TypeScript
npx tsc --noEmit
```

---

## 👥 Autores

- **Anthony de Melo**
- **Pedro Sales**

**Professor:** Karithon Gomes

---

## 🤝 Contribuições

Contribuições são bem-vindas! Para contribuir:

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/NovaFuncionalidade`)
3. Commit suas mudanças (`git commit -m 'Add: nova funcionalidade'`)
4. Push para a branch (`git push origin feature/NovaFuncionalidade`)
5. Abra um Pull Request

---

## 📬 Contato

Para dúvidas ou sugestões, abra uma [issue](https://github.com/seu-usuario/IMCapp/issues) no repositório.

---

**Status: Em Desenvolvimento 🚧**
