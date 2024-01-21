# Projeto SQL EBAC

[link_projeto_SQL]([https://www.kaggle.com/code/carolrmr/notebookac619d0e07]

Os .csvs são os resultados da exploração e analise de dados de crédito com SQL

Query1: SELECT DISTINCT estado_civil FROM credito

Query2: SELECT DISTINCT salario_anual FROM credito

Query3: select count(*), salario_anual from credito group by salario_anual

Query4: select count(*), sexo from credito group by sexo

Query5: select max(limite_credito) as limite_credito, escolaridade, tipo_cartao, sexo from credito where escolaridade != 'na' and tipo_cartao != 'na' group by escolaridade, tipo_cartao, sexo order by limite_credito desc limit 10

Query6: select max(limite_credito) as limite_credito, escolaridade, tipo_cartao, sexo from credito where escolaridade != 'na' and tipo_cartao != 'na' group by escolaridade, tipo_cartao, sexo order by limite_credito asc

Query7: select min(valor_transacoes_12m) as transacao_minima, max(valor_transacoes_12m) as transacao_minima from credito

Query8: select avg(qtd_produtos) as qts_produtos, avg(valor_transacoes_12m) as media_valor_transacoes, avg(limite_credito) as media_limite, sexo, salario_anual from credito where salario_anual != 'na' group by sexo, salario_anual order by avg(valor_transacoes_12m) desc

Query9: SELECT sexo, idade, AVG(limite_credito) as media_credito FROM credito GROUP BY sexo, idade limit 10;

Query10: SELECT salario_anual, idade, AVG(limite_credito) as media_credito FROM credito GROUP BY salario_anual, idade limit 10;


Essas foram algumas análises extraídas do dataset de crédito:

-A maior parte dos clientes possui renda até 40K

-O sexo influencia no limite do cartão

-Os clientes com maiores limites são em sua maioria homens

-Os clientes com menores limites são em sua maioria mulheres

-A faixa salarial impacta diretamente no limite de crédito
