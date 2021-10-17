# Practica2_BD1

## Marco Teorico

### Modelo Conceptual

> Un modelo conceptual de datos identifica las relaciones de más alto nivel entre las diferentes entidades.
>
> Las características del modelo conceptual de datos incluyen:
>
> + Incluye las entidades importantes y las relaciones entre ellas.
> + No se especifica ningún atributo.
> + No se especifica ninguna clave principal.

### Modelo Logico

> Un modelo lógico de datos es un modelo que no es específico de una base de datos que describe aspectos relacionados con las necesidades de una organización para recopilar datos y las relaciones entre estos aspectos.
>
> Un modelo lógico contiene representaciones de entidades y atributos, relaciones, identificadores exclusivos, subtipos y supertipos y restricciones entre relaciones. Un modelo lógico también puede contener objetos de modelo de dominio o referirse a uno o varios modelos de dominio o de glosario. Una vez definidas las relaciones y los objetos lógicos en un modelo lógico de datos, utilice el área de trabajo para transformar el modelo lógico en una representación física específica de la base de datos en forma de modelo físico de datos.
>
> Mediante el área de trabajo, puede crear un modelo lógico de datos a partir de una plantilla. También puede importar tipos de datos simples de un archivo de definición de esquemas XML (.xsd) en un modelo lógico de datos como tipos de dominio.

### Modelo Fisico

> Un modelo de datos físicos es un modelo específico de bases de datos que representa objetos de datos relacionales (por ejemplo, tablas, columnas, claves principales y claves externas) y sus relaciones. Un modelo de datos físicos se puede utilizar para generar sentencias DDL que, después, se pueden desplegar en un servidor de base de datos.

## Modelo Conceptual

