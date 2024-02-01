This application serves to manage Skat (a card game) tournaments. It can also be used for managing other similar card game tournaments.

It is not a 100% autonomous application, as it requires some CSV file reader and editor to function correctly.

The "Start Championship" button creates a directory for the new championship. To create a new championship, the user must determine the tournament's name. The created directory will have the same name as the tournament.

Additionally, the user must determine the number of random and ranked series when creating the tournament. The random series, predefined by the table algorithm, establishes "blinds" to complete a multiple of 4 for the creation of tables. Players are divided into 4 groups of equal quantity (if it's not a multiple of 4, blinds are added) according to the order they are inserted into the players.csv list, from where the system will pull the data to assemble the random series.

Thus, assuming a tournament of 40 players, group 1 will gather players from player_id 1 to 10, group 2 from 11 to 20, 21-30, 31-40. Players from the same group will not face each other at the same table, so the organizer must pay attention to the quartiles of the list. There cannot be players with the same player_id in the players.csv list.

The "Add Results to Ranking" button opens the file browser and assumes that the user will choose a series to add their results to the ranking.csv document contained in the same directory. The program will select the player_id of each line, the points, and lost games and send them to the ranking.csv spreadsheet.

The "New Ranked List" button creates a ranked list from the general ranking or a specific list. The user simply chooses the .csv file from which they want to create the ranked list. If it is from a ranking.csv, it will pull from the "total" column; if it is from a series, it will pull from the "points" column.

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
