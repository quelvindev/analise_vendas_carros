
library(tidyverse)

arquivo <- "https://raw.githubusercontent.com/fernandobarbalho/enap_auto_instucional/main/data/dados_municipios.csv"


dados_municipios <- read_csv(file=arquivo)


dados_pernanbuco <- dados_municipios %>%
  filter(sigla_uf=="PE" & populacao>100000) %>%
  arrange(desc(populacao))



dados_municipios %>%
  filter(sigla_uf=="CE" ) %>%
  select(sigla_uf,nome,populacao) %>%
  arrange(desc(populacao))


dados_municipios %>%
  filter(sigla_uf!="DF" ) %>%
  group_by(sigla_uf) %>%
  summarise(
    media_populacao_municipio = mean(populacao)
  ) %>%
  arrange(desc(populacao))
  


ggplot(data = dados_pernanbuco)+
  geom_col(aes(x = populacao , y = reorder(nome, populacao), fill = nome)) 
  

dados_municipios %>%
  filter(sigla_uf=="PE" & populacao>100000) %>%
  slice_max(populacao,n=10) %>%
  ggplot()+
  geom_col(aes(x = populacao , y = reorder(nome, populacao), fill = nome)) 


dados_municipios %>%
  filter(nome_regiao=="Nordeste") %>%
  ggplot()+
  geom_boxplot(aes(x=sigla_uf,y= populacao))+
  scale_y_log10()

dados_municipios %>%
  filter(nome_regiao=="Sudeste") %>%
  ggplot()+
  geom_histogram(aes(x=populacao),color="White")+
  scale_x_log10()

table(dados_municipios$nome_regiao)

dados_municipios %>%
  ggplot(aes(x = populacao)) +
  geom_histogram(color = "White") +
  scale_x_log10() +
  facet_wrap(~ nome_regiao, ncol = 1)
