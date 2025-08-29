
# Template de Dissertação – Quarto + R/RStudio

> **ATENÇÃO (leia primeiro):** este README é um **guia inicial**.  

> Assim que você criar o seu repositório a partir deste template e 
clonar o **seu** repositório, **apague todo o conteúdo deste arquivo** e 
passe a usar este próprio arquivo `README.md`** para 
**documentar a evolução do seu trabalho** 
 
> Você pode acessar estas instruções iniciais deste template, acessando 
este repositório do template original no GitHub.

> Para facilitar, forneço por e-mail um **modelo de README do orientando** 
como uma referência inicial para você adaptar e usar.




## Visão geral

Este repositório fornece um **template de dissertação** do Mestrado 
Profissional em Administração do IFMG - Campus Formiga que gera um 
arquivo **dpf** usando **Sistema Quarto** + **R** + **LaTeX**.  

A parte **pré-textual** (capa, folha de rosto, ficha catalográfica, 
dedicatória (opcional), resumo/abstract, agradecimentos (opcional) é controlada 
pelo arquivo`pre_textuais.tex`.  

O **corpo** (capítulos/seções) é escrito em `template_dissertacao.qmd`.




## Requisitos (Windows e macOS)

- **Linguagem R**  
- IDE **RStudio**  
- **Sistema Quarto**: <https://quarto.org>  
- **LaTeX** (recomendado **TinyTeX**):

  - Abra um terminal e execute:  
  
    ```bash
    quarto install tinytex
    ```

### Observações para **Windows**

- Recomendo instalar **Rtools**: <https://cran.r-project.org/bin/windows/Rtools/> 

- Não utilize caminhos muito longos e com espaços/acentos no caminho 
  do projeto.  




## Como começar?

**Opção A (no GitHub):**

1. Clique em **Use this template** (no topo deste repositório).

2. Crie **seu** repositório a partir deste modelo, utilize um 
nome apropriado (ex.: `dissertacao-joao-silva`).

3. Clone **seu** repositório localmente (via Git Bash). 

4. Abra o projeto no RStudio (`template_dissertacao.Rproj`).

5. Comece a editar.


**Opção B (no RStudio):**

1. *File → New Project → Version Control → Git*  
2. Cole a URL do **seu** repositório (criado a partir do template).  
3. Escolha a pasta local e conclua.


**Primeira renderização (no terminal Git Bash do projeto):**

```bash
quarto render template_dissertacao.qmd
```

O PDF será gerado na raiz do projeto (por padrão, **não é versionado**).




## Estrutura dos arquivos

- `template_dissertacao.qmd` — documento principal (capítulos).

- `pre_textuais.tex` — elementos **pré-textuais** 
(capa, rosto, ficha catalográfica, dedicatória, agradecimentos,
resumo, abstract, ).

- `referencias.bib` — base bibliográfica (BibTeX).

- `associacao-brasileira-de-normas-tecnicas-ipea.csl` — estilo ABNT (CSL).

- `template_dissertacao.Rproj` — arquivo do projeto RStudio (**é versionado**).

- `entregas/` — use para **versões parciais/final** do PDF 

> Observação: o `.gitignore` está configurado para ignorar caches e
PDFs gerados, o que é uma boa prática para evitar conflitos durante a 
colaboração.




## Boas práticas de versionamento

- **Versione somente arquivos fontes**: `.qmd`, `.tex`, `.bib`, `.csl`, `.Rproj`.
- **Não** versione PDFs gerados
- Faça *commits* frequentes e mensagens descritivas.
- Evite renomear arquivos sem necessidade (quebra links e referências).




## Problemas comuns (FAQ rápido)

- **Erro de LaTeX/falta de pacote**: instale o **TinyTeX** 
(`quarto install tinytex`) ou o pacote ausente que o erro indicar.

- **Caminhos com acentos/espaços** (sobretudo no Windows): evite; mova o 
projeto para um caminho simples (ex.: `C:\projetos\minha-dissertacao`).

- **Imagens não aparecem**: verifique caminho relativo e extensão (`figs/…`).

- **Citações não resolvem**: confira a chave BibTeX em 
`referencias.bib` e a sintaxe para citações com o sistema Quarto.




## Próximos passos (sugestão de roteiro)

1. Leia e entenda `pre_textuais.tex` (personalize capa, rosto, dedicatória, 
   resumo/abstract).
   
2. Escreva os capítulos no `template_dissertacao.qmd`.

3. Adicione suas referências em `referencias.bib`. Mantenha este 
arquivo organizado (usando espaços e formatação adequada) ou use um 
gerenciador de referências (ex.: Zotero, Mendeley).

4. Gere versões de leitura (`quarto render`) e, quando necessário, 
exporte o PDF final para a pasta `entregas/`.




**IMPORTANTE: Substitua este README agora pelo modelo que forneci**


