# Estatística I - Entenda os seus dados com R

## Criando Lista com R

```
lista <- c(1,2,3,4,5,6,7,8,9,0)
```

## Média, Mediana e Moda

Média
```
lista <- c(1,2,3,4,5,6,7,8,9,0)
mean(lista);
```

Mediana
```
lista <- c(1,2,3,4,5,6,7,8,9,0)
median(lista);
```

Moda

Moda em R não existe um comando ate o momenta da versão. Uma alternativa é programar uma função:
```
mode <- function(x) {
     ux <- unique(x)
     ux[which.max(tabulate(match(x, ux)))]
}
```
E usar o comando:
```
lista <- c(1,2,3,4,5,6,7,8,9,0)
mode(lista)
```

### Distribuição Normal

Usamos o comando <b>shapiro.test()</b> e devemos observar o valor de p-value. Caso seja maior que 0,05 é uma <b>distribuição normal</b> caso seja menor <b>não é Normal</b>.

```
lista <- c(1,2,3,4,5,6,7,8,9,0)
shapiro.test(lista)
```

### Sumary

Esse comando traz informações de uma lista como Media, Mediana, 1º Quartil e 3º Quartil.

```
numeros <- c (1, 3, 5, 6, 10, 19, 23, 5, 7, 89, 15, 14, 22, 23, 32, 23, 37)
summary(numeros)
```

### Boxplot

```
numeros <- c (1, 3, 5, 6, 10, 19, 23, 5, 7, 89, 15, 14, 22, 23, 32, 23, 37)
boxplot(numeros)
```

### Gerar arquivos de imagem

Para gerar um arquivo de imagem em R podemos usar o comando <b>png</b>

```
numeros <- c (1, 3, 5, 6, 10, 19, 23, 5, 7, 89, 15, 14, 22, 23, 32, 23, 37)
png(file="User/gabriel/boxplot.png", width=700, height=700)
boxplot(numeros)
dev.off()
```

### Desvio Padrão

```

```