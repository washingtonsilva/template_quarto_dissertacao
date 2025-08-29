# Template de Dissertação de Mestrado Profissional em Administração

> **⚠️ ATENÇÃO - LEIA PRIMEIRO:** 
> 
> Este README é um **guia inicial** para configuração do template.
> 
> **Após criar seu repositório** a partir deste template:
> 1. Clone **seu** repositório (não este template)
> 2. **Apague todo o conteúdo deste arquivo README.md**
> 3. Use este arquivo para **documentar a evolução do seu trabalho**
> 
> 📧 **Modelo de README para orientandos:** será enviado por e-mail como 
referência inicial.

---

## Visão Geral

Template para dissertação do [Mestrado Profissional em Administração do IFMG - Campus Formiga](https://formiga.ifmg.edu.br/mestrado) 
que gera um arquivo pdf usando:

- **Quarto** (sistema de publicação científica)
- **R** (linguagem para análise de dados)  
- **LaTeX** (formatação profissional)

### Estrutura do documento:

- **Elementos pré-textuais**: controlados por `pre_textuais.tex`
- **Corpo da dissertação**: escrito em `template_dissertacao.qmd`

---

## Instalação e Configuração

### Pré-requisitos obrigatórios:

1. **Linguagem R** (versão 4.0+): <https://cran.r-project.org/>
2. **RStudio Desktop**: <https://posit.co/download/rstudio-desktop/>
3. **Sistema Quarto**: <https://quarto.org/docs/get-started/>


### Instalação de uma distribuição LaTeX (obrigatório):

Abra o **terminal** (macOS) ou **Prompt de Comando** (Windows) e execute:

```bash
quarto install tinytex
```

### Configurações específicas por sistema:

#### Windows:

- **Instale Rtools**: <https://cran.r-project.org/bin/windows/Rtools/>

- **Evite caminhos com**:
  - Espaços: `C:\Meus Documentos\` ❌
  - Acentos: `C:\João\` ❌  
  - **Use**: `C:\projetos\dissertacao\` ✅


### Verificação da instalação:

Abra o RStudio e execute no console:

```r
# Verificar versões
R.version.string
quarto::quarto_version()

# Testar LaTeX
tinytex::is_tinytex()
```

---

## Como Utilizar este Template?

### Opção: Via GitHub (recomendada)

1. **Crie seu repositório**:

   - Clique em **"Use this template"** (botão verde) 
   - Nome sugerido para seu repositório: `dissertacao-joao-silva`
   - Defina como **privado** (recomendado)

2. **Clone localmente:** Caso utilize Windows:

- Abra o Windows Explorer e navegue até a pasta na qual deseja salvar 
a pasta do repositório. 

- Clique no botão direito do mouse e selecione "Git Bash Here", depois 
execute: 

```bash
# Substitua SEU-USUARIO e SEU-REPOSITORIO pelos seus dados 
git clone https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
```

3. Abra o RStudio e, em seguida, abra o arquivo do projeto (`.Rproj`.)



### Primeiros passos após instalação:

1. **Teste a renderização**: Pelo terminal do RStudio, execute:

```bash
quarto render template_dissertacao.qmd
```

2. **Personalize informações básicas** em `pre_textuais.tex`:

   - Nome do autor
   - Título da dissertação
   - Nome do orientador
   - Data

---

## 📁 Estrutura dos Arquivos

| Arquivo | Descrição |
|---------|-----------|
| `template_dissertacao.qmd` | **Documento principal** - corpo da dissertação |
| `pre_textuais.tex` | **Elementos pré-textuais** (capa, resumo, etc.) |
| `referencias.bib` | **Bibliografia** em formato BibTeX |
| `associacao-brasileira-de-normas-tecnicas-ipea.csl` | **Estilo ABNT 2023** |
| `template_dissertacao.Rproj` | **Projeto RStudio** (versionado) |
| `entregas/` | **Pasta para PDFs finais** (crie conforme necessário) |

### Pastas importantes:

- `figs/` - Imagens e gráficos externos e elaborados.
- `dados/` - arquivos de dados
- `scripts/` - Scripts R auxiliares

---

## Workflow Recomendado

### Desenvolvimento diário:

1. **Abra o RStudio e seu projeto**:
2. **Edite o conteúdo**: `template_dissertacao.qmd`
3. **Renderize**: `Ctrl+Shift+K` ou botão "Render"
4. **Commit frequente**: salvar progresso no Git

### Entregas importantes:

1. **Gerar PDF final**: `quarto render`
2. **Copiar para pasta entregas**: `entregas/dissertacao_v1.pdf`
3. **Commit e push**: sincronizar com GitHub

---

## Boas Práticas

### Versionamento (Git):

✅ **Versione sempre**:

- `.qmd`, `.tex`, `.bib`, `.csl`, `.Rproj`
- Scripts R personalizados
- Dados pequenos (< 100MB)

❌ **NÃO versione**:

- PDFs gerados automaticamente
- Cache do Quarto (`_freeze/`)
- Dados temporários

### Organização:

- **Commits descritivos**: "Adiciona seção de metodologia" em vez de "update"
- **Backup regular**: push para GitHub frequentemente
- **Versões importantes**: use tags Git para marcos importantes

### Escrita:

- **Seções pequenas**: escreva incrementalmente
- **Renderize frequentemente**: detecte erros rapidamente
- **Referências organizadas**: mantenha `.bib` limpo

---

## Soluções para Problemas Comuns

### Erro de LaTeX/pacotes faltando:

```bash
# Reinstalar TinyTeX
quarto uninstall tinytex
quarto install tinytex

# Instalar pacote específico
tlmgr install NOME_DO_PACOTE
```

### Imagens não aparecem:

- Verifique caminho relativo: `figs/imagem.png` ✅
- Formatos suportados: PNG, JPG, PDF

### Citações não funcionam:

- Verificar se a chave BibTeX existe em `referencias.bib`
- Sintaxe correta no quarto: `[@chave2023]` ou `@chave2023`, etc.

### Performance lenta:

```r
# Limpar cache do Quarto
quarto::quarto_render("template_dissertacao.qmd", cache_refresh = TRUE)
```

---

## Cronograma Sugerido

### Fase 1 - Configuração (1ª semana):

- [ ] Instalar todas as dependências
- [ ] Criar e clonar repositório
- [ ] Testar renderização inicial
- [ ] Personalizar elementos pré-textuais

### Fase 2 - Desenvolvimento:

- [ ] Adicionar referências principais ao `.bib`
- [ ] Escrever capítulos incrementalmente
- [ ] Renderizar e revisar semanalmente

### Fase 3 - Finalização:

- [ ] Revisão completa dos elementos pré-textuais
- [ ] Formatação final e ajustes
- [ ] Gerar versão final para entrega


