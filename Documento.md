# Entrega 2 Analisis de bases de Datos

Lo que se quiere hacer inicialmente es un analisis y reduccion de dimension de la base de datos de Matriculados.  
Así que primero caractericemos esta base:  

## Caracterizacion de la Base de Datos Original de Matriculados

Los 44 atributos de la base son los siguientes y corresponden a la siguiente informacion:

+ **YEAR:**  
+ **SEMESTRE:**  
+ **TIPO_NIVEL:**          
+ **NIVEL:**  
+ **DEP_NAC:**  
+ **COD_DEP_NAC:**  
+ **CIU_NAC:**  
+ **COD_CIU_NAC:**  
+ **LON_CIU_NAC:**  
+ **LAT_CIU_NAC:**  
+ **DEP_PROC:**  
+ **COD_DEP_PROC:**  
+ **CIU_PROC:**  
+ **COD_CIU_PROC:**  
+ **LON_CIU_PROC:**  
+ **LAT_CIU_PROC:**  
+ **CODS_NAC:**  
+ **CODN_NAC:**  
+ **NACIONALIDAD:**  
+ **EDAD:**  
+ **SEXO:**  
+ **ESTRATO:**  
+ **TIPO_COL:**  
+ **PBM:**  
+ **MAT_PVEZ:**  
+ **SNIES_SEDE_ADM:**  
+ **SEDE_NOMBRE_ADM:**  
+ **SNIES_SEDE_MAT:**  
+ **SEDE_NOMBRE_MAT:**  
+ **ADM_PEAMA_ANDINA**  
+ **MOD_ADM:**  
+ **TIPO_ADM:**  
+ **PAES:**  
+ **PEAMA:**  
+ **MOV_PEAMA:**  
+ **CONVENIO:**  
+ **TIP_CONVENIO:**  
+ **FACULTAD:**  
+ **SNIES_PROGRA:**  
+ **PROGRAMA:**  
+ **AREAC_SNIES:**  
+ **CA_CINE:**  
+ **CD_CINE:**  
+ **AREA_CINE:**  

Estos atributos pueden agruparse de la siguiente manera:  

+ ***NIVEL:*** En esta categoria corresponden *TIPO_NIVEL* y *Nivel*. Pues la primera solo indica que si el estudiante pertenece a pregrado o postgrado,
  la segunda hace lo mismo pero tiene ademas como posibles datos 'Maestria'.'Especializacion','Doctorado','Especializaciones medicas' y 'Pregrado' .  
  Con lo cual podemos tomar unicamente *Nivel*, pues si un estudiante no esta haciendo pregrado y tiene otro Nivel es porque esta haciendo postgrado.  
  Dicho de otra manera, 'NIVEL' determina a 'TIPO_NIVEL'

+ ***DEPARTAMENTO:*** A Esta categoria pertenecen *DEP_NAC* y *COD_DEP_NAC*, pues ambos se determinan entre sí, sabiendo el codigo se puede saber el departemento y viceversa.  

+ ***MUNICIPIO*** A esta categoria pertenece *CIU_NAC*, *COD_CIU_NAC*, *LON_CIU_NAC* y *LAT_CIU_NAC*. Si se conoce el municipio del que proviene un estudiantes se conoce un codigo y su latidu y longitud.  

+ ***DEPARTAMENTO PROCEDIMIENTO***  

+ ***MUNICIPIO PROCEDIMIENTO***  

+ ***NACIONALIDAD***  

+ ***SEDE ADMISION***  

+ ***SEDE MATRICULADO***  

+ ***TIPO DE ADMISION*** Aqui pertenecen *MOD_ADM* y *TIPO_ADM* , pues si se conoce el tipo de admision (REgular,PAES,Peama,PEAA) se conoce si el modo de admision fuue regular o Especial.  

TODO: mirar si se puede unir todos los atributos relativos a admisiones especiales



#_______
primeramente se va a reducir la dimension de la base de datos de Matriculados, pues a simple vista 
se nota que existen varios atributos que corresponden a la misma información  
