# Registro de Atividade - Otimizando a Performance Web

**Escola Manoel Ignácio** - Desenvolvimento de Sistemas - 3ª série B - 2026  
**Programação Frontend** - 3º Bimestre  
`nome@dev:~$_`

---

## 🎯 Contexto e Objetivo

Vocês foram contratados para otimizar a performance de uma aplicação web, enfrentando problemas de carregamento lento. Para isso, vocês implementarão Lazy Loading nas imagens, usarão minificação do CSS para reduzir o tamanho dos arquivos e realizarão uma análise de performance usando uma ferramenta de diagnóstico. O objetivo é aprimorar a experiência do usuário, reduzindo o tempo de carregamento e o uso de recursos.

> **Atenção:** A estrutura de código base necessária para iniciar esta atividade encontra-se em anexo ao final deste documento.

---

## 📋 Tarefas a Realizar

1. **Estrutura HTML e CSS:** Criem os arquivos `index.html` e `estilos.css` utilizando o código fornecido em anexo. Use o atributo `loading="lazy"` nas tags `<img>` para implementar Lazy Loading.

2. **Preparar imagens:** Baixem três imagens de repositórios gratuitos (como Unsplash ou Pixabay), nomeiem como `imagem1.jpg`, `imagem2.jpg` e `imagem3.jpg`, e salvem na mesma pasta.

3. **Minificar o arquivo CSS:** Instalarem o PostCSS CLI e o cssnano (`npm install postcss postcss-cli cssnano --save-dev`). Usem o arquivo de configuração `postcss.config.js` (em anexo) e executem o comando para gerar o `estilos.min.css`.

4. **Testar a página:** Usem um servidor local (Live Server no VS Code ou http-server) para abrir a página no navegador.

5. **Análise de performance:** Abram as DevTools do Chrome, vão até a aba "Lighthouse" e analisem o carregamento da página.

6. **Reflexão:** Respondam qual impacto observaram na performance, quais sugestões adicionais o Lighthouse forneceu e por que a otimização é fundamental.

---

## ⏳ Prazos e Pontuação

* **Entrega na 1ª semana (até 30 de julho):** 10 pontos de semana AVA.
* **Entrega na 2ª semana (até 7 de agosto):** 5 pontos de semana AVA.
* **Entrega após 7 de agosto:** 1 ponto de semana AVA.

---

## ✈️ Envio

* **Identificação Obrigatória:** A primeira linha do seu arquivo HTML e do relatório de reflexão deve conter seu nome completo.
* **Opções de envio no AVA:** Cole a captura de tela dos resultados (Lighthouse e terminal), envie o arquivo da captura, ou copie os códigos alterados e as respostas e cole-os diretamente no documento.

---

## Anexo: Código Base Inicial

### CÓDIGO HTML (`index.html`)

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="estilos.css">
  <title>Otimizando a Performance Web</title>
</head>
<body>
  <!-- Digite seu nome completo na linha 1 do arquivo -->
  <h1>Galeria Otimizada de Imagens</h1>

  <main>
    <img src="imagem1.jpg" alt="Imagem 1" loading="lazy">
    <img src="imagem2.jpg" alt="Imagem 2" loading="lazy">
    <img src="imagem3.jpg" alt="Imagem 3" loading="lazy">
  </main>
</body>
</html>
```

### CÓDIGO CSS (`estilos.css`)

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  flex-direction: column;
  align-items: center;
}

h1 {
  color: #333;
}

img {
  max-width: 300px;
  margin: 10px;
}
```

### CÓDIGO JS (`postcss.config.js`)

```javascript
module.exports = {
  plugins: [
    require('cssnano')({
      preset: 'default',
    }),
  ],
};
```
