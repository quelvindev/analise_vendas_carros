
install.packages("dados")

library(dados)
library(tidyverse)

dados_gapminder %>%
  filter(pais=="Brasil") %>%
  ggplot()+
  geom_point(aes(x=ano,y=expectativa_de_vida))+
  geom_point(aes(x=ano,y=expectativa_de_vida))




dados_gapminder %>%
  filter(ano==2007) %>%
  ggplot()+
  geom_histogram(aes(x=pib_per_capita),color="White")+
  scale_y_log10(breaks=c(seq(0,10,1)))+
  scale_x_log10()

