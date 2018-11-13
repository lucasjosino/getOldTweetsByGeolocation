# getOldTweetsByGeolocation
Como buscar tweets por ferramentas disponibilizadas filtrando pela localização.

# Introduction
O Twitter descontinuou seu conceito de localizações deixando as ferramentas existentes para extração de dados de lado quanto à obtenção de tweets por localização. Segue tutorial para busca de tweets utilizando getOldTweets (https://github.com/lucasjosino/GetOldTweets-java) ou twitterscraper (https://github.com/taspinar/twitterscraper) que permitirá a busca filtrando por bairro, cidade, estado, País. dDve ser funcional para outras ferramentas de extração.

# Twitter Advanced Search
As duas ferramentas de busca com intuito de barrar a limitação do número de tweets e a data máxima de 7 dias atrás para obtenção fazem uma varredura na busca avançada do twitter criando url de forma dinâmica de acordo com os argumentos passados. a idéia geral é fornecer argumentos que a busca interprete e atualmente o funcionamento via nome da localização não funciona mais.

# Geocode
O componente permitido pela busca do twitter são as coordenadas existentes no json de cada tweet e são traduzidas na busca como "geocode:". Ao fazer uma busca avançada na rede social utilizando "geocode:coordenada,xKM" onde x representa o raio de distância coberto pela busca a partir da coordenada é possivel obter os resultados filtrados. Tente https://twitter.com/search?f=tweets&q=geocode%3A-18.914000%2C-48.261981%2C18.18km&src=typd.

# Incrementando busca no GetOldTweets e twitterscraper
Obtenha as coordenadas da região que deseja coletar e calcule o raio necessário para atingir todo o bairro/cidade/estado/País (é possível obter pelo google maps e ao clicar com o esquerdo medir a distância a partir do ponto), insira no campo da ferramenta de sua preferência "geocode:coordenadas,Xkm termosdabusca".
legenda:
coordenadas = as coordenadas do ponto.
X = número de distância coberto a partir da coordenada.
termosdabusca = argumentos para encontrar em meio as tweets.

Exemplo em getOldTweets: Exporter.py --querysearch "geocode%3A-18.9327484%2C-48.2529798%2C13.75km Ator"

# Considerações
Essa busca pode limitar ou extraviar as regiões necessárias mas ainda permite filtrar por bairro, cidade, estado, País desde que haja certa cautela quando a amostragem escolhida para sua pesquisa, aplicação ou trabalho.


