# 🎬 Dual Play - Projeto Luna Labs

Este repositório contém projetos experimentais e ferramentas desenvolvidas pela Luna Labs.

## 📁 Estrutura do Projeto

### 🎥 Dual Video Player
Um player de vídeos YouTube sincronizado e responsivo criado em HTML/JavaScript puro.

**Arquivo:** `dual_video_player.html`

#### ✨ Características:
- **Sincronização Perfeita**: Play/pause simultâneo em ambos os vídeos
- **Controles Independentes**: Volume e mute individual para cada vídeo
- **Design Responsivo**: Funciona perfeitamente em desktop, tablet e mobile
- **Interface Moderna**: Design glassmorphism com gradientes e animações
- **Controles de Navegação**: Avanço/retrocesso de 5s e 10s
- **Atalhos de Teclado**: Controle rápido via teclado
- **Arquivo Único**: Tudo em um HTML standalone

#### 🎮 Controles:
- **Play/Pause**: Botão central ou `Espaço`
- **Navegação**: Botões ±5s/±10s ou `Setas ← →`
- **Volume**: Sliders individuais para cada vídeo
- **Mute Rápido**: Botões de tap rápido ou teclas `1`/`2`

#### 🚀 Como Usar:
1. Abra o arquivo `dual_video_player.html` em qualquer navegador moderno
2. Aguarde o carregamento dos players do YouTube
3. Use os controles para sincronizar e controlar os vídeos
4. Aproveite a experiência sincronizada!

---

### 📱 My App
Aplicação Next.js com componentes modernos.

**Pasta:** `my_app/`

---

### 📚 Documentação
Documentação completa do projeto e tutoriais.

**Pasta:** `docs/`

---

## 🛠️ Tecnologias Utilizadas

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **APIs**: YouTube IFrame Player API
- **Design**: CSS Grid, Flexbox, Gradientes, Backdrop Filter
- **Responsividade**: Media Queries, Mobile-First
- **Interatividade**: Event Listeners, Keyboard Shortcuts

## 🎯 Recursos Avançados

### 🎨 Design System
- **Glassmorphism**: Efeitos de vidro com backdrop-filter
- **Gradientes**: Cores modernas e vibrantes
- **Animações**: Micro-interações e feedback visual
- **Tipografia**: Hierarquia clara e legibilidade

### ⚡ Performance
- **API Otimizada**: Carregamento assíncrono da YouTube API
- **Sincronização Inteligente**: Algoritmo de média temporal
- **Estados de Loading**: Feedback visual durante carregamento
- **Error Handling**: Tratamento robusto de erros

### 📱 Responsividade
- **Mobile-First**: Design otimizado para dispositivos móveis
- **Breakpoints**: 768px (tablet) e 480px (mobile)
- **Touch-Friendly**: Botões e controles otimizados para touch
- **Orientação**: Funciona em portrait e landscape

## 🔧 Configuração

### Personalização de Vídeos
Para alterar os vídeos, edite as constantes no JavaScript:

```javascript
const VIDEO_IDS = {
    video1: 'SEU_VIDEO_ID_1',
    video2: 'SEU_VIDEO_ID_2'
};
```

### Customização de Estilo
Todas as variáveis CSS estão organizadas no início do arquivo para fácil customização:
- Cores e gradientes
- Espaçamentos e dimensões  
- Animações e transições
- Breakpoints responsivos

## 🎪 Demonstração

O player suporta os seguintes vídeos por padrão:
- **Vídeo 1**: [YouTube Link](https://www.youtube.com/watch?v=bW_W7hSW_-0)
- **Vídeo 2**: [YouTube Link](https://www.youtube.com/watch?v=PRCdUkQQuAs)

## 🤝 Contribuição

Sinta-se à vontade para contribuir com melhorias, correções de bugs ou novas funcionalidades!

## 📄 Licença

Este projeto está sob licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

---

**Desenvolvido com �� pela Luna Labs**
