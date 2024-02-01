Esse aplicativo tem a função de gerir torneios de Skat (jogo de baralho)
Eventualmente, também pode ser usado para gestão de outros torneios de jogos de carta similares.

Ele não é uma aplicação 100% autônoma, pois requer algum leitor e editor de arquivos .CSV para funcionar corretamente.

O botão "Start Championship" cria um diretório para o novo campeonato. Para criar um novo campeonato, o usuário deve 
determinar o nome do torneio. O diretório criado terá o mesmo nome do torneio.

Além disso, o usuário deve determinar o número de séries aleatórias e rankeadas ao criar o torneio.
As séries aleatórias, definidas de antemão pelo algoritmo de mesas, estabelece "blinds" para completar um número
múltiplo de 4 para a criação das mesas. Os jogadores são divididos em 4 grupos de mesma quantidade 
(se não for múltiplo de 4, agrega-se os blinds) de acordo com a ordem em que são inseridos na lista players.csv,
de onde o sistema puxará os dados para montar as séries aleatórias.

Dessa forma, supondo um torneio de 40 jogadores, o grupo 1 reunirá jogadores de player_id 1 a 10, grupo 2 de 11 a 20,
21-30, 31-40. Jogadores de um mesmo grupo não se enfrentar em uma mesma mesa, então o organizador deve estar atento
aos quartis da lista. Não pode haver jogadores com um mesmo player_id na lista players.csv.

O botão "Add Results to Ranking" abre o navegador de arquivos e supõe que o usuário escolherá uma série para agregar
seus resultados ao documento ranking.csv que estará contido no mesmo diretório. O programa selecionará o player_id de 
cada linha, os pontos e jogos perdidos e enviará para a planilha ranking.csv.

O botão "New Ranked List" cria uma lista rankeada a partir dos ranking geral, ou de uma lista específica.
Basta que o usuário escolha o arquivo .csv a partir do qual quererá criar a lista rankeada. Se for a partir
de um ranking.csv, ele puxará da coluna "total", se for de uma série, ele puxará da coluna "points".