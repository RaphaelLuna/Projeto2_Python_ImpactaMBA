### PROJETO 02 
#### COMPLETANDO O PROJETO, CRIADO AS FUNÇÕES  keys_check (utils.py) E feat_eng (app.py)

# ORGANIZAÇÃO
 - db-pipeline
   - assets (create_table.py - utils.py - work_metadado_flights.xlsx) contém os arquivos necessarios para app.py funcionar
   - data (nycflights.csv - NyflightsDB.db) contém o arquivo csv de voo que será utilizado para alimentar um banco de dados 
 - .env ( arquivo para variavés de ambiente)
 - app.py (arquivo principal no qual contém as funcões necessarias para ingestão do banco de daos e apresentação do plano de voo)
 
### Como utilizar:

1. Crie um ambiente virtual
```
python -m venv env
```
2. Ative o ambiente virtual
3. Instale o requirements (se necessário)
```
pip install -r requirements.txt
```
4. Execute o script passando a mensagem em morse
```
py /db-pipeline/app.py
```

----

#### INFORMAÇÕES PARA IMPLEMENTAÇÃO

## 1.Complete os projeto criando as funções:

# Função de validação de chaves - keys_check (utils.py)
 - Input da função: colunas chave
 - Lógica: df[[cols_chave]] == len(df) 
 - Output da função: Log/warning dizendo que os campos declarados como chave, não são chave
 - Hint: Não é necessário fazer bater, ou seja, não é obrigatório retornar a condicional retornar True, concentrem-se na lógica.


# Função para a criação de novos campos / Engenharia de Features - feat_eng (app.py)
 - tempo_voo_esperado -> datetime_chegada - datetime_partida
 - dia_semana -> [data do voo]dt.day_of_week hint: tem que ser do tipo datetime para funcionar
 - horario -> classificar em manhã, tarde, noite e madrugada
 - tempo_voo_hr -> tempo de voo que está em minutos, mas em horas
 - atraso -> tempo_voo_hr  - tempo_voo_esperado 
 - flg_status -> classificar quanto tempo de atraso é "ATRASO" e os demais casos "ON-TIME"

## A lógica da implementação foi realizada em aula e está disponível no notebook em anexo

2.No main inclua a execução de todas as etapas do processo (funções desenvolvidas)
3.Inclua um logger para cada step do processo.
4.Documente as funções desenvolvidas utilizando docstrings.
5.Inclua um arquivo readme no projeto descrevendo o objetivo dele e a organização dos arquivos nas pastas
6.Inclua um arquivo de requirements.txt
7.Siga a mesma estrutura de projeto que está no git da disciplina (link acima)
