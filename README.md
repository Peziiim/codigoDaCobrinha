# codigoDaCobrinha
codigo da animação da cobrinha no meu perfil
<h1>Copie e cole no seu READ.ME</h1>
<h4>Lembre de trocar o nome de usuário na URL</h4>

```
 <picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Peziiim/Peziiim/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Peziiim/Peziiim/output/github-contribution-grid-snake.svg">
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/Peziiim/Peziiim/output/github-contribution-grid-snake.svg">
  </picture>
```

<h1>Copie e cole no workflow</h1>

```
name: generate animation

on:
  schedule:
    
cron: "0 /24 * *" 


  workflow_dispatch:


  push:
    branches:
    
master


jobs:
  generate:
    permissions: 
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
 
      
name: generate github-contribution-grid-snake.svg
      uses: Platane/snk/svg-only@v3
      with:
        github_user_name: ${{ github.repository_owner }}
        outputs: |
          dist/github-contribution-grid-snake.svg
          dist/github-contribution-grid-snake-dark.svg?palette=github-dark

name: push github-contribution-grid-snake.svg to the output branch
uses: crazy-max/ghaction-github-pages@v3.1.0
with:
  target_branch: output
  build_dir: dist
env:
  GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

```

<h1>Tutorial Completo</h1>
<h4><a href="https://github.com/GabrielaZanetti/animacaoCobrinha"> Tutorial</a></h4>
