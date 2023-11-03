print ("Calculadora de Custo de Viagem")

distancia_km = float(input("Qual é a distância da viagem em quilômetros?"))
consumo_km_litro = float(input("Qual é o consumo médio de combustível de carro em km/l?"))
preco_litro = float(input("Qual é o preço do combustível por litro R$?"))
quantidade_pedagios = int(input("Quantos pedágios existem ao longo da viagem?"))
custo_pedagio = 0
for pedagio in range (quantidade_pedagios):
       valor_pedagio = float(input(f"Informe o valor do pedágio {pedagio+1}: "))
       custo_pedagio += valor_pedagio

quilometragem_oleo = float(input("Quantos quilômetros dura o óleo do carro?"))
custo_oleo = float(input("Qual é o custo para trocar o óleo do carro?"))

quantidade_litros = distancia_km / consumo_km_litro
custo_combustivel = quantidade_litros *preco_litro
total_oleo = (distancia_km / quilometragem_oleo) * custo_oleo
custo_total = custo_combustivel + custo_pedagio + total_oleo

print("O custo total da viagem é de : R$" , custo_total)
print("Custo do óleo: R$", total_oleo)
