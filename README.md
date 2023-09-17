# Modelo de clasificación de fallas de sistemas de levantamiento artificial en Hocol

## Descripción

Hocol es una filial del Grupo Ecopetrol. Las actividades de producción y exploración se concentran especialmente en las cuencas del norte de Colombia (Guajira, Sinú San Jacinto, Valle Inferior del Magdalena y Cesar Ranchería), los Llanos (norte del Meta y sur del Casanare) y el Valle Superior del Magdalena (Huila y Tolima). 

El alcance de este proyecto está enfocado en disminuir los costos de paradas de producción en el campo, por eventos relacionados con mantenimientos correctivos y fallas en elementos críticos del pozo, los cuales pueden detectarse de manera proactiva y ser mitigados controladamente, asegurando la continuidad operacional del campo y la mínima afectación económica en la producción de crudo del bloque.  

# Integrantes
* Juan David Ayala Nariño
* Brayan Steven Garcia Cardenas
* Alberto Jose Mendoza Peñaloza
* Carlos Fernando Montaña Herrera
  
## Conclusiones

Estos son algunos insights que se han concluido después de realizar el analisis exploratorio inicial de los datos:

* La distribución de registros por hora no es uniforme (prueba chi cuadrado)
* Existe una gran cantidad de valores nulos, esto puede deberse a que el sensor reporta únicamente al momento de presentarse cambios **(Se requiere validar con negocio)**
* Algunas de las métricas se recuperan muy pocas veces para ser tenidas en cuenta.
* Se encuentran algunos valores negativos incluso cuando las unidades no lo permiten **(Validar con el negocio)**
* Existen algunas posibles correlaciones entre variables pero es necesario asegurar que los datos con los que se dispone muestran la información correcta.
* Existen outliers muy grandes o muy pequeños que superan las medias en ordenes de magnitud.

## Fuentes de Datos

Este analisis está basado en información reportada por los dispositivos IoT, la cual es almacenada en **CosmosDB** y **Scada Experion**. 

## Requerimientos

Para  correr este proyecto es necesario:
- Python 3.x
- Pandas
- Seaborn
- Jupyter Notebook (Para ejecutar el Notebook respectivo)
- Openpyxl
  
## Uso

1. Clonar este repositorio.
2. Abrir el Notebook de Jupyter **analysis.ipynb** para ver el analisis exploratorio de los datos.
3. En el archivo **entrega.pdf** se encuentran los entregables respectivos para cada iteración.



