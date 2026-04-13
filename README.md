# Taller-Pr-ctico-01-Ingenier-a-Inversa-con-XQuery-y-BaseX

## *RETO 1:* El Filtro de Selección

for $libro in //libro[@categoria = "programacion"]
let $valor := $libro/precio
where number($valor) > 30.00
order by $libro/libro[@titulo] ascending
return <resultado>Titulo: {data($libro/titulo)}- Precio: {data($valor)}€ </resultado>
