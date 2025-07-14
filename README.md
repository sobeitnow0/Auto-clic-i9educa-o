# Script para Automação de Cursos Online (Firefox + Violentmonkey)

Este script foi desenvolvido para automatizar a navegação em plataformas de cursos online, especificamente para simular cliques no botão "Próximo" em um intervalo de tempo definido.

---

## Funcionalidades

* **Automação de Cliques:** Clica automaticamente no ícone de navegação `next.svg` em intervalos regulares.
* * **Tempo Configurável:** O intervalo entre os cliques automáticos é de 20 segundos (facilmente configurável).
* **Específico para URL:** O script é configurado para rodar em uma URL específica da plataforma i9educacao.com.

---

## Como Funciona

O script inicia um `setInterval` que simula cliques no mesmo botão a cada 20 segundos.

---

## Pré-requisitos

* **Mozilla Firefox** (Navegador)
* **Violentmonkey** (Extensão de navegador para gerenciar User Scripts)

---

## Instalação e Uso

1.  **Instale Violentmonkey:** Se ainda não tiver, adicione a extensão Violentmonkey ao seu Firefox através da [loja de addons do Firefox](https://addons.mozilla.org/firefox/addon/violentmonkey/).
2.  **Crie um Novo Script:**
    * Clique no ícone do Violentmonkey na barra de ferramentas do seu navegador.
    * Selecione **"New script"** (Novo script).
3.  **Cole o Código:** Apague todo o conteúdo padrão no editor e cole o código completo do script.
4.  * **Clique manualmente** no botão "Próximo" (a imagem de seta).
    * Após o seu clique, o script iniciará a automação, clicando no botão a cada 20 segundos.

---

## Contribuição

Sinta-se à vontade para abrir issues ou pull requests se tiver sugestões de melhoria ou encontrar problemas.

---
