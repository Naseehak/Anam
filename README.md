set serveroutput on
declare
n number;
factorial number;
function fact(x number)
return number
is 
begin 
if x=1 then
return 1;
else 
return x*fact(x-1);
end if;
end;
begin
n:=&n;
factorial:=fact;
dbms_output.put_line('factorial'||'n'||'is'||factorial);
end;
/
