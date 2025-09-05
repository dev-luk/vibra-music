# 🎵 VibraMusic

**Música através de Vibrações para Pessoas Surdas e com Deficiência Auditiva**

## 📖 Sobre o Projeto

O VibraMusic é uma aplicação web inovadora que transforma arquivos de música MIDI em padrões de vibração, permitindo que pessoas surdas e com deficiência auditiva possam "sentir" a música através do tato. O projeto utiliza a API de vibração nativa dos dispositivos móveis para criar uma experiência sensorial única.

## 🎯 Objetivo

Promover a **inclusão digital** e **acessibilidade** no mundo da música, oferecendo uma nova forma de experienciar arte sonora através de tecnologia assistiva.

## ✨ Funcionalidades

### 🔧 Principais Recursos
- **Upload de arquivos MIDI** (.mid, .midi)
- **Conversão de notas musicais em vibrações**
- **Controle de intensidade personalizável** (50ms a 300ms)
- **Interface totalmente acessível**
- **Design responsivo** para todos os dispositivos
- **Feedback visual em tempo real**

### ♿ Recursos de Acessibilidade
- Interface visual clara com alto contraste
- Navegação por teclado completa
- Textos explicativos e descritivos
- Ícones intuitivos e botões grandes
- Feedback sonoro e visual
- Compatibilidade com leitores de tela

## 🛠️ Tecnologias Utilizadas

### Frontend
- **React 18** - Biblioteca para interface de usuário
- **TypeScript** - Tipagem estática para JavaScript
- **Tailwind CSS** - Framework de estilos utilitários
- **Lucide React** - Ícones modernos e acessíveis

### APIs Nativas
- **Vibration API** - Para controle de vibrações do dispositivo
- **File API** - Para upload e leitura de arquivos
- **Web Audio API** - Para processamento de áudio (futuro)

### Ferramentas de Desenvolvimento
- **Vite** - Build tool e servidor de desenvolvimento
- **ESLint** - Linting de código
- **PostCSS** - Processamento de CSS

## 🚀 Como Executar o Projeto

### Pré-requisitos
- Node.js 16+ instalado
- Navegador moderno com suporte à Vibration API
- Dispositivo móvel para testar vibrações

### Instalação
```bash
# Clone o repositório
git clone [url-do-repositorio]

# Entre na pasta do projeto
cd vibramusic

# Instale as dependências
npm install

# Execute o servidor de desenvolvimento
npm run dev
```

### Uso
1. Abra o projeto no navegador (preferencialmente em um dispositivo móvel)
2. Clique em "Selecionar arquivo MIDI"
3. Escolha um arquivo .mid ou .midi do seu dispositivo
4. Ajuste a intensidade da vibração conforme sua preferência
5. Clique em "Tocar com Vibração" para iniciar a experiência
6. Use "Parar" para interromper a reprodução

## 📱 Compatibilidade

### Navegadores Suportados
- ✅ Chrome/Chromium (Android)
- ✅ Firefox (Android)
- ✅ Samsung Internet
- ❌ Safari (iOS) - Não suporta Vibration API
- ❌ Navegadores desktop - Vibração limitada

### Dispositivos Recomendados
- Smartphones Android
- Tablets Android com vibração
- Qualquer dispositivo com suporte à Vibration API

## 🎓 Aspectos Educacionais

### Conceitos Demonstrados
1. **Acessibilidade Web** - WCAG 2.1, ARIA, navegação por teclado
2. **APIs Nativas** - Vibration API, File API
3. **React Moderno** - Hooks, componentes funcionais, TypeScript
4. **Design Responsivo** - Mobile-first, Tailwind CSS
5. **Inclusão Digital** - Tecnologia assistiva, UX inclusivo

### Estrutura do Código
```
src/
├── components/          # Componentes React organizados
│   ├── Header.tsx      # Cabeçalho da aplicação
│   ├── IntroSection.tsx # Seção explicativa
│   ├── PlayerSection.tsx # Player principal (core)
│   ├── AccessibilityInfo.tsx # Informações de acessibilidade
│   └── Footer.tsx      # Rodapé
├── App.tsx             # Componente principal
├── main.tsx           # Ponto de entrada
└── index.css          # Estilos globais
```

## 🔬 Como Funciona (Técnico)

### 1. Upload de Arquivo
```typescript
// Validação de arquivo MIDI
const handleFileUpload = (event: React.ChangeEvent<HTMLInputElement>) => {
  const file = event.target.files?.[0];
  if (file && (file.name.endsWith('.mid') || file.name.endsWith('.midi'))) {
    setSelectedFile(file);
    // Arquivo válido carregado
  }
};
```

### 2. Processamento MIDI (Simulado)
```typescript
// Padrão de vibração baseado em notas musicais
const musicPattern = [
  vibrationIntensity,     // Nota musical
  100,                    // Pausa/silêncio
  vibrationIntensity * 0.7, // Nota mais fraca
  150,                    // Pausa maior
  // ... mais padrões
];
```

### 3. Controle de Vibração
```typescript
// Execução do padrão de vibração
const playPattern = () => {
  if (patternIndex % 2 === 0) {
    // Índice par = vibração (nota musical)
    navigator.vibrate(duration);
  }
  // Índice ímpar = pausa (silêncio)
  setTimeout(playPattern, duration + 50);
};
```

## 🎯 Melhorias Futuras

### Versão 2.0
- [ ] Parser real de arquivos MIDI
- [ ] Diferentes padrões de vibração por instrumento
- [ ] Visualização gráfica da música
- [ ] Salvamento de preferências do usuário
- [ ] Biblioteca de músicas pré-carregadas

### Versão 3.0
- [ ] Modo colaborativo (múltiplos usuários)
- [ ] Integração com streaming de música
- [ ] Suporte a outros formatos (MP3, WAV)
- [ ] Aplicativo móvel nativo
- [ ] Dispositivos de vibração externos

## 🤝 Contribuindo

Este projeto foi desenvolvido com fins educacionais e de inclusão. Contribuições são bem-vindas!

### Como Contribuir
1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 👥 Créditos

- **Desenvolvimento**: [Seu Nome]
- **Conceito**: Inclusão digital e acessibilidade
- **Inspiração**: Comunidade surda e tecnologia assistiva
- **Ícones**: Lucide React
- **Estilos**: Tailwind CSS

## 📞 Contato

Para dúvidas, sugestões ou colaborações:
- Email: [seu-email]
- GitHub: [seu-github]
- LinkedIn: [seu-linkedin]

---

**"Música para todos através da tecnologia"** 🎵❤️