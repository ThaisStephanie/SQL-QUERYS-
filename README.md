-- mostrar o nome, sobrenome dos pacientes masculinos.  
/*SELECT FIRST_NAME, LAST_NAME, GENDER FROM patients
WHERE GENDER = 'M'; 



-- mostrar nome, sobrenome dos pacientes que não pussuem alergias
select first_name, last_name from patients
WHERE allergies IS null; 

-- mostrar nome dos pacientes que começam com a letra C
select first_name FROM patients
where first_name LIKE 'c%';

-- mostrar nome, sobrenome dos pacientes que pesam entre 100 e 120kg
select first_name, last_name FROM patients
WHERE weight between '100' AND '120'; 

--  alterar alergias onde o resultado for nulo
update patients SET allergies = 'NKA' where allergies is null; 

-- mostrar o nome e o sobrenome de colunas diferentes em uma só coluna
select concat(first_name, ' ', last_name) FROM patients; */

-- mostrar nome, sobrenome e province name -- 2 tabelas diferentes
/*select P.first_name, P.last_name, PN.province_name
FROM patients P 
INNER JOIN province_names PN ON P.province_id = PN.province_id
; 

-- mostrar a quantidade de pacientes que nasceram em 2010
select birth_date FROM patients; 
select count(*) AS TOTAL_PATIENTS FROM patients WHERE BIRTH_DATE LIKE '2010%'  ; 

-- mostrar primeiro nome, sobrenome e altura do paciente mais alto. 
select MAX(height) from patients; 
select first_name, last_name, MAX(height) from patients; 


-- mostrar todos os dados dos pacientes que tiverem os seguintes id's 1, 45, 
--534, 879,1000
select * from patients where patient_id in(1,45,534,879,1000); 

-- mostrar a quantidade de admissões
select count(*) as records from admissions; 

-- mostrar todos os dados de admissões onde o paciente deu entrada e saida no mesmo dia

select * from admissions where admission_date = discharge_date; 

-- mostrar o id do paciente e quantidade de registros com o id 579

select patient_id,   count(*) as records  from admissions where patient_id = '579'; 
; 

-- mostrar as cidades que ñ se repetem com o UF 'ns' 
select distinct city from patients
where province_id = 'NS'; 

-- mostrar o nome e sobrenome dos pacientes que tem uma determinada altura e peso
select first_name, last_name, birth_date from patients 
where height > 160 AND weight > 70; 

-- mostrar o nome, sobrenome e alergia dos pacientes que moram em hamilton e possuem 
-- alergia
select first_name, last_name, allergies from patients
where city = 'Hamilton' AND allergies is not null;  

-- mostrar as cidades únicas que começam com as vogais, e ordená-las de forma crescente.
select distinct city
from patients
where city LIKE 'A%'
or city LIKE 'E%' 
or city LIKE 'I%' 
or city LIKE 'O%' 
or city LIKE 'U%' 
order by city ASC; */
