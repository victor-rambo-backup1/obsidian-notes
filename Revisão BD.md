
create table conta (cod number(5), saldo number(7,2)); alter table conta add check(cod is not null); alter table conta add check(saldo is not null and saldo>=0); alter table conta add constraint conta_pk primary key(cod);

drop table
drop index
drop view
alter table drop constraint

Update departamento Set ramal = ‘1234 where nome = ‘RH’;


CASCADE
SET NULL
SET DEFAULT

turmas_pkey
turmas_codd_fkey