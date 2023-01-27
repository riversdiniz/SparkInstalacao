# 🚀 Utilizando o Spark no Windows
[fonte](https://spark.apache.org/docs/3.1.2/api/python/getting_started/install.html)

### 📋 Pré-requisitos
#### Passo 1 - Instalando o Java
O PySpark requer a instalação do Java na versão 7 ou superior. Obtenha a versão mais recente clicando [aqui](https://www.java.com/pt-BR/download/). Para verificar a versão que está instalada em sua máquina execute a seguinte linha de código no seu prompt:
```
java -version
```
### Passo 2 - Instalando o Python
O Python deve ser instalado em sua versão 2.6 ou superior. Para obter a versão mais recente clique [aqui](https://www.python.org/downloads/windows/). Para verificar a versão do Python que está instalada em sua máquina digite o seguinte comando em seu prompt:
```
python --version
```
#### Passo 3 - Instalando o Apache Spark
Selecione a versão mais estável clicando [aqui](http://spark.apache.org/downloads.html). Na criação deste projeto utilizamos a versão do Spark 3.1.2 e como tipo de pacote selecionamos Pre-built for Apache Hadoop 2.7.

Para instalar o Apache Spark não é necessário executar um instalador, basta descomprimir os arquivos em uma pasta de sua escolha.

`
Obs.: certifique-se de que o caminho onde os arquivos do Spark foram armazenados não contenham espaços (ex.: "C:\spark\spark-3.1.2-bin-hadoop2.7").
`

Para testar o funcionamento do Spark execute os comandos abaixo em seu prompt de comando. Esses comandos assumem que você extraiu os arquivos do Spark na pasta "C:\spark".

cd C:\spark\spark-3.1.2-bin-hadoop2.7
bin\pyspark
O comando acima inicia o shell do PySpark que permite trabalhar interativamente com o Spark.

Para sair basta digitar exit() e logo depois presionar Enter. Para voltar ao prompt pressione Enter novamente.

#### Passo 4 - Instalando o findspark
```
pip install findspark
```
#### Passo 5 - Instalando o winutils
Os arquivos do Spark não incluem o utilitário winutils.exe que é utilizado pelo Spark no Windows. Se não informar onde o Spark deve procurar este utilitário, veremos alguns erros no console e também não conseguiremos executar scripts Python utilizando o utilitário spark-submit.

Faça o [download](https://github.com/steveloughran/winutils) para a versão do Hadoop para a qual sua instalação do Spark foi construída. Em nosso exemplo foi utilizada a [versão 2.7](https://github.com/steveloughran/winutils/tree/master/hadoop-2.7.1/bin). Faça o download apenas do arquivo winutils.exe.

Crie a pasta "hadoop\bin" dentro da pasta que contém os arquivos do Spark (em nosso exemplo "C:\spark\spark-3.1.2-bin-hadoop2.7") e copie o arquivo winutils.exe para dentro desta pasta.

Crie duas variáveis de ambiente no seu Windows. A primeira chamada SPARK_HOME que aponta para a pasta onde os arquivos Spark foram armazenados (em nosso exemplo "C:\spark\spark-3.1.2-bin-hadoop2.7"). A segunda chamada HADOOP_HOME que aponta para %SPARK_HOME%\hadoop (assim podemos modificar SPARK_HOME sem precisar alterar HADOOP_HOME).

## 🛠️ Projeto
Nosso projeto consiste em ler, manipular, tratar e salvar um conjunto de dados volumosos utilizando como ferramenta o Spark.

Carregamento de dados

Dados Públicos CNPJ

Receita Federal
* [Empresas](https://caelum-online-public.s3.amazonaws.com/2273-introducao-spark/01/empresas.zip)
* [Estabelecimentos](https://caelum-online-public.s3.amazonaws.com/2273-introducao-spark/01/estabelecimentos.zip)
* [Sócios](https://caelum-online-public.s3.amazonaws.com/2273-introducao-spark/01/socios.zip)

[Fonte original dos dados](https://www.gov.br/receitafederal/pt-br/assuntos/orientacao-tributaria/cadastros/consultas/dados-publicos-cnpj)

⌨️ 🚀 por [River Diniz](https://gist.github.com/riversdiniz) 🧑‍🚀
