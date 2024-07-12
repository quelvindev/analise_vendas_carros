# Criando colunas numéricas para os valores categóricos
dados$Nivel.Marca <- as.numeric(dados$Marca)
hist(dados$Nivel.Marca)
head(dados[,c("Marca")])


# Supondo que 'dados_vendas_carros' seja o dataframe que você tem

# Gerando o histograma das cores vendidas
# Convertendo a coluna "Cor" em um vetor numérico
dados$Nivel.Cor<- as.numeric(dados$Cor)

# Gerando o histograma das cores vendidas
hist(dados$Nivel.Cor, main = "Histograma de Cores Vendidas", xlab = "Cor", ylab = "Frequência",col = "skyblue")

axis(1, at = 1:length(levels(dados$Cor)), labels = levels(dados$Cor));



# Gerando o diagrama de dispersão considerando a marca e o valor dos carros
plot(dados$Preço ~ dados$Marca, 
     xlab = "Marca", ylab = "Valor dos Carros", 
     main = "Diagrama de Dispersão: Marca vs Valor",
     col = as.numeric(dados$Marca), 
     pch = 19)

# Adicionando legenda
legend("topright", legend = levels(dados$Marca), col = 1:length(levels(dados$Marca)), pch = 19)




# Gerando o gráfico de dispersão
plot(dados_ford$Preço, dados_ford$Quantidade,
     xlab = "Valor dos Carros", ylab = "Marca",
     main = "Gráfico de Dispersão: Valor dos Carros vs Marca",
     col = dados_ford$Quantidade)


plot(dados$Preço, dados$Quantidade,
     xlab = "Valor dos Carros", ylab = "Marca",
     main = "Gráfico de Dispersão: Valor dos Carros vs Marca",
     col = dados$Quantidade)


dados_ford <- subset(dados, Marca == "Ford")
