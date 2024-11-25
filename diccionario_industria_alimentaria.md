# Diccionario de Códigos CIIU para la Industria Alimentaria

Este diccionario contiene los códigos CIIU y sus descripciones correspondientes a las actividades relacionadas con la elaboración de productos alimenticios. Estos códigos pueden ser utilizados para filtrar datos en la consulta de la industria alimentaria.

## Códigos y Descripciones:

- **1011**: PROCESAMIENTO Y CONSERVACIÓN DE CARNE Y PRODUCTOS CÁRNICOS
- **1012**: PROCESAMIENTO Y CONSERVACIÓN DE PESCADOS, CRUSTÁCEOS Y MOLUSCOS
- **1020**: PROCESAMIENTO Y CONSERVACIÓN DE FRUTAS, LEGUMBRES, HORTALIZAS Y TUBÉRCULOS
- **1030**: ELABORACIÓN DE ACEITES Y GRASAS DE ORIGEN VEGETAL Y ANIMAL
- **1040**: ELABORACIÓN DE PRODUCTOS LÁCTEOS
- **1051**: ELABORACIÓN DE PRODUCTOS DE MOLINERÍA
- **1052**: ELABORACIÓN DE ALMIDONES Y PRODUCTOS DERIVADOS DEL ALMIDÓN
- **1061**: TRILLA DE CAFÉ
- **1062**: DESCAFEINADO, TOSTIÓN Y MOLIENDA DEL CAFÉ
- **1063**: OTROS DERIVADOS DEL CAFÉ
- **1071**: ELABORACIÓN Y REFINACIÓN DE AZÚCAR
- **1072**: ELABORACIÓN DE PANELA
- **1081**: ELABORACIÓN DE PRODUCTOS DE PANADERÍA
- **1082**: ELABORACIÓN DE CACAO, CHOCOLATE Y PRODUCTOS DE CONFITERÍA
- **1083**: ELABORACIÓN DE MACARRONES, FIDEOS, ALCUZCUZ Y PRODUCTOS FARINÁCEOS SIMILARES
- **1084**: ELABORACIÓN DE COMIDAS Y PLATOS PREPARADOS
- **1089**: ELABORACIÓN DE OTROS PRODUCTOS ALIMENTICIOS N.C.P.
- **1090**: ELABORACIÓN DE ALIMENTOS PREPARADOS PARA ANIMALES
- **1101**: DESTILACIÓN, RECTIFICACIÓN Y MEZCLA DE BEBIDAS ALCOHÓLICAS
- **1102**: ELABORACIÓN DE BEBIDAS FERMENTADAS NO DESTILADAS
- **1103**: PRODUCCIÓN DE MALTA, ELABORACIÓN DE CERVEZAS Y OTRAS BEBIDAS MALTEADAS
- **1104**: ELABORACIÓN DE BEBIDAS NO ALCOHÓLICAS, PRODUCCIÓN DE AGUAS MINERALES Y DE OTRAS AGUAS EMBOTELLADAS

## Descripción de la Consulta de Datos

La consulta de datos para la industria alimentaria utiliza los códigos CIIU de este diccionario para filtrar los datos correspondientes a la elaboración de productos alimenticios. En particular, los datos de la colección **"Demanda Comercial No Regulada por CIIU"** se filtran por el sector de **"INDUSTRIAS MANUFACTURERAS"** y los códigos CIIU relacionados con la industria alimentaria.

### Ejemplo de Uso:

1. **Obtener la lista de códigos CIIU relevantes**: Puedes utilizar esta lista para filtrar el conjunto de datos con los códigos correspondientes.
   
2. **Filtrar los datos en el DataFrame**: Los datos son filtrados para incluir solo las filas que pertenecen a la categoría "INDUSTRIAS MANUFACTURERAS" y que tienen un código CIIU incluido en este diccionario. Este filtrado te permitirá analizar únicamente los datos relacionados con la industria alimentaria.

```python
# Ejemplo de filtrado con los códigos CIIU
ciiu_codes = ['1011', '1012', '1020', '1030', '1040', '1051', '1052', '1061', '1062', '1063', '1071', 
              '1072', '1081', '1082', '1083', '1084', '1089', '1090', '1101', '1102', '1103', '1104']

df_manufactura_alimentos = df_DemaComeNoReg[
    (df_DemaComeNoReg['Values_Activity'] == "INDUSTRIAS MANUFACTURERAS") & 
    (df_DemaComeNoReg['Values_code'].isin(ciiu_codes))
]
