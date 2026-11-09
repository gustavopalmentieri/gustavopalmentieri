<!-- ===== BANNER ANIMADO ===== --> <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:0E4429,100:39D353&height=200&section=header&text=Gustavo%20Palmentieri&fontSize=44&fontColor=FFFFFF&animation=twinkling&fontAlignY=36&desc=Estudante%20de%20ADS%20%E2%80%A2%20Programa%C3%A7%C3%A3o%20%E2%80%A2%20Dados&descAlignY=56&descSize=17"/> <!-- ===== TEXTO DIGITANDO ===== --> <p align="center"> <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=2800&pause=900&color=39D353&center=true&vCenter=true&width=560&lines=Ol%C3%A1%2C+eu+sou+o+Gustavo!+%F0%9F%91%8B;Programo+em+C+e+C%2B%2B;Estudando+Python+e+SQL;Rumo+%C3%A0+%C3%A1rea+de+Dados+%F0%9F%93%8A" alt="Texto animado"/> </p> <!-- ===== CONTATOS ===== --> <p align="center"> <a href="https://www.linkedin.com/in/SEU-LINKEDIN"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a> <a href="mailto:SEU-EMAIL@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"/></a> <img src="https://komarev.com/ghpvc/?username=gustavopalmentieri&label=Visitas&color=39D353&style=for-the-badge" alt="Visitas no perfil"/> </p>
💻 Sobre mim
<!-- ===== TERMINAL ANIMADO ===== --> <p align="center"> <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=500&size=16&duration=1500&pause=300&color=39D353&background=0D1117FF&center=false&vCenter=false&multiline=true&repeat=false&width=620&height=260&lines=gustavo%40dev%3A~%24+.%2Fsobre_mim;----------------------------------;Nome%3A+Gustavo+Palmentieri;Curso%3A+ADS+%28desde+2025%29;Linguagens%3A+C%2C+C%2B%2B%2C+Python;Estudando%3A+SQL%2C+Excel%2C+Power+BI;Foco%3A+Programa%C3%A7%C3%A3o+e+Dados;Local%3A+Santo+Andr%C3%A9%2C+SP;Status%3A+aberto+a+oportunidades" alt="Terminal animado"/> </p>
🧰 Tecnologias
<p align="center"><b>Uso hoje</b></p> <p align="center"> <img src="https://skillicons.dev/icons?i=c,cpp,git,github,vscode&theme=dark" alt="Tecnologias que uso"/> </p> <p align="center"><b>Estudando</b></p> <p align="center"> <img src="https://skillicons.dev/icons?i=python,mysql,js,html,css&theme=dark" alt="Tecnologias que estou estudando"/> </p>
🚀 Projetos
<!-- Troque pelos seus projetos reais. Copie um bloco para adicionar mais. -->
Projeto	O que faz	Tecnologias
Nome do projeto	Explique em uma frase	C
Nome do projeto	Explique em uma frase	C++
Nome do projeto	Explique em uma frase	Python
📈 Minha atividade
<p align="center"> <img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=gustavopalmentieri&bg_color=0D1117&color=FFFFFF&line=39D353&point=FFFFFF&area=true&area_color=39D353&hide_border=true" alt="Gráfico de atividade"/> </p> <p align="center"> <img height="165" src="https://streak-stats.demolab.com/?user=gustavopalmentieri&background=0D1117&ring=39D353&fire=39D353&currStreakLabel=39D353&hide_border=true&locale=pt_BR" alt="Sequência de contribuições"/> </p> <!-- ===== COBRINHA ANIMADA (precisa do arquivo snake.yml) ===== --> <p align="center"> <picture> <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gustavopalmentieri/gustavopalmentieri/output/github-snake-dark.svg"/> <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gustavopalmentieri/gustavopalmentieri/output/github-snake.svg"/> <img alt="Cobrinha comendo as contribuições" src="https://raw.githubusercontent.com/gustavopalmentieri/gustavopalmentieri/output/github-snake-dark.svg"/> </picture> </p> <!-- ===== RODAPÉ ANIMADO ===== --> <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:39D353,50:0E4429,100:0D1117&height=120&section=footer&animation=twinkling"/>

name: Gerar cobrinha
 
on:
  schedule:
    - cron: "0 0 * * *"   # roda todo dia
  workflow_dispatch:       # permite rodar na mão
  push:
    branches:
      - main
 
jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    steps:
      - name: Gerar a animação
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
 
      - name: Enviar para a branch output
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
 
