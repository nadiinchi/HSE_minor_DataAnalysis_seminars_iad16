### Данные для проекта по предсказанию зарплаты

##### Ссылка на архив с csv-файлом: [https://goo.gl/lOETvg](https://goo.gl/lOETvg)

##### Ссылка на дополнительную информацию (дерево локаций):  [https://goo.gl/sklLD7](https://goo.gl/sklLD7)

##### Описание полей:
* LocationRaw - The freetext location as provided by the job advertiser.

* LocationNormalized - Adzuna's normalised location from within our own location tree, interpreted by us based on the raw location. 
Our normaliser is not perfect!

* ContractType - full_time or part_time, interpreted by Adzuna from description or a specific additional field we received from the advertiser.

* ContractTime - permanent or contract, interpreted by Adzuna from description or a specific additional field we received from the advertiser.

* Company - the name of the employer as supplied to us by the job advertiser.

* Category - which of 30 standard job categories this ad fits into, inferred in a very messy way based on the source the ad came from.  
We know there is a lot of noise and error in this field.

* SalaryRaw - the freetext salary field we received in the job advert from the advertiser.

* SalaryNormalised - the annualised salary interpreted by Adzuna from the raw salary.  Note that this is always a single value based on the midpoint of any range found in the raw salary.  This is the value we are trying to predict.

* SourceName - the name of the website or advertiser from whom we received the job advert.

В __тестовой выборке__ (будет доступна уже на kaggle в следующем модуле) не будет полей SalaryNormalized и SalaryRaw.

__Целевой признак__: SalaryNormalized (т. е. его мы предсказываем).

В __дополнительном файле__ дано дерево локаций; с его помощью вы можете делать разные признаки (район, регион, город вакансии).
