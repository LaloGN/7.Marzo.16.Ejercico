# 7.Marzo.16.Ejercico

### Clase
help(AirPassengers)
data("AirPassengers")
panam<-(AirPassengers)
class(panam)
start(panam);end(panam);frequency(panam)
panam
###ppp<-ts(base1,start=c(1998,1),freq=4)### funcion para declarar una base de datos com serie de tiempo
plot (panam)
layout(1:2)
plot(panam, main = "Numero de pasajeros aereos en Estados Unidos, 1949-1960", 
     xlab = "Años", ylab = "Pasajeros (miles)",col="blue")
plot(aggregate(panam))               

### Ejercicio
### 1) Generar una data frame con la tasa de desocupacion que inicia en el primer trimestre del 2005,
### tasa de desocupacio 3.4, 4.8, 3.3, 5.6, 3.2, 2.9, 1.9, 2.8, 6.0, 4.3, 2.2
### 2) convertir en serie de tiempo y graficar la ST y la tendencia
### ***punto extra
### 3) obtener un pdf, .jpg. tiff. con las dos graficas en una misma imagen
### Subir a GitHub martes 8 de marzo antes de las 11:59 hrs.....

### Solucion
datos<-c(3.4, 4.8, 3.3, 5.6, 3.2, 2.9, 1.9, 2.8, 6.0, 4.3, 2.2)
tasa<-data.frame(datos)
st<-ts(tasa,start=c(2005,1),freq=4) 
pdf("GraficaTasaDeDesocupacion.pdf")
layout(1:2)
plot(st, main="Tasa de desocupacion, 2005-2007", 
     xlab="Años", ylab="Tasa", col="blue")
plot(aggregate(st))