![ModeloConceptual](https://drive.google.com/uc?export=view&id=1k_Kk9j0JIOvJ1Wu3Qhjt0Ss9UYYnsWlN)

### Explicacion de tablas

#### Fecha

> Esta tabla se utiliza para almacenar todas las fechas, ya que por cada pais se debe ingresar la misma fecha crea datos duplicados por eso decidi utilizar una tabla especifica para manejar las fechas

#### Continente

> Tabla en la cual se almacenan los continentes existentes, esta tabla necesita ser cargada antes de empezar a llenar las demas

#### Pais_Info

> Esta tabla almacena los datos estadisticos correspondientes a cada pais, estos datos tienen relacion con el desarrollo de la enfermedad.
> + population: representa la poblacion del pais
> + population_density: representa la densidad de la poblacion en el pais
> + median_age: representa la edad media en el pais
> + aged_65_older: Indicadores de desarrollo mundial del Banco Mundial basados en distribuciones por edad / sexo de la Revisión de 2017 de Perspectivas de la población mundial de las Naciones Unidas 
> + aged_70_older: Naciones Unidas, Departamento de Asuntos Económicos y Sociales, División de Población (2017), Revisión de 2017 de Perspectivas de la población mundial
> + gdp_per_capita: Indicadores de desarrollo mundial del Banco Mundial, fuente del Banco Mundial, base de datos del Programa de Comparación Internacional
> + extreme_poverty: Indicadores de desarrollo mundial del Banco Mundial, obtenidos del Grupo de Investigación sobre el Desarrollo del Banco Mundial
> + diabetes_prevalence: Indicadores de desarrollo mundial del Banco Mundial, extraídos de la Federación Internacional de Diabetes, Diabetes Atlas
> + female_smokers: Indicadores de desarrollo mundial del Banco Mundial, obtenidos de la Organización Mundial de la Salud, Repositorio de datos del Observatorio de la salud mundial
> + male_smokers: Indicadores de desarrollo mundial del Banco Mundial, obtenidos de la Organización Mundial de la Salud, Repositorio de datos del Observatorio de la salud mundial
> + handwashing_facilities: Indicador de lugares para lavar manos segun la División de Estadística de las Naciones Unida
> + life_expectancy: Expectativa de vida segun James C. Riley, Clio Infra, División de Población de las Naciones Unidas
> + human_development_index: Indice de desarrollo segun Programa de las Naciones Unidas para el Desarrollo (PNUD)
> + excess_mortality: Base de datos de mortalidad humana (HMD) Proyecto de fluctuaciones de la mortalidad a corto plazo y Conjunto de datos de mortalidad mundial (WMD)

#### Caso

> + total_cases: Cantidad de casos totales de covid hasta la fecha dada
> + new_cases: Nuevos casos de covid en una fecha dada
> + new_cases_smoothed: 
> + total_cases_per_million: Total de casos por millon hasta la fecha dada
> + new_cases_per_million: Nuevos casos de covid en una fecha dada
> + new_cases_smoothed_per_million: 

#### Muerte

> + total_deaths: Total de muertes por covid hasta una fecha dada
> + new_deaths: Nuevas muertes por covid en una fecha dada
> + new_deaths_smoothed: 
> + total_deaths_per_million: Total de muertes por covid por millon hasta la fecha dada 
> + new_deaths_per_million: Nuevas muertes por covid en una fecha dada
> + new_deaths_smoothed_per_million: 

#### Rate

> + reproduction_rate: tasa de reproduccion segun Arroyo Marioli et al. (2020). https://doi.org/10.2139/ssrn.3581633
> + positive_rate: tasa de casos positivos
> + cardiovasc_death_rate: tasa de muerte por problemas cardiovasculares

#### Icu

> + icu_patients: Pacientes en cuidados intensivos hasta la fecha dada
> + icu_patients_per_million: Pacientes en cuidados intensivos por millon
> + weekly_icu_admissions: Pacientes en cuidados intensivos en cierta semana
> + weekly_icu_admissions_per_million: Pacientes en cuidados intensivos en cierta semana por millon

#### Info_Hospital

> + hosp_patients: Pacientes hospitalizados hasta una fecha dada
> + hosp_patients_per_million: Pacientes hospitalizados por millon
> + weekly_hosp_admissions: Admisiones semanales
> + weekly_hosp_admissions_per_million: Adminisiones semnales por millon
> + hospital_beds_per_thousand: Camas en hospitales por cada mil habitantes

#### Test

> + new_tests: Test nuevos en una fecha dada
> + total_tests: Test totales en una fecha dada
> + total_tests_per_thousand: Test totales por cada mil habitantes
> + new_tests_per_thousand: Test nuevos por cada mil habitantes
> + new_tests_smoothed: 
> + new_tests_smoothed_per_thousand: 
> + tests_per_case: Test por cada caso positivo
> + tests_units: Cantidad de test

#### Vacuna

> + total_vaccinations: Cantidad de vacunados
> + people_vaccinated: Cantidad de vacunados
> + people_fully_vaccinated: Cantidad de personas con dosis completas
> + new_vaccinations: Nuevas vacunas en una fecha dada
> + new_vaccinations_smoothed: 
> + total_vaccinations_per_hundred: Total de vacunaciones por ciento
> + people_vaccinated_per_hundred: Personas vacunadas por ciento
> + people_fully_vaccinated_per_hundred: Personas con dosis completas por ciento
> + new_vaccinations_smoothed_per_million: 
> + stringency_index: tasa de rigorosidad

## Modelo Logico

| Fecha       |           |           |
| ----------- | --------- | --------- |
| Columnas    | Id\_fecha | Date |
| Restriccion | PK        | NN |
|             | 1         | 2/24/2020 |
|             | 2         | 5/19/2021 |
|             | 3         | 12/15/2020 |
|             | 4         | 9/4/2020 |
|             | 5         | 6/15/2021 |
|             | 6         | 4/1/2021 |
|             | 7         | 4/25/2021 |
|             | 8         | 11/23/2020 |
|             | 9         | 6/30/2020 |
|             | 10        | 3/29/2020 |

| Pais        |          |          |          |
| ----------- | -------- | -------- | -------- |
| Columnas    | Id\_pais | Iso\_code | nombre |
| Restriccion | PK       | NN | NN |
|             | 1        | AFG | Afghanistan |
|             | 2        | AGO | Angola |
|             | 3        | ATG | Antigua and Barbuda |
|             | 4        | CPV | Cape Verde |
|             | 5        | CYP | Cyprus |
|             | 6        | ECU | Ecuador |
|             | 7        | GAB | Gabon |
|             | 8        | IRN | Iran |
|             | 9        | KWT | Kuwait |
|             | 10       | MCO | Monaco |

| Continente  |                |                |
| ----------- | -------------- | -------------- |
| Columnas    | Id\_continente | Nombre |
| Restriccion | PK             | NN |
|             | 1              | Asia |
|             | 2              | Africa |
|             | 3              | North America |
|             | 4              | Europe |
|             | 5              | South America |

| Pais\_Info  |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |
| ----------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| Columnas    | Id\_pais | Id\_continente | population | population\_density | median\_age | aged\_65\_older | aged\_70\_older | gdp\_per\_capita | extreme\_poverty | diabetes\_prevalence | female\_smokers | male\_smokers | handwashing\_facilities | life\_expectancy | human\_development\_index | excess\_mortality |
| Restriccion | PK FK    | PK FK | NN | NN |  |  |  |  |  |  |  |  |  | NN |  |  |
|             | 1        | 1 | 39835428 | 54.422 | 18.6 | 2.581 | 1.337 | 1803.987 |  | 9.59 |  |  | 37.746 | 64.83 | 0.511 |  |
|             | 2        | 2 | 33933611 | 23.89 | 16.8 | 2.405 | 1.362 | 5819.495 |  | 3.94 |  |  | 26.664 | 61.15 | 0.581 |  |
|             | 3        | 3 | 98728 | 231.845 | 32.1 | 6.933 | 4.631 | 21490.943 |  | 13.17 |  |  |  | 77.02 | 0.778 |  |
|             | 4        | 2 | 561901 | 135.58 | 25.7 | 4.46 | 3.437 | 6222.554 |  | 2.42 | 2.1 | 16.5 |  | 72.98 | 0.665 |  |
|             | 5        | 4 | 888005 | 127.657 | 37.3 | 13.416 | 8.563 | 32415.132 |  | 9.24 | 19.6 | 52.7 |  | 80.98 | 0.887 |  |

| Caso        |          |          |          |          |          |          |          |          |          |
| ----------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| Columnas    | Id\_caso | Id\_pais | Id\_fecha | total\_cases | new\_cases | new\_cases\_s | total\_cases\_pm | new\_cases\_pm | new\_cases\_s\_pm |
| Restriccion | PK       | FK | FK | NN | NN |  | NN | NN |  |
|             | 1        | 1 | 1 | 1 | 1 |  | 0.025 | 0.025 |  |
|             | 2        | 2 | 2 | 31438 | 393 | 290.429 | 926.456 | 11.581 | 8.559 |
|             | 3        | 3 | 3 | 148 | 0 | 0.286 | 1499.068 | 0 | 2.894 |
|             | 4        | 4 | 4 | 4200 | 75 | 65 | 7474.626 | 133.475 | 115.679 |
|             | 5        | 5 | 5 | 73311 | 64 | 56 | 82556.968 | 72.072 | 63.063 |

| Muerte      |            |            |            |            |            |            |            |            |            |
| ----------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Columnas    | Id\_muerte | Id\_pais | Id\_fecha | total\_deaths | new\_deaths | new\_deaths\_s | total\_deaths\_pm | new\_deaths\_pm | new\_deaths\_s\_pm |
| Restriccion | PK         | FK | FK |  |  |  |  |  |  |
|             | 1          | 1 | 1 |  |  |  |  |  |  |
|             | 2          | 2 | 2 | 696 | 11 | 7.286 | 20.511 | 0.324 | 0.215 |
|             | 3          | 3 | 3 | 5 | 0 | 0.143 | 50.644 | 0 | 1.447 |
|             | 4          | 4 | 4 | 41 | 0 | 0.429 | 72.967 | 0 | 0.763 |
|             | 5          | 5 | 5 | 374 | 0 | 1.286 | 421.169 | 0 | 1.448 |

| Rate        |          |          |          |          |          |          |
| ----------- | -------- | -------- | -------- | -------- | -------- | -------- |
| Columnas    | id\_rate | Id\_pais | Id\_fecha | reproduction\_rate | positive\_rate | cardiovasc\_death\_rate |
| Restriccion | PK       | FK | FK |  |  |  |
|             | 1        | 1 | 1 |  |  | 597.029 |
|             | 2        | 2 | 2 | 1.05 |  | 276.045 |
|             | 3        | 3 | 3 | 0.68 | 0.16 | 191.511 |
|             | 4        | 4 | 4 | 1.11 | 0.001 | 182.219 |
|             | 5        | 5 | 5 | 1.07 | 0.387 | 141.171 |

| Icu         |         |         |         |         |         |         |         |
| ----------- | ------- | ------- | ------- | ------- | ------- | ------- | ------- |
| Columnas    | id\_icu | Id\_pais | Id\_fecha | icu\_patients | icu\_patients\_per\_million | weekly\_icu\_admissions | weekly\_icu\_admissions\_per\_million |
| Restriccion | PK      | FK | FK |  |  |  |  |
|             | 1       | 1 | 1 |  |  |  |  |
|             | 2       | 2 | 2 |  |  |  |  |
|             | 3       | 3 | 3 |  |  |  |  |
|             | 4       | 4 | 4 |  |  |  |  |
|             | 5       | 5 | 5 | 8 | 9.009 |  |  |

| Info\_Hospital |                    |                    |                    |                    |                    |                    |                    |                    |
| -------------- | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| Columnas       | id\_info\_hospital | Id\_pais | Id\_fecha | hosp\_patients | hosp\_patients\_pm | weekly\_hosp\_adm | weekly\_hosp\_adm\_pm | hospital\_beds\_pt |
| Restriccion    | PK                 | FK | FK |  |  |  |  |  |
|                | 1                  | 1 | 1 |  |  |  |  | 0.5 |
|                | 2                  | 2 | 2 |  |  |  |  |  |
|                | 3                  | 3 | 3 |  |  |  |  | 3.8 |
|                | 4                  | 4 | 4 |  |  |  |  | 2.1 |
|                | 5                  | 5 | 5 | 32 | 36.036 |  |  | 3.4 |

| Test        |          |          |          |          |          |          |          |          |          |          |          |
| ----------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| Columnas    | id\_test | Id\_pais | Id\_fecha | new\_tests | total\_tests | total\_tests\_pt | new\_tests\_pt | new\_tests\_s | new\_tests\_s\_pt | tests\_per\_case | tests\_units |
| Restriccion | PK       | FK | FK |  |  |  |  |  |  |  |  |
|             | 1        | 1 | 1 |  |  |  |  |  |  |  |  |
|             | 2        | 2 | 2 |  |  |  |  |  |  |  |  |
|             | 3        | 3 | 3 |  |  |  |  |  |  |  |  |
|             | 4        | 4 | 4 | 515 |  |  | 0.917 | 407 | 0.724 | 6.3 | tests performed |
|             | 5        | 5 | 5 | 35729 | 7668213 | 8635.326 | 40.235 | 41841 | 47.118 | 747.2 | tests performed |

| Vacuna      |            |            |            |            |            |            |            |            |            |            |            |            |            |
| ----------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Columnas    | id\_vacuna | Id\_pais | Id\_fecha | total\_vs | people\_vd | people\_fully\_vd | new\_vs | new\_vs\_s | total\_vs\_ph | people\_vd\_ph | people\_fully\_vd\_ph | new\_vs\_s\_pm | stringency\_inde |
| Restriccion | PK         | FK | FK |  |  |  |  |  |  |  |  |  |  |
|             | 1          | 1 | 1 |  |  |  |  |  |  |  |  |  | 8.33 |
|             | 2          | 2 | 2 |  |  |  |  | 11468 |  |  |  | 338 | 33.33 |
|             | 3          | 3 | 3 |  |  |  |  |  |  |  |  |  |  |
|             | 4          | 4 | 4 |  |  |  |  |  |  |  |  |  | 68.98 |
|             | 5          | 5 | 5 | 718775 | 436280 | 282495 |  | 8102 | 80.94 | 49.13 | 31.81 | 9124 | 43.52 |


## DDL

```
CREATE TABLE Fecha(
	id_fecha INT NOT NULL IDENTITY(1, 1),
	fecha DATE NOT NULL,
	PRIMARY KEY(id_fecha)
);

CREATE TABLE Pais(
	id_pais INT NOT NULL IDENTITY(1, 1),
	iso_code CHAR(3) NOT NULL,
	nombre VARCHAR2(50) NOT NULL,
	PRIMARY KEY(id_pais)
);

CREATE TABLE Continente(
	id_continente INT NOT NULL IDENTITY(1, 1),
	nombre VARCHAR2(50) NOT NULL,
	PRIMARY KEY(id_continente)
);
	
CREATE TABLE Pais_Info(
	id_pais INT NOT NULL,
	id_continente INT NOT NULL,
	population BIGINT,
	population_density DECIMAL,
	median_age DECIMAL,
	aged_65_older DECIMAL,
	aged_70_older DECIMAL,
	gdp_per_capita DECIMAL,
	extreme_poverty DECIMAL,
	diabetes_prevalence DECIMAL,
	female_smokers DECIMAL,
	male_smokers DECIMAL,
	handwashing_facilities DECIMAL,
	life_expectancy DECIMAL,
	human_development_index DECIMAL,
	excess_mortality DECIMAL,
	PRIMARY KEY (id_pais),
	CONSTRAINT fk_id_pais
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_continente 
		FOREIGN KEY (id_continente) 
		REFERENCES Continente (id_continente)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Caso(
	id_caso INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	total_cases BIGINT,
	new_cases BIGINT,
	new_cases_smoothed FLOAT,
	total_cases_per_million FLOAT,
	new_cases_per_million FLOAT,
	new_cases_smoothed_per_million FLOAT,
	PRIMARY KEY (id_caso),
	CONSTRAINT fk_id_pais_caso
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_caso
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Muerte(
	id_muerte INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	total_deaths BIGINT,
	new_deaths BIGINT,
	new_deaths_smoothed FLOAT,
	total_deaths_per_million FLOAT,
	new_deaths_per_million FLOAT,
	new_deaths_smoothed_per_million FLOAT,
	PRIMARY KEY (id_muerte),
	CONSTRAINT fk_id_pais_muerte
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_muerte
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Rate(
	id_rate INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	reproduction_rate FLOAT,
	positive_rate FLOAT,
	cardiovasc_death_rate FLOAT,
	PRIMARY KEY (id_rate),
	CONSTRAINT fk_id_pais_rate
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_rate
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Icu(
	id_icu INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	icu_patients BIGINT,
	icu_patients_per_million FLOAT,
	weekly_icu_admissions FLOAT,
	weekly_icu_admissions_per_million FLOAT,
	PRIMARY KEY (id_icu),
	CONSTRAINT fk_id_pais_icu
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_icu
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Info_Hospital(
	id_info_hospital INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	hosp_patients BIGINT,
	hosp_patients_per_million FLOAT,
	weekly_hosp_admissions FLOAT,
	weekly_hosp_admissions_per_million FLOAT,
	hospital_beds_per_thousand FLOAT,
	PRIMARY KEY (id_info_hospital),
	CONSTRAINT fk_id_pais_info_hospital
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_info_hospital
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Test(
	id_test INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	new_tests BIGINT,
	total_tests BIGINT,
	total_tests_per_thousand FLOAT,
	new_tests_per_thousand FLOAT,
	new_tests_smoothed FLOAT,
	new_tests_smoothed_per_thousand FLOAT,
	tests_per_case FLOAT,
	tests_units VARCHAR(255),
	PRIMARY KEY (id_test),
	CONSTRAINT fk_id_pais_test
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_test
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);

CREATE TABLE Vacuna(
	id_vacuna INT NOT NULL IDENTITY(1,1),
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	total_vaccinations BIGINT,
	people_vaccinated BIGINT,
	people_fully_vaccinated BIGINT,
	new_vaccinations BIGINT,
	new_vaccinations_smoothed FLOAT,
	total_vaccinations_per_hundred FLOAT,
	people_vaccinated_per_hundred FLOAT,
	people_fully_vaccinated_per_hundred FLOAT,
	new_vaccinations_smoothed_per_million FLOAT,
	stringency_index FLOAT,
	PRIMARY KEY (id_vacuna),
	CONSTRAINT fk_id_pais_vacuna
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION,
	CONSTRAINT fk_id_fecha_vacuna
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
		ON DELETE NO ACTION
		ON UPDATE NO ACTION
);
```

## DML

```
INSERT INTO Fecha(date) VALUES('2/24/2020');
INSERT INTO Fecha(date) VALUES('5/19/2021');
INSERT INTO Fecha(date) VALUES('12/15/2020');
INSERT INTO Fecha(date) VALUES('9/4/2020');
INSERT INTO Fecha(date) VALUES('6/15/2021');
INSERT INTO Fecha(date) VALUES('4/1/2021');
INSERT INTO Fecha(date) VALUES('4/25/2021');
INSERT INTO Fecha(date) VALUES('11/23/2020');
INSERT INTO Fecha(date) VALUES('6/30/2020');
INSERT INTO Fecha(date) VALUES('3/29/2020');

INSERT INTO Pais(iso_code, nombre) VALUES('AFG', 'Afghanistan');
INSERT INTO Pais(iso_code, nombre) VALUES('AGO', 'Angola');
INSERT INTO Pais(iso_code, nombre) VALUES('ATG', 'Antigua and Barbuda');
INSERT INTO Pais(iso_code, nombre) VALUES('CPV', 'Cape Verde');
INSERT INTO Pais(iso_code, nombre) VALUES('CYP', 'Cyprus');
INSERT INTO Pais(iso_code, nombre) VALUES('ECU', 'Ecuador');
INSERT INTO Pais(iso_code, nombre) VALUES('GAB', 'Gabon');
INSERT INTO Pais(iso_code, nombre) VALUES('IRN', 'Iran');
INSERT INTO Pais(iso_code, nombre) VALUES('KWT', 'Kuwait');
INSERT INTO Pais(iso_code, nombre) VALUES('MCO', 'Monaco');

INSERT INTO Continente(nombre) VALUES('Asia');
INSERT INTO Continente(nombre) VALUES('Africa');
INSERT INTO Continente(nombre) VALUES('North America');
INSERT INTO Continente(nombre) VALUES('Europe');
INSERT INTO Continente(nombre) VALUES('South America');

INSERT INTO Pais_Info(id_pais, id_continente, population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, handwashing_facilities, life_expectancy, human_development_index) VALUES(1, 1, 39835428, 54.422, 18.6, 2.581, 1.337, 1803.987, 9.59, 37.746, 64.83, 0.511);
INSERT INTO Pais_Info(id_pais, id_continente, population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, handwashing_facilities, life_expectancy, human_development_index) VALUES(2, 2, 33933611, 23.89, 16.8, 2.405, 1.362, 5819.495, 3.94, 26.664, 61.15, 0.581);
INSERT INTO Pais_Info(id_pais, id_continente, population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, life_expectancy, human_development_index) VALUES(3, 3, 98728, 231.845	32.1, 6.933, 4.631, 21490.943, 13.17, 77.02, 0.778);
INSERT INTO Pais_Info(id_pais, id_continente, population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, female_smokers, male_smokers, life_expectancy, human_development_index) VALUES(4, 2, 561901, 135.58, 25.7, 4.46, 3.437, 6222.554, 2.42, 2.1, 16.5, 72.98, 0.665);
INSERT INTO Pais_Info(id_pais, id_continente, population, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, diabetes_prevalence, female_smokers, male_smokers, life_expectancy, human_development_index) VALUES(5, 4, 888005	127.657	37.3, 13.416, 8.563, 32415.132, 9.24, 19.6, 52.7, 80.98, 0.887);

INSERT INTO Caso(id_pais, id_fecha, total_cases, new_cases, total_cases_per_million, new_cases_per_million) VALUES(1, 1, 1, 1, 0.025, 0.025);
INSERT INTO Caso(id_pais, id_fecha, total_cases, new_cases, new_cases_smoothed, total_cases_per_million, new_cases_per_million, new_cases_smoothed_per_million) VALUES(2, 2, 31438, 393, 290.429, 926.456, 11.581, 8.559);
INSERT INTO Caso(id_pais, id_fecha, total_cases, new_cases, new_cases_smoothed, total_cases_per_million, new_cases_per_million, new_cases_smoothed_per_million) VALUES(3, 3, 148, 0, 0.286, 1499.068, 0, 2.894);
INSERT INTO Caso(id_pais, id_fecha, total_cases, new_cases, new_cases_smoothed, total_cases_per_million, new_cases_per_million, new_cases_smoothed_per_million) VALUES(4, 4, 4200, 75, 65, 7474.626, 133.475, 115.679);
INSERT INTO Caso(id_pais, id_fecha, total_cases, new_cases, new_cases_smoothed, total_cases_per_million, new_cases_per_million, new_cases_smoothed_per_million) VALUES(5, 5, 73311, 64, 56, 82556.968, 72.072, 63.063);

INSERT INTO Muerte(id_pais, id_fecha) VALUES(1, 1);
INSERT INTO Muerte(id_pais, id_fecha, total_deaths, new_deaths, new_deaths_smoothed, total_deaths_per_million, new_deaths_per_million, new_deaths_smoothed_per_million) VALUES(2, 2, 696, 11, 7.286, 20.511, 0.324, 0.215);
INSERT INTO Muerte(id_pais, id_fecha, total_deaths, new_deaths, new_deaths_smoothed, total_deaths_per_million, new_deaths_per_million, new_deaths_smoothed_per_million) VALUES(3, 3, 5, 0, 0.143, 50.644, 0, 1.447);
INSERT INTO Muerte(id_pais, id_fecha, total_deaths, new_deaths, new_deaths_smoothed, total_deaths_per_million, new_deaths_per_million, new_deaths_smoothed_per_million) VALUES(4, 4, 41, 0, 0.429, 72.967, 0, 0.763);
INSERT INTO Muerte(id_pais, id_fecha, total_deaths, new_deaths, new_deaths_smoothed, total_deaths_per_million, new_deaths_per_million, new_deaths_smoothed_per_million) VALUES(5, 5, 374, 0, 1.286, 421.169, 0, 1.448);

INSERT INTO Rate(id_pais, id_fecha, cardiovasc_death_rate) VALUES(1, 1, 597.029);
INSERT INTO Rate(id_pais, id_fecha, reproduction_rate, cardiovasc_death_rate) VALUES(2, 2, 1.05, 276.045);
INSERT INTO Rate(id_pais, id_fecha, reproduction_rate, positive_rate, cardiovasc_death_rate) VALUES(3, 3, 0.68, 0.16, 191.511);
INSERT INTO Rate(id_pais, id_fecha, reproduction_rate, positive_rate, cardiovasc_death_rate) VALUES(4, 4, 1.11, 0.001, 182.219);
INSERT INTO Rate(id_pais, id_fecha, reproduction_rate, positive_rate, cardiovasc_death_rate) VALUES(5, 5, 1.07, 0.387, 141.171);

INSERT INTO Icu(id_pais, id_fecha) VALUES(1, 1);
INSERT INTO Icu(id_pais, id_fecha) VALUES(2, 2);
INSERT INTO Icu(id_pais, id_fecha) VALUES(3, 3);
INSERT INTO Icu(id_pais, id_fecha) VALUES(4, 4);
INSERT INTO Icu(id_pais, id_fecha, icu_patients, icu_patients_per_million) VALUES(5, 5, 8, 9.009);

INSERT INTO Info_Hospital(id_pais, id_fecha, hospital_beds_per_thousand) VALUES(1, 1, 0.5);
INSERT INTO Info_Hospital(id_pais, id_fecha) VALUES(2, 2);
INSERT INTO Info_Hospital(id_pais, id_fecha, hospital_beds_per_thousand) VALUES(3, 3, 3.8);
INSERT INTO Info_Hospital(id_pais, id_fecha, hospital_beds_per_thousand) VALUES(4, 4, 2.1);
INSERT INTO Info_Hospital(id_pais, id_fecha, hosp_patients, hosp_patients_per_million, hospital_beds_per_thousand) VALUES(5, 5, 32, 36.036, 3.4);

INSERT INTO Test(id_pais, id_fecha) VALUES(1, 1);
INSERT INTO Test(id_pais, id_fecha) VALUES(2, 2);
INSERT INTO Test(id_pais, id_fecha) VALUES(3, 3);
INSERT INTO Test(id_pais, id_fecha, new_tests, new_tests_per_thousand, new_tests_smoothed, tests_per_case, tests_units) VALUES(4, 4, 515, , 0.917, 407, 0.724, 6.3, tests performed);
INSERT INTO Test(id_pais, id_fecha, new_tests, total_tests, total_tests_per_thousand, new_tests_per_thousand, new_tests_smoothed, tests_per_case, tests_units) VALUES(5, 5, 35729, 7668213, 8635.326, 40.235, 41841, 47.118, 747.2, tests performed);

INSERT INTO Vacuna(id_pais, id_fecha, stringency_index) VALUES(1, 1, 8.33);
INSERT INTO Vacuna(id_pais, id_fecha, new_vaccinations_smoothed, new_vaccinations_smoothed_per_million, stringency_index) VALUES(2, 2, 11468, 338, 33.33);
INSERT INTO Vacuna(id_pais, id_fecha) VALUES(3, 3);
INSERT INTO Vacuna(id_pais, id_fecha, stringency_index) VALUES(4, 4, 68.98);
INSERT INTO Vacuna(id_pais, id_fecha, total_vaccinations, people_vaccinated, people_fully_vaccinated, new_vaccinations_smoothed, total_vaccinations_per_hundred, people_vaccinated_per_hundred, people_fully_vaccinated_per_hundred, new_vaccinations_smoothed_per_million, stringency_index) VALUES(5, 5, 718775, 436280, 282495, 8102, 80.94, 49.13, 31.81, 9124, 43.52);
```

## Glosario

1. DML
> Data Manipulation Language o Lenguaje de Manipulacion de Datos
2. DDL
> Data Definition Language o Lenguaje de Definicion de Datos
3. Primary Key
> Es el atributo que identifica a un conjunto de atributos, esta llave nos sirve para poder encotrar datos con mayor facilidad y evitar duplicados
4. Foreign Key
> Una llave foranea en una tabla A hace referencia a una llave primaria de una tabla B con la cual tiene relacion
5. Relacion
> Una relacion es una conexion existente entre dos tablas
6. Modelo Fisico
> El modelo fisico son todas las instrucciones con las cuales generamos las entidades, relaciones, atributos, etc.
7. Modelo Logico
> El modelo logico es una representacion grafica de las tablas y algunos ejemplos de datos ingresados
8. Modelo Conceptual
> El modelo conceptual es lo que mejor conocemos como Entidad Relacion, en este modelo podemos observar de manera grafica las entidades y sus relaciones
9. Entidad
> Una entidad o tambien conocida como tabla es el nombre que llevan los conjuntos de datos, estas tienen atributos, relaciones, restricciones, etc.
10. Atributo
> Un atributo es una parte escencial de una entidad, este tiene un tipo de dato definido, restricciones, etc.

## Notacion de Peter Chen

![ModeloConceptual](https://drive.google.com/uc?export=view&id=1m0yDe3z-wkhmtiXwEzVbk2YWBDLtaqF8)

## Notacion de Bachmann

![ModeloConceptual](https://drive.google.com/uc?export=view&id=1m5qaqXd0kFi2e9XeEZqXWm07qW6Wa8tK)

## Script Carga Masiva

#### ORACLE
```
OPTIONS (SKIP=1)
LOAD DATA INFILE 'C:\Users\jared\Desktop\Practica2_BD\owid-covid-data.csv'
INTO TABLE PROYECTO.Temporal FIELDS TERMINATED BY ','
TRAILING NULLCOLS
(
    iso_code, continent, locacion, fecha,
    total_cases, new_cases, new_cases_smoothed, total_deaths, new_deaths,
    new_deaths_smoothed, total_cases_per_million,
    new_cases_per_million,new_cases_smoothed_per_million, total_deaths_per_million,
    new_deaths_per_million, new_deaths_smoothed_per_million, reproduction_rate,
    icu_patients, icu_patients_per_million, hosp_patients, hosp_patients_per_million,
    weekly_icu_admissions,
    weekly_icu_admissions_per_million, weekly_hosp_admissions,
    weekly_hosp_admissions_per_million, new_tests, total_tests,
    total_tests_per_thousand, new_tests_per_thousand,
    new_tests_smoothed, new_tests_smoothed_per_thousand,
    positive_rate, tests_per_case, tests_units,
    total_vaccinations, people_vaccinated,
    people_fully_vaccinated, total_boosters,
    new_vaccinations, new_vaccinations_smoothed,
    total_vaccinations_per_hundred, people_vaccinated_per_hundred,
    people_fully_vaccinated_per_hundred, total_boosters_per_hundred,
    new_vaccinations_smoothed_per_million, stringency_index, population,
    population_density, median_age, aged_65_older, aged_70_older,
    gdp_per_capita, extreme_poverty, cardiovasc_death_rate,
    diabetes_prevalence, female_smokers, male_smokers,
    handwashing_facilities, hospital_beds_per_thousand, life_expectancy
    human_development_index, excess_mortality_cumulative_absolute,
    excess_mortality_cumulative, excess_mortality,
    excess_mortality_cumulative_per_million
)
```

#### MYSQL
```
LOAD DATA INFILE 'C:\Users\jared\Desktop\Practica2_BD\owid-covid-data.csv'
INTO TABLE Temporal FIELDS TERMINATED BY ','
LINES TERMINATED BY '\n'
IGNORE 1 LINES
(
    iso_code, continent, locacion, fecha, total_cases, new_cases,
    new_cases_smoothed, total_deaths, new_deaths, new_deaths_smoothed,
    total_cases_per_million, new_cases_per_million,
    new_cases_smoothed_per_million, total_deaths_per_million,
    new_deaths_per_million, new_deaths_smoothed_per_million,
    reproduction_rate, icu_patients, icu_patients_per_million,
    hosp_patients, hosp_patients_per_million, weekly_icu_admissions,
    weekly_icu_admissions_per_million, weekly_hosp_admissions,
    weekly_hosp_admissions_per_million, new_tests, total_tests,
    total_tests_per_thousand, new_tests_per_thousand,
    new_tests_smoothed, new_tests_smoothed_per_thousand, positive_rate,
    tests_per_case, tests_units, total_vaccinations, people_vaccinated,
    people_fully_vaccinated, total_boosters, new_vaccinations,
    new_vaccinations_smoothed, total_vaccinations_per_hundred,
    people_vaccinated_per_hundred, people_fully_vaccinated_per_hundred,
    total_boosters_per_hundred, new_vaccinations_smoothed_per_million,
    stringency_index, population, population_density, median_age,
    aged_65_older, aged_70_older, gdp_per_capita, extreme_poverty,
    cardiovasc_death_rate, diabetes_prevalence, female_smokers,
    male_smokers, handwashing_facilities, hospital_beds_per_thousand,
    life_expectancy, human_development_index,
    excess_mortality_cumulative_absolute, excess_mortality_cumulative,
    excess_mortality, excess_mortality_cumulative_per_million
)
```

## Creacion DB

#### ORACLE
```
-- Comando para cargar el archivo
-- sqlldr userid=PROYECTO/admin control = C:\Users\jared\Desktop\Practica2_BD\ORACLE\cargaDatos.ctl log=track.log
--Ya 0 Creacion de tabla Temporal
CREATE TABLE Temporal(
	iso_code VARCHAR2(255),
	continent VARCHAR2(255),
	locacion VARCHAR2(255),
	fecha VARCHAR2(255),
	total_cases VARCHAR2(255),
	new_cases VARCHAR2(255),
	new_cases_smoothed VARCHAR2(255),
	total_deaths VARCHAR2(255),
	new_deaths VARCHAR2(255),
	new_deaths_smoothed VARCHAR2(255),
	total_cases_per_million VARCHAR2(255),
	new_cases_per_million VARCHAR2(255),
	new_cases_smoothed_per_million VARCHAR2(255),
	total_deaths_per_million VARCHAR2(255),
	new_deaths_per_million VARCHAR2(255),
	new_deaths_smoothed_per_million VARCHAR2(255),
	reproduction_rate VARCHAR2(255),
	icu_patients VARCHAR2(255),
	icu_patients_per_million VARCHAR2(255),
	hosp_patients VARCHAR2(255),
	hosp_patients_per_million VARCHAR2(255),
	weekly_icu_admissions VARCHAR2(255),
	weekly_icu_admissions_per_million VARCHAR2(255),
	weekly_hosp_admissions VARCHAR2(255),
	weekly_hosp_admissions_per_million VARCHAR2(255),
	new_tests VARCHAR2(255),
	total_tests VARCHAR2(255),
	total_tests_per_thousand VARCHAR2(255),
	new_tests_per_thousand VARCHAR2(255),
	new_tests_smoothed VARCHAR2(255),
	new_tests_smoothed_per_thousand VARCHAR2(255),
	positive_rate VARCHAR2(255),
	tests_per_case VARCHAR2(255),
	tests_units VARCHAR2(255),
	total_vaccinations VARCHAR2(255),
	people_vaccinated VARCHAR2(255),
	people_fully_vaccinated VARCHAR2(255),
	total_boosters VARCHAR2(255),
	new_vaccinations VARCHAR2(255),
	new_vaccinations_smoothed VARCHAR2(255),
	total_vaccinations_per_hundred VARCHAR2(255),
	people_vaccinated_per_hundred VARCHAR2(255),
	people_fully_vaccinated_per_hundred VARCHAR2(255),
	total_boosters_per_hundred VARCHAR2(255),
	new_vaccinations_smoothed_per_million VARCHAR2(255),
	stringency_index VARCHAR2(255),
	population VARCHAR2(255),
	population_density VARCHAR2(255),
	median_age VARCHAR2(255),
	aged_65_older VARCHAR2(255),
	aged_70_older VARCHAR2(255),
	gdp_per_capita VARCHAR2(255),
	extreme_poverty VARCHAR2(255),
	cardiovasc_death_rate VARCHAR2(255),
	diabetes_prevalence VARCHAR2(255),
	female_smokers VARCHAR2(255),
	male_smokers VARCHAR2(255),
	handwashing_facilities VARCHAR2(255),
	hospital_beds_per_thousand VARCHAR2(255),
	life_expectancy VARCHAR2(255),
	human_development_index VARCHAR2(255),
	excess_mortality_cumulative_absolute VARCHAR2(255),
	excess_mortality_cumulative VARCHAR2(255),
	excess_mortality VARCHAR2(255),
	excess_mortality_cumulative_per_million VARCHAR2(255)
);
--Ya 1 Creacion de tabla Continente
CREATE TABLE Continente(
	id_continente NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	nombre VARCHAR2(255),
	PRIMARY KEY (id_continente)
);
--Ya 2 Creacion de tabla Fecha
CREATE TABLE Fecha(
	id_fecha NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	fecha DATE,
	PRIMARY KEY (id_fecha)
);
--Ya 3 Creacion de tabla Pais
CREATE TABLE Pais(
	id_pais NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	id_continente NUMBER NOT NULL,
	iso_code VARCHAR2(255),
	nombre VARCHAR2(255),
	population NUMBER,
	population_density DECIMAL,
	median_age DECIMAL,
	aged_65_older DECIMAL,
	aged_70_older DECIMAL,
	gdp_per_capita DECIMAL,
	extreme_poverty DECIMAL,
	diabetes_prevalence DECIMAL,
	female_smokers DECIMAL,
	male_smokers DECIMAL,
	handwashing_facilities DECIMAL,
	life_expectancy DECIMAL,
	human_development_index DECIMAL,
	PRIMARY KEY (id_pais),
	CONSTRAINT fk_id_continente 
		FOREIGN KEY (id_continente) 
		REFERENCES Continente (id_continente)
);
--Ya 4 Creacion de tabla Casos
CREATE TABLE Casos(
	id_casos NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	id_pais NUMBER NOT NULL,
	id_fecha NUMBER NOT NULL,
	total_cases NUMBER,
	new_cases NUMBER,
	new_cases_smoothed FLOAT,
	total_cases_per_million FLOAT,
	new_cases_per_million FLOAT,
	new_cases_smoothed_per_million FLOAT,
	PRIMARY KEY (id_casos),
	CONSTRAINT fk_id_pais_casos
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_casos
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 5 Creacion de tabla Muertes
CREATE TABLE Muertes(
	id_muertes NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	id_pais NUMBER NOT NULL,
	id_fecha NUMBER NOT NULL,
	total_deaths NUMBER,
	new_deaths NUMBER,
	new_deaths_smoothed FLOAT,
	total_deaths_per_million FLOAT,
	new_deaths_per_million FLOAT,
	new_deaths_smoothed_per_million FLOAT,
	PRIMARY KEY (id_muertes),
	CONSTRAINT fk_id_pais_muertes
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_muertes
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 6 Creacion de tabla Rates
CREATE TABLE Rates(
	id_rates NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	id_pais NUMBER NOT NULL,
	id_fecha NUMBER NOT NULL,
	reproduction_rate FLOAT,
	positive_rate FLOAT,
	cardiovasc_death_rate FLOAT,
	PRIMARY KEY (id_rates),
	CONSTRAINT fk_id_pais_rates
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_rates
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 7 Creacion de tabla Icu
CREATE TABLE Icu(
	id_icu NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	id_pais NUMBER NOT NULL,
	id_fecha NUMBER NOT NULL,
	icu_patients NUMBER,
	icu_patients_per_million FLOAT,
	weekly_icu_admissions FLOAT,
	weekly_icu_admissions_per_million FLOAT,
	PRIMARY KEY (id_icu),
	CONSTRAINT fk_id_pais_icu
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_icu
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 8 Creacion de tabla HospitalInfo
CREATE TABLE HospitalInfo(
	id_hospital_info NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	id_pais NUMBER NOT NULL,
	id_fecha NUMBER NOT NULL,
	hosp_patients NUMBER,
	hosp_patients_per_million FLOAT,
	weekly_hosp_admissions FLOAT,
	weekly_hosp_admissions_per_million FLOAT,
	hospital_beds_per_thousand FLOAT,
	PRIMARY KEY (id_hospital_info),
	CONSTRAINT fk_id_pais_hospital_info
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_hospital_info
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 9 Creacion de tabla Test
CREATE TABLE Test(
	id_test NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	id_pais NUMBER NOT NULL,
	id_fecha NUMBER NOT NULL,
	new_tests NUMBER,
	total_tests NUMBER,
	total_tests_per_thousand FLOAT,
	new_tests_per_thousand FLOAT,
	new_tests_smoothed FLOAT,
	new_tests_smoothed_per_thousand FLOAT,
	tests_per_case FLOAT,
	tests_units VARCHAR2(255),
	PRIMARY KEY (id_test),
	CONSTRAINT fk_id_pais_test
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_test
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 10 Creacion de tabla Vacuna
CREATE TABLE Vacuna(
	id_vacuna NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	id_pais NUMBER NOT NULL,
	id_fecha NUMBER NOT NULL,
	total_vaccinations NUMBER,
	people_vaccinated NUMBER,
	people_fully_vaccinated NUMBER,
	new_vaccinations NUMBER,
	new_vaccinations_smoothed FLOAT,
	total_vaccinations_per_hundred FLOAT,
	people_vaccinated_per_hundred FLOAT,
	people_fully_vaccinated_per_hundred FLOAT,
	new_vaccinations_smoothed_per_million FLOAT,
	stringency_index FLOAT,
	PRIMARY KEY (id_vacuna),
	CONSTRAINT fk_id_pais_vacuna
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_vacuna
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 11 Creacion de tabla Boosters
CREATE TABLE Boosters(
	id_booster NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	id_pais NUMBER NOT NULL,
	id_fecha NUMBER NOT NULL,
	total_boosters DECIMAL,
	total_boosters_per_hundred DECIMAL,
	PRIMARY KEY (id_booster),
	CONSTRAINT fk_id_pais_booster
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_booster
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 12 Creacion de tabla Mortality
CREATE TABLE Mortality(
	id_mortality NUMBER GENERATED ALWAYS AS IDENTITY(START WITH 1 INCREMENT BY 1),
	id_pais NUMBER NOT NULL,
	id_fecha NUMBER NOT NULL,
	excess_mortality_cumulative_absolute DECIMAL,
	excess_mortality_cumulative DECIMAL,
	excess_mortality DECIMAL,
	excess_mortality_cumulative_per_million DECIMAL,
	PRIMARY KEY (id_mortality),
	CONSTRAINT fk_id_pais_mortality
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_mortality
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);

-- Area para eliminar las tablas
DROP TABLE Temporal;
DROP TABLE Casos;
DROP TABLE Muertes;
DROP TABLE Rates;
DROP TABLE Icu;
DROP TABLE HospitalInfo;
DROP TABLE Test;
DROP TABLE Vacuna;
DROP TABLE Boosters;
DROP TABLE Pais;
DROP TABLE Fecha;
DROP TABLE Continente;
DROP TABLE Mortality;
```

#### MYSQL
```
-- Comando para cargar el archivo
--Ya 0 Creacion de tabla Temporal
DROP TABLE IF EXISTS Temporal;
CREATE TABLE Temporal(
	iso_code VARCHAR(255),
	continent VARCHAR(255),
	locacion VARCHAR(255),
	fecha VARCHAR(255),
	total_cases VARCHAR(255),
	new_cases VARCHAR(255),
	new_cases_smoothed VARCHAR(255),
	total_deaths VARCHAR(255),
	new_deaths VARCHAR(255),
	new_deaths_smoothed VARCHAR(255),
	total_cases_per_million VARCHAR(255),
	new_cases_per_million VARCHAR(255),
	new_cases_smoothed_per_million VARCHAR(255),
	total_deaths_per_million VARCHAR(255),
	new_deaths_per_million VARCHAR(255),
	new_deaths_smoothed_per_million VARCHAR(255),
	reproduction_rate VARCHAR(255),
	icu_patients VARCHAR(255),
	icu_patients_per_million VARCHAR(255),
	hosp_patients VARCHAR(255),
	hosp_patients_per_million VARCHAR(255),
	weekly_icu_admissions VARCHAR(255),
	weekly_icu_admissions_per_million VARCHAR(255),
	weekly_hosp_admissions VARCHAR(255),
	weekly_hosp_admissions_per_million VARCHAR(255),
	new_tests VARCHAR(255),
	total_tests VARCHAR(255),
	total_tests_per_thousand VARCHAR(255),
	new_tests_per_thousand VARCHAR(255),
	new_tests_smoothed VARCHAR(255),
	new_tests_smoothed_per_thousand VARCHAR(255),
	positive_rate VARCHAR(255),
	tests_per_case VARCHAR(255),
	tests_units VARCHAR(255),
	total_vaccinations VARCHAR(255),
	people_vaccinated VARCHAR(255),
	people_fully_vaccinated VARCHAR(255),
	total_boosters VARCHAR(255),
	new_vaccinations VARCHAR(255),
	new_vaccinations_smoothed VARCHAR(255),
	total_vaccinations_per_hundred VARCHAR(255),
	people_vaccinated_per_hundred VARCHAR(255),
	people_fully_vaccinated_per_hundred VARCHAR(255),
	total_boosters_per_hundred VARCHAR(255),
	new_vaccinations_smoothed_per_million VARCHAR(255),
	stringency_index VARCHAR(255),
	population VARCHAR(255),
	population_density VARCHAR(255),
	median_age VARCHAR(255),
	aged_65_older VARCHAR(255),
	aged_70_older VARCHAR(255),
	gdp_per_capita VARCHAR(255),
	extreme_poverty VARCHAR(255),
	cardiovasc_death_rate VARCHAR(255),
	diabetes_prevalence VARCHAR(255),
	female_smokers VARCHAR(255),
	male_smokers VARCHAR(255),
	handwashing_facilities VARCHAR(255),
	hospital_beds_per_thousand VARCHAR(255),
	life_expectancy VARCHAR(255),
	human_development_index VARCHAR(255),
	excess_mortality_cumulative_absolute VARCHAR(255),
	excess_mortality_cumulative VARCHAR(255),
	excess_mortality VARCHAR(255),
	excess_mortality_cumulative_per_million VARCHAR(255)
);
--Ya 1 Creacion de tabla Continente
DROP TABLE IF EXISTS Continente;
CREATE TABLE Continente(
	id_continente INT NOT NULL AUTO_INCREMENT,
	nombre VARCHAR(255),
	PRIMARY KEY (id_continente)
);
--Ya 2 Creacion de tabla Fecha
DROP TABLE IF EXISTS Fecha;
CREATE TABLE Fecha(
	id_fecha INT NOT NULL AUTO_INCREMENT,
	fecha DATE,
	PRIMARY KEY (id_fecha)
);
--Ya 3 Creacion de tabla Pais
DROP TABLE IF EXISTS Pais;
CREATE TABLE Pais(
	id_pais INT NOT NULL AUTO_INCREMENT,
	id_continente INT NOT NULL,
	iso_code VARCHAR(255),
	nombre VARCHAR(255),
	population INT,
	population_density FLOAT,
	median_age FLOAT,
	aged_65_older FLOAT,
	aged_70_older FLOAT,
	gdp_per_capita FLOAT,
	extreme_poverty FLOAT,
	diabetes_prevalence FLOAT,
	female_smokers FLOAT,
	male_smokers FLOAT,
	handwashing_facilities FLOAT,
	life_expectancy FLOAT,
	human_development_index FLOAT,
	PRIMARY KEY (id_pais),
	CONSTRAINT fk_id_continente 
		FOREIGN KEY (id_continente) 
		REFERENCES Continente (id_continente)
);
--Ya 4 Creacion de tabla Casos
DROP TABLE IF EXISTS Casos;
CREATE TABLE Casos(
	id_casos INT NOT NULL AUTO_INCREMENT,
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	total_cases INT,
	new_cases INT,
	new_cases_smoothed FLOAT,
	total_cases_per_million FLOAT,
	new_cases_per_million FLOAT,
	new_cases_smoothed_per_million FLOAT,
	PRIMARY KEY (id_casos),
	CONSTRAINT fk_id_pais_casos
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_casos
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 5 Creacion de tabla Muertes
DROP TABLE IF EXISTS Muertes;
CREATE TABLE Muertes(
	id_muertes INT NOT NULL AUTO_INCREMENT,
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	total_deaths INT,
	new_deaths INT,
	new_deaths_smoothed FLOAT,
	total_deaths_per_million FLOAT,
	new_deaths_per_million FLOAT,
	new_deaths_smoothed_per_million FLOAT,
	PRIMARY KEY (id_muertes),
	CONSTRAINT fk_id_pais_muertes
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_muertes
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 6 Creacion de tabla Rates
DROP TABLE IF EXISTS Rates;
CREATE TABLE Rates(
	id_rates INT NOT NULL AUTO_INCREMENT,
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	reproduction_rate FLOAT,
	positive_rate FLOAT,
	cardiovasc_death_rate FLOAT,
	PRIMARY KEY (id_rates),
	CONSTRAINT fk_id_pais_rates
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_rates
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 7 Creacion de tabla Icu
DROP TABLE IF EXISTS Icu;
CREATE TABLE Icu(
	id_icu INT NOT NULL AUTO_INCREMENT,
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	icu_patients INT,
	icu_patients_per_million FLOAT,
	weekly_icu_admissions FLOAT,
	weekly_icu_admissions_per_million FLOAT,
	PRIMARY KEY (id_icu),
	CONSTRAINT fk_id_pais_icu
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_icu
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 8 Creacion de tabla HospitalInfo
DROP TABLE IF EXISTS HospitalInfo;
CREATE TABLE HospitalInfo(
	id_hospital_info INT NOT NULL AUTO_INCREMENT,
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	hosp_patients INT,
	hosp_patients_per_million FLOAT,
	weekly_hosp_admissions FLOAT,
	weekly_hosp_admissions_per_million FLOAT,
	hospital_beds_per_thousand FLOAT,
	PRIMARY KEY (id_hospital_info),
	CONSTRAINT fk_id_pais_hospital_info
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_hospital_info
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 9 Creacion de tabla Test
DROP TABLE IF EXISTS Test;
CREATE TABLE Test(
	id_test INT NOT NULL AUTO_INCREMENT,
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	new_tests INT,
	total_tests INT,
	total_tests_per_thousand FLOAT,
	new_tests_per_thousand FLOAT,
	new_tests_smoothed FLOAT,
	new_tests_smoothed_per_thousand FLOAT,
	tests_per_case FLOAT,
	tests_units VARCHAR(255),
	PRIMARY KEY (id_test),
	CONSTRAINT fk_id_pais_test
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_test
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 10 Creacion de tabla Vacuna
DROP TABLE IF EXISTS Vacuna;
CREATE TABLE Vacuna(
	id_vacuna INT NOT NULL AUTO_INCREMENT,
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	total_vaccinations INT,
	people_vaccinated INT,
	people_fully_vaccinated INT,
	new_vaccinations INT,
	new_vaccinations_smoothed FLOAT,
	total_vaccinations_per_hundred FLOAT,
	people_vaccinated_per_hundred FLOAT,
	people_fully_vaccinated_per_hundred FLOAT,
	new_vaccinations_smoothed_per_million FLOAT,
	stringency_index FLOAT,
	PRIMARY KEY (id_vacuna),
	CONSTRAINT fk_id_pais_vacuna
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_vacuna
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 11 Creacion de tabla Boosters
DROP TABLE IF EXISTS Boosters;
CREATE TABLE Boosters(
	id_booster INT NOT NULL AUTO_INCREMENT,
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	total_boosters FLOAT,
	total_boosters_per_hundred FLOAT,
	PRIMARY KEY (id_booster),
	CONSTRAINT fk_id_pais_booster
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_booster
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);
--Ya 12 Creacion de tabla Mortality
DROP TABLE IF EXISTS Mortality;
CREATE TABLE Mortality(
	id_mortality INT NOT NULL AUTO_INCREMENT,
	id_pais INT NOT NULL,
	id_fecha INT NOT NULL,
	excess_mortality_cumulative_absolute FLOAT,
	excess_mortality_cumulative FLOAT,
	excess_mortality FLOAT,
	excess_mortality_cumulative_per_million FLOAT,
	PRIMARY KEY (id_mortality),
	CONSTRAINT fk_id_pais_mortality
		FOREIGN KEY (id_pais)
		REFERENCES Pais (id_pais),
	CONSTRAINT fk_id_fecha_mortality
		FOREIGN KEY (id_fecha)
		REFERENCES Fecha (id_fecha)
);

-- Area para eliminar las tablas
DROP TABLE Temporal;
DROP TABLE Casos;
DROP TABLE Muertes;
DROP TABLE Rates;
DROP TABLE Icu;
DROP TABLE HospitalInfo;
DROP TABLE Test;
DROP TABLE Vacuna;
DROP TABLE Boosters;
DROP TABLE Pais;
DROP TABLE Fecha;
DROP TABLE Continente;
DROP TABLE Mortality;
```

## Carga de Modelo

#### ORACLE
```
-- Continente
	INSERT INTO CONTINENTE(nombre) SELECT DISTINCT CONTINENT FROM Temporal;

-- Pais
	INSERT INTO Pais(id_continente, iso_code, nombre, population, population_density, median_age, aged_65_older,
	    aged_70_older, gdp_per_capita, extreme_poverty, diabetes_prevalence, female_smokers, male_smokers,
	    handwashing_facilities, life_expectancy, human_development_index)
	    SELECT DISTINCT Continente.id_continente, Temporal.iso_code, Temporal.locacion, Temporal.population,
	    	Temporal.population_density, Temporal.median_age,Temporal.aged_65_older, Temporal.aged_70_older,
	    	Temporal.gdp_per_capita, Temporal.extreme_poverty, Temporal.diabetes_prevalence, Temporal.female_smokers,
	    	Temporal.male_smokers, Temporal.handwashing_facilities, Temporal.life_expectancy,
	    	Temporal.human_development_index
	    FROM Temporal, Continente
	    WHERE Temporal.continent = Continente.nombre OR (Temporal.continent IS NULL AND Continente.nombre IS NULL);

-- Fecha
	INSERT INTO Fecha(fecha) SELECT DISTINCT TO_DATE(FECHA, 'YYYY MM DD') FROM Temporal;

-- Casos
	INSERT INTO Casos(id_pais, id_fecha, total_cases, new_cases, new_cases_smoothed, total_cases_per_million,
	    	new_cases_per_million, new_cases_smoothed_per_million)
	    SELECT Pais.id_pais, Fecha.id_fecha, Temporal.total_cases, Temporal.new_cases, Temporal.new_cases_smoothed,
	        Temporal.total_cases_per_million, Temporal.new_cases_per_million, Temporal.new_cases_smoothed_per_million
	    FROM Temporal, Pais, Fecha
	    WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Muertes
	INSERT INTO Muertes(id_pais, id_fecha, total_deaths, new_deaths, new_deaths_smoothed, total_deaths_per_million,
	    	new_deaths_per_million, new_deaths_smoothed_per_million)
	    SELECT Pais.id_pais, Fecha.id_fecha, Temporal.total_deaths, Temporal.new_deaths, Temporal.new_deaths_smoothed,
	        Temporal.total_deaths_per_million, Temporal.new_deaths_per_million, Temporal.new_deaths_smoothed_per_million
	    FROM Temporal, Pais, Fecha
	    WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Rates
	INSERT INTO Rates(id_pais, id_fecha, reproduction_rate, positive_rate, cardiovasc_death_rate)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.reproduction_rate, Temporal.positive_rate, Temporal.cardiovasc_death_rate
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Icu
	INSERT INTO Icu(id_pais, id_fecha, icu_patients, icu_patients_per_million, weekly_icu_admissions, weekly_icu_admissions_per_million)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.icu_patients, Temporal.icu_patients_per_million,
    	    Temporal.weekly_icu_admissions, Temporal.weekly_icu_admissions_per_million
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- HospitalInfo
	INSERT INTO HospitalInfo(id_pais, id_fecha, hosp_patients, hosp_patients_per_million, weekly_hosp_admissions,
    	    weekly_hosp_admissions_per_million, hospital_beds_per_thousand)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.hosp_patients, Temporal.hosp_patients_per_million,
    	    Temporal.weekly_hosp_admissions, Temporal.weekly_hosp_admissions_per_million, Temporal.hospital_beds_per_thousand
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Test
	INSERT INTO Test(id_pais, id_fecha, new_tests, total_tests, total_tests_per_thousand, new_tests_per_thousand,
	    	new_tests_smoothed, new_tests_smoothed_per_thousand, tests_per_case, tests_units)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.new_tests, Temporal.total_tests, Temporal.total_tests_per_thousand,
    	    Temporal.new_tests_per_thousand, Temporal.new_tests_smoothed, Temporal.new_tests_smoothed_per_thousand,
    	    Temporal.tests_per_case, tests_units
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Vacuna
	INSERT INTO Vacuna(id_pais, id_fecha, total_vaccinations, people_vaccinated, people_fully_vaccinated, new_vaccinations,
        new_vaccinations_smoothed, total_vaccinations_per_hundred, people_vaccinated_per_hundred,
        people_fully_vaccinated_per_hundred, new_vaccinations_smoothed_per_million, stringency_index)
    SELECT Pais.id_pais, Fecha.id_fecha, Temporal.total_vaccinations, Temporal.people_vaccinated,
        Temporal.people_fully_vaccinated, Temporal.new_vaccinations, Temporal.new_vaccinations_smoothed,
        Temporal.total_vaccinations_per_hundred, Temporal.people_vaccinated_per_hundred,
        Temporal.people_fully_vaccinated_per_hundred, Temporal.new_vaccinations_smoothed_per_million, Temporal.stringency_index
    FROM Temporal, Pais, Fecha
    WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Boosters
	INSERT INTO Boosters(id_pais, id_fecha, total_boosters, total_boosters_per_hundred)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.total_boosters, Temporal.total_boosters_per_hundred
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Mortality
	INSERT INTO Mortality(id_pais, id_fecha, excess_mortality_cumulative_absolute, excess_mortality_cumulative,
            excess_mortality, excess_mortality_cumulative_per_million)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.excess_mortality_cumulative_absolute, Temporal.excess_mortality_cumulative,
            Temporal.excess_mortality, excess_mortality_cumulative_per_million
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

```

#### MYSQL
```
-- Continente
	INSERT INTO CONTINENTE(nombre) SELECT DISTINCT CONTINENT FROM Temporal;

-- Pais
	INSERT INTO Pais(id_continente, iso_code, nombre, population, population_density, median_age, aged_65_older,
	    aged_70_older, gdp_per_capita, extreme_poverty, diabetes_prevalence, female_smokers, male_smokers,
	    handwashing_facilities, life_expectancy, human_development_index)
	    SELECT DISTINCT Continente.id_continente, Temporal.iso_code, Temporal.locacion, Temporal.population,
	    	Temporal.population_density, Temporal.median_age,Temporal.aged_65_older, Temporal.aged_70_older,
	    	Temporal.gdp_per_capita, Temporal.extreme_poverty, Temporal.diabetes_prevalence, Temporal.female_smokers,
	    	Temporal.male_smokers, Temporal.handwashing_facilities, Temporal.life_expectancy,
	    	Temporal.human_development_index
	    FROM Temporal, Continente
	    WHERE Temporal.continent = Continente.nombre OR (Temporal.continent IS NULL AND Continente.nombre IS NULL);

-- Fecha
	INSERT INTO Fecha(fecha) SELECT DISTINCT TO_DATE(FECHA, 'YYYY MM DD') FROM Temporal;

-- Casos
	INSERT INTO Casos(id_pais, id_fecha, total_cases, new_cases, new_cases_smoothed, total_cases_per_million,
	    	new_cases_per_million, new_cases_smoothed_per_million)
	    SELECT Pais.id_pais, Fecha.id_fecha, Temporal.total_cases, Temporal.new_cases, Temporal.new_cases_smoothed,
	        Temporal.total_cases_per_million, Temporal.new_cases_per_million, Temporal.new_cases_smoothed_per_million
	    FROM Temporal, Pais, Fecha
	    WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Muertes
	INSERT INTO Muertes(id_pais, id_fecha, total_deaths, new_deaths, new_deaths_smoothed, total_deaths_per_million,
	    	new_deaths_per_million, new_deaths_smoothed_per_million)
	    SELECT Pais.id_pais, Fecha.id_fecha, Temporal.total_deaths, Temporal.new_deaths, Temporal.new_deaths_smoothed,
	        Temporal.total_deaths_per_million, Temporal.new_deaths_per_million, Temporal.new_deaths_smoothed_per_million
	    FROM Temporal, Pais, Fecha
	    WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Rates
	INSERT INTO Rates(id_pais, id_fecha, reproduction_rate, positive_rate, cardiovasc_death_rate)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.reproduction_rate, Temporal.positive_rate, Temporal.cardiovasc_death_rate
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Icu
	INSERT INTO Icu(id_pais, id_fecha, icu_patients, icu_patients_per_million, weekly_icu_admissions, weekly_icu_admissions_per_million)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.icu_patients, Temporal.icu_patients_per_million,
    	    Temporal.weekly_icu_admissions, Temporal.weekly_icu_admissions_per_million
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- HospitalInfo
	INSERT INTO HospitalInfo(id_pais, id_fecha, hosp_patients, hosp_patients_per_million, weekly_hosp_admissions,
    	    weekly_hosp_admissions_per_million, hospital_beds_per_thousand)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.hosp_patients, Temporal.hosp_patients_per_million,
    	    Temporal.weekly_hosp_admissions, Temporal.weekly_hosp_admissions_per_million, Temporal.hospital_beds_per_thousand
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Test
	INSERT INTO Test(id_pais, id_fecha, new_tests, total_tests, total_tests_per_thousand, new_tests_per_thousand,
	    	new_tests_smoothed, new_tests_smoothed_per_thousand, tests_per_case, tests_units)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.new_tests, Temporal.total_tests, Temporal.total_tests_per_thousand,
    	    Temporal.new_tests_per_thousand, Temporal.new_tests_smoothed, Temporal.new_tests_smoothed_per_thousand,
    	    Temporal.tests_per_case, tests_units
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Vacuna
	INSERT INTO Vacuna(id_pais, id_fecha, total_vaccinations, people_vaccinated, people_fully_vaccinated, new_vaccinations,
        new_vaccinations_smoothed, total_vaccinations_per_hundred, people_vaccinated_per_hundred,
        people_fully_vaccinated_per_hundred, new_vaccinations_smoothed_per_million, stringency_index)
    SELECT Pais.id_pais, Fecha.id_fecha, Temporal.total_vaccinations, Temporal.people_vaccinated,
        Temporal.people_fully_vaccinated, Temporal.new_vaccinations, Temporal.new_vaccinations_smoothed,
        Temporal.total_vaccinations_per_hundred, Temporal.people_vaccinated_per_hundred,
        Temporal.people_fully_vaccinated_per_hundred, Temporal.new_vaccinations_smoothed_per_million, Temporal.stringency_index
    FROM Temporal, Pais, Fecha
    WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Boosters
	INSERT INTO Boosters(id_pais, id_fecha, total_boosters, total_boosters_per_hundred)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.total_boosters, Temporal.total_boosters_per_hundred
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

-- Mortality
	INSERT INTO Mortality(id_pais, id_fecha, excess_mortality_cumulative_absolute, excess_mortality_cumulative,
            excess_mortality, excess_mortality_cumulative_per_million)
    	SELECT Pais.id_pais, Fecha.id_fecha, Temporal.excess_mortality_cumulative_absolute, Temporal.excess_mortality_cumulative,
            Temporal.excess_mortality, excess_mortality_cumulative_per_million
    	FROM Temporal, Pais, Fecha
    	WHERE Temporal.locacion = Pais.nombre AND TO_DATE(Temporal.fecha, 'YYYY MM DD') = Fecha.fecha;

```

## Consultas

#### ORACLE
```
-- set serveroutput on size unlimited;
-- Consulta 1
	SELECT Pais.nombre AS Pais, COALESCE(SUM(Casos.new_cases), 0) AS "Actuales por Sumatoria", COALESCE(MAX(Casos.total_cases), 0) AS "Actuales por Total" 
		FROM Pais, Casos, Continente
		WHERE Casos.id_pais = Pais.id_pais AND Pais.id_continente = Continente.id_continente AND Continente.nombre IS NOT NULL
		GROUP BY Pais.nombre;

-- Consulta 2
	CREATE OR REPLACE PROCEDURE consulta2 (
    	p_pais           VARCHAR2,
    	p_salida    IN OUT SYS_REFCURSOR
	)
	IS
	BEGIN
	    OPEN p_salida FOR SELECT SUM(Casos.new_cases) AS Casos, SUM(Muertes.new_deaths) AS Muertes, SUM(Vacuna.new_vaccinations) AS Vacunas,
				EXTRACT(month FROM Fecha.fecha) AS M, TO_CHAR(Fecha.fecha, 'Month') AS Mes, EXTRACT(year FROM Fecha.fecha) AS Year
			FROM Pais, Casos, Fecha, Muertes, Vacuna
			WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha AND Pais.nombre = p_pais
				AND Casos.id_pais = Muertes.id_pais AND Casos.id_fecha = Muertes.id_fecha AND Casos.id_pais = Vacuna.id_pais
				AND Casos.id_fecha = Vacuna.id_fecha
			GROUP BY TO_CHAR(Fecha.fecha, 'Month'), EXTRACT(month FROM Fecha.fecha), EXTRACT(year FROM Fecha.fecha)
			ORDER BY EXTRACT(year FROM Fecha.fecha) ASC, EXTRACT(month FROM Fecha.fecha);
	END;

	DECLARE
	    v_casos NUMBER;
	    v_muertes NUMBER;
	    v_vacunas NUMBER;
	    v_m NUMBER;
	    v_mes VARCHAR2(32);
	    v_year NUMBER;
	    v_salida    SYS_REFCURSOR;
	BEGIN
	    DBMS_OUTPUT.ENABLE;
	    DBMS_OUTPUT.PUT_LINE('Casos    Muertes    Vacunas    Month    Year');
	    DBMS_OUTPUT.PUT_LINE('-------    -------    -------    -------    -------');
	    consulta2('United States', v_salida);
	    LOOP
	        FETCH v_salida INTO v_casos, v_muertes, v_vacunas, v_m, v_mes, v_year;
	        EXIT WHEN v_salida%NOTFOUND;
	        DBMS_OUTPUT.PUT_LINE(
	        	v_casos || '             ' ||
	        	v_muertes || '             ' ||
	        	v_vacunas || '             ' ||
	        	v_mes || '             ' ||
	        	v_year
	        );
	    END LOOP;
	    CLOSE v_salida;
	END;

-- Consulta 3
	SELECT Continente.nombre AS "Continente", SUM(Casos.new_cases) AS "Cantidad de contagios"
	    FROM Continente, Pais, Casos, Fecha, Dual
	    WHERE Casos.id_pais = Pais.id_pais AND Pais.id_continente = Continente.id_continente AND Casos.id_fecha = Fecha.id_fecha
            AND Continente.nombre IS NOT NULL
	        AND (EXTRACT(month FROM Fecha.fecha) - EXTRACT(month FROM CURRENT_DATE)) <= 3
	        AND (EXTRACT(year FROM Fecha.fecha) = EXTRACT(year FROM CURRENT_DATE))
	    GROUP BY Continente.nombre;

-- Consulta 4
	SELECT t1.Pais, ROUND((t2."Casos 1-2021" / t1."Casos 12-2020"), 2) AS "Crecimiento en %" FROM 
		(
			(
				SELECT Pais.nombre AS Pais, SUM(Casos.new_cases) AS "Casos 12-2020"
		    		FROM Pais, Fecha, Casos
		    		WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha
		    			AND EXTRACT(month FROM Fecha.fecha) = 12
		    			AND EXTRACT(year FROM Fecha.fecha) = 2020
		    		GROUP BY Pais.nombre
		    		HAVING SUM(Casos.new_cases) > 0
		    ) t1
		)
		LEFT JOIN
		(
			(
				SELECT Pais.nombre AS Pais, SUM(Casos.new_cases) AS "Casos 1-2021"
		    		FROM Pais, Fecha, Casos
		    		WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha
		    			AND EXTRACT(month FROM Fecha.fecha) = 1
		    			AND EXTRACT(year FROM Fecha.fecha) = 2021
		    		GROUP BY Pais.nombre
		    		HAVING SUM(Casos.new_cases) > 0
		    ) t2
		)
		ON t1.pais = t2.pais
		ORDER BY "Crecimiento en %" DESC;

-- Consulta 5
	SELECT Pais.nombre AS Pais, COALESCE(ROUND(AVG(Casos.new_cases), 2), 0) AS Contagios
		FROM Pais, Casos, Fecha, Continente
		WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha
		    AND EXTRACT(year FROM Fecha.fecha) = 2020
		    AND EXTRACT(month FROM Fecha.fecha) BETWEEN 1 AND 3
            AND Pais.id_continente = Continente.id_continente
            AND Continente.nombre IS NOT NULL
		GROUP BY Pais.nombre;

-- Consulta 6
	CREATE OR REPLACE PROCEDURE consulta6 (
    	p_inferior           NUMBER,
        p_superior           NUMBER,
    	p_salida    IN OUT SYS_REFCURSOR
	)
	IS
	BEGIN
        IF p_inferior < p_superior THEN
            OPEN p_salida FOR SELECT Pais.nombre, Fecha.fecha, SUM(Casos.new_cases)
                FROM Casos, Pais, Fecha, Continente
                WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha
                AND Casos.new_cases BETWEEN p_inferior AND p_superior
                AND Pais.id_continente = Continente.id_continente
            	AND Continente.nombre IS NOT NULL
                GROUP BY Pais.nombre, Fecha.fecha
                FETCH NEXT 600 ROWS ONLY;
        ELSIF p_superior < p_inferior THEN
            OPEN p_salida FOR SELECT Pais.nombre, Fecha.fecha, SUM(Casos.new_cases)
                FROM Casos, Pais, Fecha, Continente
                WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha
                AND Casos.new_cases BETWEEN p_superior AND p_inferior
                AND Pais.id_continente = Continente.id_continente
            	AND Continente.nombre IS NOT NULL
                GROUP BY Pais.nombre, Fecha.fecha
                FETCH NEXT 600 ROWS ONLY;
        END IF;
	END;

    DECLARE
	    v_nombre VARCHAR(256);
        v_fecha DATE;
        v_suma NUMBER;
	    v_salida    SYS_REFCURSOR;
	BEGIN
	    DBMS_OUTPUT.ENABLE;
	    DBMS_OUTPUT.PUT_LINE('Nombre    Fecha    Cantidad');
	    DBMS_OUTPUT.PUT_LINE('-------    Fecha    Cantidad');
	    consulta6(80000, 90000, v_salida);
	    LOOP
	        FETCH v_salida INTO v_nombre, v_fecha, v_suma;
	        EXIT WHEN v_salida%NOTFOUND;
	        DBMS_OUTPUT.PUT_LINE(v_nombre || '             ' || v_fecha || '             ' || v_suma);
	    END LOOP;
	    CLOSE v_salida;
	END;

-- Consulta 7
	CREATE OR REPLACE PROCEDURE consulta7 (
    	p_salida    IN OUT SYS_REFCURSOR
	)
	IS
	BEGIN
        OPEN p_salida FOR SELECT Pais.nombre AS Pais, SUM(Test.new_tests) AS Pruebas
            FROM Pais, Test
            WHERE Test.id_pais = Pais.id_pais AND Test.new_tests IS NOT NULL
            GROUP BY Pais.nombre
            ORDER BY SUM(Test.new_tests) DESC
            FETCH NEXT 10 ROWS ONLY;
	END;

    DECLARE
	    v_nombre VARCHAR(256);
        v_pruebas NUMBER;
	    v_salida    SYS_REFCURSOR;
	BEGIN
	    DBMS_OUTPUT.ENABLE;
	    DBMS_OUTPUT.PUT_LINE('Pais    Pruebas');
	    DBMS_OUTPUT.PUT_LINE('-------    -------');
	    consulta7(v_salida);
	    LOOP
	        FETCH v_salida INTO v_nombre, v_pruebas;
	        EXIT WHEN v_salida%NOTFOUND;
	        DBMS_OUTPUT.PUT_LINE(v_nombre || '             ' || v_pruebas);
	    END LOOP;
	    CLOSE v_salida;
	END;

-- Consulta 8
	CREATE OR REPLACE PROCEDURE consulta8 (
        p_fecha VARCHAR2,
    	p_salida    IN OUT SYS_REFCURSOR
	)
	IS
	BEGIN
        OPEN p_salida FOR SELECT Pais.nombre AS Pais, Muertes.new_deaths AS Muertes
    	FROM Pais, Muertes, Fecha, Continente
    	WHERE Muertes.id_pais = Pais.id_pais AND Muertes.id_fecha = Fecha.id_fecha
    	    AND Fecha.fecha = TO_DATE(p_fecha, 'YYYY MM DD')
    	    AND Muertes.new_deaths IS NOT NULL
            AND Pais.id_continente = Continente.id_continente
            AND Continente.nombre IS NOT NULL
    	ORDER BY Muertes.new_deaths DESC
    	FETCH NEXT 1 ROWS ONLY;
	END;

    DECLARE
	    v_pais VARCHAR(256);
        v_muertes NUMBER;
	    v_salida    SYS_REFCURSOR;
	BEGIN
	    DBMS_OUTPUT.ENABLE;
	    DBMS_OUTPUT.PUT_LINE('Pais    Muertes');
	    DBMS_OUTPUT.PUT_LINE('-------    -------');
	    consulta8('2020-08-23', v_salida);
	    LOOP
	        FETCH v_salida INTO v_pais, v_muertes;
	        EXIT WHEN v_salida%NOTFOUND;
	        DBMS_OUTPUT.PUT_LINE(v_pais || '             ' || v_muertes);
	    END LOOP;
	    CLOSE v_salida;
	END;

-- Consulta 9
	-- Muertes, Casos, Vacunas
	CREATE OR REPLACE PROCEDURE consulta9 (
    	p_inferior           VARCHAR2,
        p_superior           VARCHAR2,
    	p_salida    IN OUT SYS_REFCURSOR
	)
	IS
	BEGIN
	    OPEN p_salida FOR SELECT Casos.new_cases, Casos.total_cases, Vacuna.new_vaccinations, Vacuna.total_vaccinations, Muertes.new_deaths, Muertes.total_deaths,
            Test.new_tests, Test.total_tests, Fecha.fecha
        FROM Casos, Muertes, Vacuna, Test, Pais, Fecha
        WHERE 
            Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha AND
            Muertes.id_pais = Pais.id_pais AND Muertes.id_fecha = Fecha.id_fecha AND
            Vacuna.id_pais = Pais.id_pais AND Vacuna.id_fecha = Fecha.id_fecha AND
            Test.id_pais = Pais.id_pais AND Test.id_fecha = Fecha.id_fecha AND
            Pais.nombre = 'Guatemala' AND Fecha.fecha BETWEEN TO_DATE(p_inferior, 'YYYY MM DD') AND TO_DATE(p_superior, 'YYYY MM DD');
	END;

	DECLARE
	    v_new_cases NUMBER;
	    v_total_cases NUMBER;
	    v_new_vaccinations NUMBER;
	    v_total_vaccinations NUMBER;
	    v_new_deaths NUMBER;
	    v_total_deaths NUMBER;
        v_new_tests NUMBER;
        v_total_tests NUMBER;
        v_fecha DATE;
	    v_salida    SYS_REFCURSOR;
	BEGIN
	    DBMS_OUTPUT.ENABLE;
	    DBMS_OUTPUT.PUT_LINE(
            'Fecha' || '  ' ||
            'Casos nuevos' || '  ' ||
            'Casos totales' || '  ' ||
            'Vacunas nuevas' || '  ' ||
            'Vacunas totales' || '  ' ||
            'Muertes nuevas' || '  ' ||
            'Muertes totales' || '  ' ||
            'Tests nuevos' || '  ' ||
            'Tests totales'
        );
	    DBMS_OUTPUT.PUT_LINE('-----------    -----------    -----------    -----------    -----------    -----------    -----------    -----------');
	    consulta9('2020-08-23', '2020-09-30', v_salida);
	    LOOP
	        FETCH v_salida INTO v_new_cases, v_total_cases, v_new_vaccinations, v_total_vaccinations,
                v_new_deaths, v_total_deaths, v_new_tests, v_total_tests, v_fecha; 
	        EXIT WHEN v_salida%NOTFOUND;
	        DBMS_OUTPUT.PUT_LINE(
                v_fecha || '             ' ||
	        	v_new_cases || '             ' ||
	        	v_total_cases || '             ' ||
	        	v_new_vaccinations || '             ' ||
	        	v_total_vaccinations || '             ' ||
	        	v_new_deaths || '             ' ||
	        	v_total_deaths || '             ' ||
	        	v_new_tests || '             ' ||
	        	v_total_tests
	        );
	    END LOOP;
	    CLOSE v_salida;
	END;

-- Consulta 10
	CREATE OR REPLACE PROCEDURE consulta10 (
    	p_inferior           VARCHAR2,
        p_superior           VARCHAR2,
    	p_salida    IN OUT SYS_REFCURSOR
	)
	IS
	BEGIN
	    OPEN p_salida FOR SELECT Pais.nombre AS Pais, SUM(Casos.new_cases) AS Casos
		FROM Pais, Casos, Fecha
		WHERE
			(
				Pais.nombre = 'Argentina' OR Pais.nombre = 'Bolivia' OR Pais.nombre = 'Brazil' OR Pais.nombre = 'Chile' OR
				Pais.nombre = 'Colombia' OR Pais.nombre = 'Costa Rica' OR Pais.nombre = 'Cuba' OR Pais.nombre = 'Ecuador' OR
				Pais.nombre = 'El Salvador' OR Pais.nombre = 'Guatemala' OR Pais.nombre = 'Haiti' OR Pais.nombre = 'Honduras' OR
				Pais.nombre = 'Mexico' OR Pais.nombre = 'Nicaragua' OR Pais.nombre = 'Panama' OR Pais.nombre = 'Paraguay' OR
				Pais.nombre = 'Peru' OR Pais.nombre = 'Dominican Republic' OR Pais.nombre = 'Uruguay' OR Pais.nombre = 'Venezuela' OR
				Pais.nombre = 'Guyana' OR Pais.nombre = 'Grenada' OR Pais.nombre = 'Jamaica' OR Pais.nombre = 'Suriname'
			) AND Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha AND
			Fecha.fecha BETWEEN TO_DATE(p_inferior, 'YYYY MM DD') AND TO_DATE(p_superior, 'YYYY MM DD') 
		GROUP BY Pais.nombre ORDER BY SUM(Casos.new_cases) DESC;
	END;

	DECLARE
	    v_pais VARCHAR2(256);
	    v_casos NUMBER;
	    v_salida    SYS_REFCURSOR;
	BEGIN
	    DBMS_OUTPUT.ENABLE;
	    DBMS_OUTPUT.PUT_LINE(
            'Pais' || '  ' ||
            'Casos'
        );
	    DBMS_OUTPUT.PUT_LINE('-----------    -----------');
	    consulta10('2020-03-01', '2021-03-14', v_salida);
	    LOOP
	        FETCH v_salida INTO v_pais, v_casos; 
	        EXIT WHEN v_salida%NOTFOUND;
	        DBMS_OUTPUT.PUT_LINE(
                v_pais || '             ' ||
	        	v_casos
	        );
	    END LOOP;
	    CLOSE v_salida;
	END;
```

#### MYSQL
```
-- set serveroutput on size unlimited;
-- Consulta 1
	SELECT Pais.nombre AS Pais, SUM(Casos.new_cases) AS "Actuales por Sumatoria", MAX(Casos.total_cases) AS "Actuales por Total" 
		FROM Pais, Casos, Continente
		WHERE Casos.id_pais = Pais.id_pais AND Pais.id_continente = Continente.id_continente AND Continente.nombre IS NOT NULL
		GROUP BY Pais.nombre;

-- Consulta 2
	DELIMITER //
	CREATE PROCEDURE consulta2 (IN p_pais VARCHAR)
		IS
		BEGIN
		    SELECT SUM(Casos.new_cases) AS Casos, SUM(Muertes.new_deaths) AS Muertes, SUM(Vacuna.new_vaccinations) AS Vacunas,
					MONTH(Fecha.fecha) AS M, MONTHNAME(Fecha.fecha) AS Mes, YEAR(Fecha.fecha) AS Year
				FROM Pais, Casos, Fecha, Muertes, Vacuna
				WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha AND Pais.nombre = p_pais
					AND Casos.id_pais = Muertes.id_pais AND Casos.id_fecha = Muertes.id_fecha AND Casos.id_pais = Vacuna.id_pais
					AND Casos.id_fecha = Vacuna.id_fecha
				GROUP BY MONTHNAME(Fecha.fecha), MONTH(Fecha.fecha), YEAR(Fecha.fecha)
				ORDER BY YEAR(Fecha.fecha) ASC, MONTH(Fecha.fecha);
		END //
	DELIMITER ;

-- Consulta 3
	SELECT Continente.nombre AS "Continente", SUM(Casos.new_cases) AS "Cantidad de contagios"
	    FROM Continente, Pais, Casos, Fecha, Dual
	    WHERE Casos.id_pais = Pais.id_pais AND Pais.id_continente = Continente.id_continente AND Casos.id_fecha = Fecha.id_fecha
            AND Continente.nombre IS NOT NULL
	        AND (MONTH(Fecha.fecha) - MONTH(CURRENT_DATE)) <= 3
	        AND (YEAR(Fecha.fecha) = YEAR(CURRENT_DATE))
	    GROUP BY Continente.nombre;

-- Consulta 4
	SELECT t1.Pais, ROUND((t2."Casos 1-2021" / t1."Casos 12-2020"), 2) AS "Crecimiento en %" FROM 
		(
			(
				SELECT Pais.nombre AS Pais, SUM(Casos.new_cases) AS "Casos 12-2020"
		    		FROM Pais, Fecha, Casos
		    		WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha
		    			AND MONTH(Fecha.fecha) = 12
		    			AND YEAR(Fecha.fecha) = 2020
		    		GROUP BY Pais.nombre
		    		HAVING SUM(Casos.new_cases) > 0
		    ) t1
		)
		LEFT JOIN
		(
			(
				SELECT Pais.nombre AS Pais, SUM(Casos.new_cases) AS "Casos 1-2021"
		    		FROM Pais, Fecha, Casos
		    		WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha
		    			AND MONTH(Fecha.fecha) = 1
		    			AND YEAR(Fecha.fecha) = 2021
		    		GROUP BY Pais.nombre
		    		HAVING SUM(Casos.new_cases) > 0
		    ) t2
		)
		ON t1.pais = t2.pais
		ORDER BY "Crecimiento en %" DESC;

-- Consulta 5
	SELECT Pais.nombre AS Pais, ROUND(AVG(Casos.new_cases), 2) AS Contagios
		FROM Pais, Casos, Fecha, Continente
		WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha
		    AND YEAR(Fecha.fecha) = 2020
		    AND MONTH(Fecha.fecha) BETWEEN 1 AND 3
            AND Pais.id_continente = Continente.id_continente
            AND Continente.nombre IS NOT NULL
		GROUP BY Pais.nombre;

-- Consulta 6
	DELIMITER //
	CREATE PROCEDURE consulta6 (IN p_inferior INT, p_superior INT)
	IS
	BEGIN
	    IF p_inferior < p_superior THEN
            SELECT Pais.nombre, Fecha.fecha
                FROM Casos, Pais, Fecha
                WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha
                AND Casos.new_cases BETWEEN p_inferior AND p_superior
                FETCH NEXT 600 ROWS ONLY;
        ELSIF p_superior < p_inferior THEN
            SELECT Pais.nombre, Fecha.fecha
                FROM Casos, Pais, Fecha
                WHERE Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha
                AND Casos.new_cases BETWEEN p_superior AND p_inferior
                LIMIT 600;
        END IF;
	END //
	DELIMITER ;

-- Consulta 7
	DELIMITER //
	CREATE PROCEDURE consulta7 (IN p_fecha VARCHAR)
		IS
		BEGIN
		    SELECT Pais.nombre AS Pais, SUM(Test.new_tests) AS Pruebas
	            FROM Pais, Test
	            WHERE Test.id_pais = Pais.id_pais AND Test.new_tests IS NOT NULL
	            GROUP BY Pais.nombre
	            ORDER BY SUM(Test.new_tests) DESC
	            LIMIT 10;
		END //
	DELIMITER ;

-- Consulta 8
	DELIMITER //
	CREATE PROCEDURE consulta8 (IN p_pais)
		IS
		BEGIN
		    SELECT Pais.nombre AS Pais, Muertes.new_deaths AS Muertes
	    	FROM Pais, Muertes, Fecha, Continente
	    	WHERE Muertes.id_pais = Pais.id_pais AND Muertes.id_fecha = Fecha.id_fecha
	    	    AND Fecha.fecha = STR_TO_DATE(p_fecha, '%Y-%m-%d')
	    	    AND Muertes.new_deaths IS NOT NULL
	            AND Pais.id_continente = Continente.id_continente
	            AND Continente.nombre IS NOT NULL
	    	ORDER BY Muertes.new_deaths DESC
	    	LIMIT 1;
		END //
	DELIMITER ;

-- Consulta 9
	-- Muertes, Casos, Vacunas
	DELIMITER //
	CREATE PROCEDURE consulta9 (IN p_inferior VARCHAR, INp_superior VARCHAR)
		IS
		BEGIN
		    SELECT Casos.new_cases, Casos.total_cases, Vacuna.new_vaccinations, Vacuna.total_vaccinations, Muertes.new_deaths, Muertes.total_deaths,
	            Test.new_tests, Test.total_tests, Fecha.fecha
	        FROM Casos, Muertes, Vacuna, Test, Pais, Fecha
	        WHERE 
	            Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha AND
	            Muertes.id_pais = Pais.id_pais AND Muertes.id_fecha = Fecha.id_fecha AND
	            Vacuna.id_pais = Pais.id_pais AND Vacuna.id_fecha = Fecha.id_fecha AND
	            Test.id_pais = Pais.id_pais AND Test.id_fecha = Fecha.id_fecha AND
	            Pais.nombre = 'Guatemala' AND Fecha.fecha BETWEEN STR_TO_DATE(p_inferior, '%Y-%m-%d') AND STR_TO_DATE(p_superior, '%Y-%m-%d');
		END //
	DELIMITER ;

-- Consulta 10
	DELIMITER //
	CREATE PROCEDURE consulta10 (IN p_inferior VARCHAR, INp_superior VARCHAR)
		IS
		BEGIN
		    SELECT Pais.nombre AS Pais, SUM(Casos.new_cases) AS Casos
			FROM Pais, Casos, Fecha
			WHERE
				(
					Pais.nombre = 'Argentina' OR Pais.nombre = 'Bolivia' OR Pais.nombre = 'Brazil' OR Pais.nombre = 'Chile' OR
					Pais.nombre = 'Colombia' OR Pais.nombre = 'Costa Rica' OR Pais.nombre = 'Cuba' OR Pais.nombre = 'Ecuador' OR
					Pais.nombre = 'El Salvador' OR Pais.nombre = 'Guatemala' OR Pais.nombre = 'Haiti' OR Pais.nombre = 'Honduras' OR
					Pais.nombre = 'Mexico' OR Pais.nombre = 'Nicaragua' OR Pais.nombre = 'Panama' OR Pais.nombre = 'Paraguay' OR
					Pais.nombre = 'Peru' OR Pais.nombre = 'Dominican Republic' OR Pais.nombre = 'Uruguay' OR Pais.nombre = 'Venezuela' OR
					Pais.nombre = 'Guyana' OR Pais.nombre = 'Grenada' OR Pais.nombre = 'Jamaica' OR Pais.nombre = 'Suriname'
				) AND Casos.id_pais = Pais.id_pais AND Casos.id_fecha = Fecha.id_fecha AND
				Fecha.fecha BETWEEN STR_TO_DATE(p_inferior, '%Y-%m-%d') AND STR_TO_DATE(p_superior, '%Y-%m-%d') 
			GROUP BY Pais.nombre ORDER BY SUM(Casos.new_cases) DESC;
		END //
	DELIMITER ;
```

## Reporte de los DBMS con propuesta
```
Se recomienda el uso del DBMS Oracle ya que este presenta un mejor tiempo de ejecucion, asi como un mejor manejo al momento de realizar la carga masiva de datos. Con el DBMS Mysql la carga presento problemas en la consitencia de datos.
Al momento de cargar los datos al modelo relacional, nuevamente Oracle presento un mejor tiempo en comparacion con Mysql.
Las consultas fueron mejor ejecutadas por Oracle ya que Mysql no presentaba todos los datos necesarios para obtener una respuesta correcta, tambien presento problemas en el tiempo de respuesta a dichas consultas.
Incluso hubieron unas consultas en las cuales no se pudo obtener respuesta alguna debido al prolongado tiempo de ejecucion.
```
