
# Definição do Projeto

## Analisar o arquivo ClassicHit

## Utilizar API Spotify

"O que o Spotify for Developers oferece:

A API do Spotify permite acessar dados como:

Informações sobre músicas (nome, artista, álbum, popularidade no Spotify)

Playlists (inclusive editoriais, como "Top 50 Global", etc.)

Dados do usuário (com permissão)

Álbuns e discografias

Popularidade de uma faixa (um número de 0 a 100, mas não é o ranking da Billboard)

Charts do próprio Spotify (por exemplo, “Top 50” de um país), mas não históricos detalhados"

🔗 O que dá pra fazer com a API do Spotify

Buscar metadados: confirmar informações de música, artista, álbum, capa da música.

Popularidade em tempo real: atualizar a coluna Popularity com dados atuais.

Informações extras: seguidores do artista, gênero oficial do Spotify, playlists em que a música aparece.

Áudio features: já tem na sua base (danceability, energy, etc.), mas você poderia validar/atualizar direto do Spotify.

Recomendações: sugerir músicas/artistas semelhantes.

🛠️ Como integrar com sua base

Conferir se o nome da faixa e artista batem.

Você tem Track e Artist.

Usar esses campos para buscar no endpoint /search da API do Spotify.

Pegar o track_id do Spotify.

Serve como chave única para cruzar dados.

Enriquecer seu dataset com:

Album (nome e ano exato)

Album cover (link da imagem, dá para mostrar no dashboard)

Artist followers (métrica de popularidade do artista)

Spotify Popularity (valor atualizado)

Genres oficiais do artista

Salvar uma tabela unificada: sua base original + dados vindos do Spotify.

📊 No Dashboard, isso daria:

Mostrar capas dos álbuns junto das músicas.

Ver popularidade atualizada no Spotify.

Comparar popularidade histórica (sua base) x popularidade atual.

Ranking de artistas mais seguidos.

Quais gêneros e artistas estão em alta hoje.

### Arquitetura medalhão do Databricks

- Catalog
  - Bronze (Dados brutos)
  - Prata (Dados tratatos)
  - Gold (Dados para o consumo)

