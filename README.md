[![LinkedIn](https://img.shields.io/badge/LinkedIn-CristinaOliveira-254a7f.svg)](https://www.linkedin.com/in/engcrisoliveira) [![LinkedIn](https://img.shields.io/badge/LinkedIn-RodrigoXavier-1c6388.svg)](https://www.linkedin.com/in/rodrigo-xavier-077372a8/) [![LinkedIn](https://img.shields.io/badge/LinkedIn-RogerioAlves-277a8b.svg)](https://www.linkedin.com/in/rog%C3%A9rio-alves-17797320a) [![LinkedIn](https://img.shields.io/badge/LinkedIn-VyctorManoel-3f908e.svg)](https://www.linkedin.com/in/vyctor-manoel-b41a141a4/)

[![](https://img.shields.io/badge/Python-7cb995.svg)](https://www.python.org/downloads/release/python-365/) [![](https://img.shields.io/badge/NumPy-7cb995.svg)](https://numpy.org/) [![](https://img.shields.io/badge/scikitlearn-7cb995.svg)](https://scikit-learn.org/stable/) [![](https://img.shields.io/badge/seaborn-7cb995.svg)](https://seaborn.pydata.org/) [![](https://img.shields.io/badge/Matplotlib-7cb995.svg)](https://matplotlib.org/) 

### Alunos com deficiência X Acessibilidade das IES

Apesar da existência de legislações que facilitam o acesso ao mercado de trabalho, assim como normas técnicas de acessibilidades às edificações, o desafio da inclusão de pessoas com deficiência (PcD) na sociedade ainda é grande. O acesso ao ensino superior, nesse sentido, engloba não apenas o ingresso como também a garantia de sua permanência, assim como condições para a conclusão dos cursos. Um conjunto que ainda enfrenta diversas barreiras, o que pode ser observado pela pouca representatividade de pessoas com deficiência no ensino superior.

Assim, este estudo procurou compreender através de técnicas de aprendizagem de máquina a relação da quantidade e distribuição de pessoas com deficiência no ensino superior, assim como as condições de acessibilidade disponibilizadas pelas Instituições de Ensino Superior. Foram aplicados modelos de regressão linear simples, para previsão de dados, de clustering, com a utilização dos algoritmos de k-means, DBSCAN e mean shift, para que se possa verificar similaridades nas características dos cursos onde há uma maior presenças de pessoas com deficiência, e de classificação, com o intuito de buscar as maiores relevâncias na acessibilidade e presença dessa parcela de alunos.

#### Objetivo

Utilizar conceitos de estatísticas, além de ferramentas e modelos de aprendizagem de máquina como regressão, classificação (árvores de decisão, KNN e SVM) e clustering (k-means, o DBSCAN e o Mean Shift) para ajudar nas análises dos dados do Censo do Ensino Superior.

### Resultados

Análise Exploratória de Dados

![A](https://user-images.githubusercontent.com/42254248/160938391-8937ef1b-dd22-445b-8672-8f8ce2d9f791.png)

![B](https://user-images.githubusercontent.com/42254248/160938406-2ef6673f-f2cf-49fb-80fa-b2cc538aaa19.png)

Na Análise Exploratória dos Dados, ao analisar a forma de ingresso, podemos perceber que a maioria dos alunos com deficiência matriculados no ensino superior, 63747, ou seja, 95,41% ingressam nos cursos por meio de cotas reservadas a pessoas com deficiência. Apenas 4,59% ingressam sem ser por cotas reservadas, o que pode indicar que o ingresso dos mesmos pode ter uma maior relação com políticas públicas.

![6](https://user-images.githubusercontent.com/42254248/160938915-369b1358-2038-487c-b3c7-47faeac7bc46.png)

1. Quantos alunos com deficiência teremos em 2030 no ensino superior?

![13](https://user-images.githubusercontent.com/42254248/160938687-b085be8c-145f-4f87-961a-0fd45fd3c990.png)

A resposta é aproximadamente 108771 alunos, ou seja, um aumento de 62.95% em relação ao ano de 2019, desse modo apesar de não podermos concluir o motivo do aumento, concluímos que existe um aumento da quantidade de alunos com deficiência no ensino superior do Brasil.

No resultado do Modelo de Regressão, não conseguimos afirmar se o crescimento do número de alunos com deficiência pode ser apenas pelo crescimento de alunos total ou políticas públicas de acessibilidades como por exemplo as cotas, além de que o problema do dataset de não fornecer informações precisas sobre os recursos existentes nos cursos, limitou nossa análise e por isso não conseguimos determinar que as ies que contém mais recursos de acessibilidades são aquelas que contém mais alunos com deficiência; 

2. Quais são as similaridades entre IES quanto à acessibilidade para pessoas com deficiência?

A fim de responder a questão sobre quais são as similaridades entre IES quanto à acessibilidade para pessoas com deficiência, foram realizados agrupamentos de acordo com as similaridades entre as IES, utilizando os seguintes parâmetros de entrada:

- Quantidade de alunos com deficiência no ensino superior;
- Diversidade de recursos de acessibilidade disponíveis na IES;
- Números de cursos ofertados pela IES (porte da IES);
- Receitas disponíveis para IES;
- Despesas realizadas com investimentos pelas IES; e
- Conceito médio da graduação (IGC).

Para complementar o pré-processamento dos dados e podermos usar nos algoritmos de clustering, foi feito o tratamento de outliers, normalização dos dados e uma análise de correlação dos atributos.

![c](https://user-images.githubusercontent.com/42254248/160938732-51fd6d4e-8a23-4569-9de1-151ff8eab993.png)

A partir do resultado do coeficiente de silhueta, usamos 3 como a quantidade de clusters ideal para nosso conjunto de dados. E Para termos uma melhor visualização dos nossos dados, foi feito ainda uma análise da densidade das features, por meio do kde plot (kernel density estimation plot), para visualização de uma estimativa da frequência relativa dos valores, ou seja, uma estimativa da função densidade de probabilidade da feature, em termos probabilísticos

![kA](https://user-images.githubusercontent.com/42254248/160938761-28a4abd6-0081-4909-8a35-83a4ce8b4383.png)

![kB](https://user-images.githubusercontent.com/42254248/160938778-1f9e49e7-dc48-40d7-b19d-35495f4eee83.png)

Foram realizados agrupamentos de acordo com as similaridades entre as IES, tendo como resultados os clusteres a seguir:

![clusterA](https://user-images.githubusercontent.com/42254248/160938824-d6a5e939-5df9-4fd0-8369-9d4c2cce97d3.png)

![clusterB](https://user-images.githubusercontent.com/42254248/160938838-f6d1f6ac-49ec-4b43-a557-fcf81ac1cad3.png)

As IES foram agrupadas conforme tabela abaixo:

ID  | Quantidade de IES | Alunos com deficiência | Média de Recurso | Receitas média (R$) | Despesa média com investimentos (R$) | Conceito médio da graduação | IES (%) | Alunos com deficiência (%)
-- | --- | ------- | -------- | ------------ | ------------ | -------- | --------- | ---------
0  | 175 | 15540.0 | 4.989344 | 4.855213e+08 | 1.353602e+07 |	2.782871 | 13.725490 | 35.050523
1  | 483 | 16607.0 | 9.558355 | 1.486772e+08 | 1.409380e+06 |	2.674184 | 37.882353 | 37.457145
2  | 617 | 12189.0 | 3.129444 | 7.977919e+07 | 7.958378e+05 |	2.533084 | 48.392157 | 27.492331

#### Impedimentos/ Dificuldades
- Pequena série temporal dos dados (registros de alunos com deficiência e recursos de acessibilidade apenas de 2011 a 2019);
- Há poucas informações relacionadas aos recursos de acessibilidade disponíveis, havendo apenas a informação se o curso possuía ou não determinado recurso e não com a quantidade de recursos que os cursos possuíam;
- Uma de nossas dificuldade foi analisar a questão sobre se há mais alunos com deficiência em estado/ região que possuem mais pessoas com deficiência, pois não havia dados de pessoas com deficiência para o ano de 2019, por estados (IBGE), apenas os dados do censo anterior, de 2010. Não conseguimos fazer uma projeção desses dados, porque as projeções da população para o Brasil e as Unidades da Federação são prospectivas, estimadas por métodos demográficos, que não podem ser os mesmos a serem utilizados para estimativa da população com deficiência por terem comportamentos diferentes;
- Ao analisar os tipos de deficiências e os recursos de acessibilidade associados às suas respectivas necessidades, não conseguimos observar nenhuma correlação entre eles nem conseguimos extrair algum comportamento entre essas variáveis;
- Outro ponto observado com os dados presentes no Censo, é a ausência de recursos de acessibilidade necessários ou específicos para alunos com deficiência cognitiva, em contrapartida das que existem para outros tipos de deficiência, como auditiva e visual;
- A ausência da informação relacionada à quantidade e à qualidade dos recursos de acessibilidade disponíveis, assim como ausência de dados referentes ao preparo e capacidade dos funcionários das IES em trabalhar no apoio a pessoas com deficiência dentro das IES limitam que uma análise mais aprofundada possa ser feita; e
- Para futuros trabalhos, a sugestão é que seja feita uma análise tanto quantitativa como qualitativa com dados primários que consigam extrair mais informações sobre o acesso (ingresso, permanência e conclusão) da pessoa com deficiência no ensino superior, sobre a quantidade e qualidade dos recursos de acessibilidade existentes e sobre o preparo dos funcionários da IES no apoio aos alunos com deficiência, num recorte de espaço, como uma universidade específica, por exemplo. Ou analisar essa questão, sob o ponto de vista de políticas públicas em um estado/região específicos.

#### Trabalhos Correlatos
- [Ingresso e permanência de alunos com deficiência em universidades públicas brasileiras](https://repositorio.ufsc.br/handle/123456789/187845)
- [Inclusão de estudantes com deficiência no ensino superior: uma revisão sistemática](https://periodicos.ufsm.br/educacaoespecial/article/view/19898)
- [Os encontros de serviço de deficientes visuais em instituições de ensino superior](https://periodicos.uff.br/pca/article/view/11258)
- [Deficientes auditivos e escolaridade: fatores diferenciais que possibilitam o acesso ao ensino superior](https://www.scielo.br/j/rbee/a/B3q6wWMmr7dHVznxf53LdZv/abstract/?lang=pt)
- [Sujeitos com deficiência no ensino superior: vozes e significados](https://repositorio.ufsc.br/handle/123456789/188487)
- [A inclusão do surdo no ensino superior no Brasil](https://nasenjournals.onlinelibrary.wiley.com/doi/full/10.1111/1471-3802.12128)
- [Políticas públicas para acesso de pessoas com deficiência ao ensino superior brasileiro: uma análise de indicadores educacionais](https://www.scielo.br/j/ensaio/a/kthK5F8TxS7Q49BpLnJLFvp/abstract/?lang=pt)
- [Estudantes com deficiência no ensino superior: trajetórias escolares, acesso e acessibilidade](http://revista.ibict.br/inclusao/article/view/4083)
