# Script para Automação de Cursos Online (Firefox + Violentmonkey)

Este script foi desenvolvido para automatizar a navegação em plataformas de cursos online, especificamente para simular cliques no botão "Próximo" em um intervalo de tempo definido, mas apenas **após o primeiro clique manual do usuário**. Isso permite um controle inicial sobre a reprodução do curso, evitando cliques automáticos indesejados antes da sua intervenção.

---

## Funcionalidades

* **Automação de Cliques:** Clica automaticamente no ícone de navegação `next.svg` em intervalos regulares.
* **Controle Humano Inicial:** O script só inicia a contagem e os cliques automáticos **depois que o usuário realiza o primeiro clique manual** no botão "Próximo". Isso garante que o usuário tenha controle sobre o início da automação.
* **Tempo Configurável:** O intervalo entre os cliques automáticos é de 20 segundos (facilmente configurável).
* **Específico para URL:** O script é configurado para rodar em uma URL específica da plataforma i9educacao.com, mas pode ser facilmente adaptado para outras páginas ou padrões de URL.

---

## Como Funciona

O script utiliza o recurso de `addEventListener` para "escutar" o clique inicial do usuário no botão `<img>` com `src="/assets/icons/next.svg"` e classe `h-6`. Uma vez detectado o primeiro clique, ele remove o ouvinte de evento e inicia um `setInterval` que simula cliques no mesmo botão a cada 20 segundos.

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
4.  **Configure a URL (se necessário):**
    * Certifique-se de que a linha `@match` no cabeçalho do script (`// @match https://i9educacao.com/watch-course/post-graduation/vf6IF7xEjnygV0J4ggce`) corresponda à URL exata da página onde você deseja que o script seja executado. Se quiser que ele funcione em múltiplas páginas de um padrão, você pode usar um coringa (`*`), por exemplo: `https://i9educacao.com/watch-course/*`.
5.  **Salve o Script:** Salve as alterações.
6.  **Ative o Script:** Certifique-se de que o script esteja habilitado (com o botão de alternância verde) na interface do Violentmonkey.
7.  **Comece a Usar:**
    * Navegue até a página configurada (`https://i9educacao.com/watch-course/post-graduation/vf6IF7xEjnygV0J4ggce`).
    * O script estará "aguardando".
    * **Clique manualmente** no botão "Próximo" (a imagem de seta).
    * Após o seu clique, o script iniciará a automação, clicando no botão a cada 20 segundos.

---

## Solução de Problemas

* **Script não inicia após o clique:** Verifique o **Console do Desenvolvedor** (pressione `F12` na página e vá na aba "Console"). Procure por mensagens de erro em vermelho ou mensagens do script (`Script Violentmonkey: ...`).
* **Botão não é encontrado:** O seletor `img[src="/assets/icons/next.svg"].h-6` é bem específico. Se o design do site mudar, este seletor pode precisar ser atualizado. Inspecione o elemento do botão "Próximo" novamente (`F12` -> "Inspetor de Elementos") para confirmar seus atributos.

---

## Contribuição

Sinta-se à vontade para abrir issues ou pull requests se tiver sugestões de melhoria ou encontrar problemas.

---
