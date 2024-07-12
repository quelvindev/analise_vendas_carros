options(digits = 10)

install.packages("tidyverse")
library(tidyverse)

?tidyverse
municipio <- c("Três Cachoeiras","Mostardas","Mostardas","Lagoa Bonita do Sul","Pirapetinga",
               "Pirapetinga","Independência","Esperança do Sul","Alagoa","Butiá","Pontão",
               "Roca Sales","Passo Fundo","Passo Fundo","Passo Fundo","Passo Fundo","Passo Fundo",
               "Passo Fundo")
pop <- c(10989,12760,12760,2884,10731,10731,6228,2969,2683,20929,3908,11300,201767,
         201767,201767,201767,201767,201767)
desp_alun <- c(36743.27381,
               22660.61764,
               22660.61764,
               30597.8084,
               21994.84054,
               21994.84054,
               39107.21986,
               37226.56322,
               19402.8741,
               30110.91,
               33734.03,
               28512.16,
               27996.61,
               27996.61,
               27996.61,
               27996.61,
               27996.61,
               27996.61)
uf <- c("RS","RS","RS","RS","MG","MG","RS","RS","MG","RS","RS","RS","RS","RS","RS","RS","RS","RS")
escola <- c("EMEF FERNANDO FERRARI",
            "EMF DR DINARTE SILVEIRA MARTINS",
            "E M F NOSSA SENHORA APARECIDA",
            "ESCOLA MUNICIPAL DE EDUACAO BASICA RAINHA DOS APOSTOLOS",
            "CENTRO EDUCACIONAL MUNICIPAL DE PIRAPETINGA",
            "EM CEL RIBEIRO DOS REIS", 
            "EMEF PRESIDENTE GETULIO VARGAS", 
            "ESCOLA MUNICIPAL ENSINO FUNDAMENTAL ESPERANCA",
            "EN CORONEL PORFIRIO MENDES PINTO",
            "ESCOLA MUNICIPAL DE ENSINO FUNDAMENTAL PROFESSORA MARIA ALZIRA",
            "E EF ALBERTO TORRES",
            "ESC MUN ENS FUN PERPETUO SOCORRO",
            "EMEF ELOY PINHEIRO MACHADO",
            "EMEF ESCOLA DO HOJE",
            "EMEF BENONI ROSADO",
            "EMEF DOM JOSE GOMES",
            "EMEF ANTONINO XAVIER",
            "EMEF URBANO RIBAS")
nota <- c(5.553167,
          4.963667,
          5.839833,
          6.066333,
          5.711333,
          5.142667,
          5.142667,
          5.142667,
          5.6995,
          5.205,
          6.087333,
          5.101167,
          5.946,
          4.745,
          5.4185,
          5.800667,
          5.636,
          5.412333
          )

matriculas <- c(192,264,284,143,202,563,503,294,297,426,268,201,421,304,278,233,280,458)
sec_edu <- c(1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1)
seg_edu <- c(0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0)
sec_saude <- c(0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0)

dados <- data.frame(municipio,pop,desp_alun,uf,escola,nota,matriculas,sec_edu,seg_edu,sec_saude)

dados

dados_filtrados <- dados %>% select(municipio,pop,desp_alun,uf,escola,nota,matriculas)

dados_passo_fundo <- dados %>% filter(municipio=="Passo Fundo" & matriculas>300)
dados_passo_fundo

dados_matricula<- dados %>% filter(matriculas>300)
dados_matricula

glimpse(dados)
table(dados$uf)

dados_uf <- dados %>%
 count(uf)

dados_uf

table(dados$municipio)

dados_municipio <- dados %>%
  count(municipio)
dados_municipio

dados_soma_matriculas <- dados %>% 
  group_by(uf)  %>% 
  summarize( total=sum(matriculas))

dados_soma_matriculas

dados_media_matriculas <- dados %>% 
  group_by(uf)  %>% 
  summarize( total=mean(matriculas))

dados_media_matriculas


dados_media_notas <- dados %>% 
  group_by(municipio)  %>% 
  summarize( total=mean(nota)) %>%
  arrange(desc(total))


dados_media_notas

dados <- dados %>%
  mutate("% populacao"=(matriculas/pop)*100) %>%
  arrange(municipio)


dados <- dados %>%
  mutate(nota=(nota*100)) %>%
  arrange(municipio)

dados$nota <- dados$nota

