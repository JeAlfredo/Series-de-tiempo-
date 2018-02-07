# Series-de-tiempo-
#### 1. SIMULACIÓN DE SERIES DE TIEMPO#######
# vAMOS A SIMULAR LOS INDICADORES 
# PARA LA SIMULACIÓN EN PRINCIPIO NECESITAMOS ALGUNA INFORMACIÓN
# VALOR MÁXIMO, MÍNIMO, EL NÚMERO DE DATOS
# EN ESTE EJEMPLO VAMOS A PROPONER LA POBLACIÓN EN MÉXICO 
# QUE LE VALOR MÍNIMO SERAN 100, MÁXIMO 120, 15 DATOS QUE INICIE EN 2000
pob<- sample (100:120, 15, replace=F) 
pob
### LA CONVERTIMOS EN UNA SERIE DE TIEMPO 
## ts= función que convierte tus datos en una serie de tiempo 
pobts <- ts (pob, frequency = 1, start = (2000))
#frequency=que tanto se repiten los datos anualmente, start= en que año iniciará el análisis
end (pobts)#En que año termina 
start(pobts)#En que año comenza
plot(pobts)#Darle formato 
plot(aggregate(pobts))
help ("aggregate")

infor4<-read.csv("C://Users//USUARIO//Desktop//Inegi.csv")
infor4
inf<- ts(infor4, frequency = 4, start = 2005)
plot(inf, ylim=c(0,100))## Para cambiar el rango 
