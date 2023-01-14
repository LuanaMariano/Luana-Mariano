# Luana-Mariano
Olá, Luana aqui.

## Hi, my name is Luana Mariano, I'm a pedagogy student!
<div align="center">
  <a href="https://github.com/LuanaMariano/">
  <img height="150em" src="https://github-readme-stats.vercel.app/api?username=LuanaMariano&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
  <img height="150em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=LuanaMariano&layout=compact&langs_count=7&theme=dracula"/>
</div>
<div style="display: inline_block"><br>
  <img align="center" alt="Luana-html" height="30" width="40" src="https://cdn-icons-png.flaticon.com/512/919/919827.png">
  <img align="center" alt="Luana-Css" height="30" width="40" src="https://cdn-icons-png.flaticon.com/512/919/919826.png">
  
 
<div>
  <a href="https://www.linkedin.com/in/joaovitordev/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  <a href = "mailto:joaovitorti07@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://https://instagram.com/unnamed.lm?igshid=YmMyMTA2M2Y=" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
 
  ![Snake animation](https://github.com/LuanaMariano/LuanaMariano/blob/output/github-contribution-grid-snake.svg)
 
</div>
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: windows11-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: LuanaMariano
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
