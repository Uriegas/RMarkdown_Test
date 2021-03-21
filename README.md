Primero es necesario obtener la [base de datos](https://cutt.ly/Gl9NLpX)
en R:

``` r
load("Datasets/wage1.RData")
```

La información se guarda en un objeto llamado `data`.

### 1. Determine el nivel educativo promedio de la muestra ¿Cuáles son los niveles de educación menor y mayor?

El nivel educativo promedio de la muestra en años es:

``` r
mean(data$educ)
```

    ## [1] 12.56274

### 2. Determine el salario promedio por hora (wage) en la muestra. ¿Parece ser alto o bajo?

El salario promedio por hora (*w**a**g**e*/*h**o**u**r*) es:

``` r
mean(data$wage)
```

    ## [1] 5.896103

De tratarse de dólares americanos y considerando que el salario mínimo
por hora en Estados Unidos es de $7.25, entonces es un salario promedio
por hora bajo.

### 3. ¿Cuántas mujeres hay en la muestra?

El número de mujeres se obtiene sumando los valores booleanos de la
columna `female`:

``` r
sum(data$female)
```

    ## [1] 252

### 4. ¿Cuántos hombres hay en la muesta?

Dado que no hay una columna que cuente el número de hombres, entonces se
resta el número de mujeres del total de la muestra:

``` r
length(data$female) - sum(data$female)
```

    ## [1] 274
