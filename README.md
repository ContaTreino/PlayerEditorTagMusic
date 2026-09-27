# WAVE local

## Instalar
Este projeto só funciona a partir de um clone git — não baixe o `.zip` nem copie os arquivos soltos, pois o app recusa iniciar se não encontrar uma pasta `.git` no diretório.
```
git clone <url-do-repositorio>
cd <pasta-do-repositorio>
pip install -r requirements.txt
```
ffmpeg precisa estar instalado no sistema (`ffmpeg -version` para conferir).

## Rodar
```
python3 app.py
```
Abra http://localhost:5000 — na primeira execução, toque em "＋ Pasta" e selecione a pasta com suas músicas (mp3/flac/m4a/wav/ogg/opus/wma/aac). É possível adicionar mais de uma pasta; todas ficam salvas em `library_dirs`, dentro de `config.json`. As faixas são sempre lidas direto de onde estão — nada é copiado para dentro do projeto.

## Organização automática
O app detecta sozinho se cada pasta adicionada é "uma biblioteca inteira" (Artista/Álbum/faixa) ou "um álbum/playlist só" (faixas soltas ou numa única camada de subpastas), e usa a estrutura de pastas para montar Artista e Álbum/Playlist, com reforço das tags do arquivo quando a pasta não define isso.

## Editar tags
Toque no ícone de lápis em qualquer música (ou na tela do player) para editar título, artista, álbum, gênero, ano, nº da faixa, capa e letra embutida. Dá para usar "🔎 Identificar no Deezer" para preencher os campos automaticamente. A gravação é feita via ffmpeg, sem reencodar o áudio.

## Créditos
Desenvolvido por **Edivaldo Silva (773H-🧓)**.