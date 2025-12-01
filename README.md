# Webscraping dados Futebol ⚽
## Webscraping de dados de resultados e e estatísticas dos jogos do Campeonato Brasileiro Série A 2025.

### Ferramentas:
#### Plataforma:
- Jupyter Notebook
#### Linguagem:
- Python
#### Bibliotecas:
- Selenium: utilizado para navegar pelo website e capturar os dados (scraping).
- Pandas: utilizado para armazenar e estruturar os dados.

</br>


## Básico de Selenium
#### Importar:
```
from selenium import webdriver
```
#### Inicializar
```
driver = webdriver.Chrome()
driver.get("https://www.https://www.placardefutebol.com.br/")
```
#### Capturar elementos
```
links_jogos = driver.find_elements(By.CLASS_NAME, "ergebnis-link")
```
#### Espera explícita (ou espera dinâmica) do Selenium
>   É importante que essa estratégia seja implementada para lidar com a assincronicidade do carregamento dos elementos de uma página web, ou seja, se nosso script tenta capturar ou clicar em um elemento antes que ele seja carregado ou seja clicável por exemplo, um erro será lançado.</br>
>   Então é importante aguardar o carregamento de um elemento antes de realizarmos uma ação com esse mesmo elemento.
```
wait = WebDriverWait(driver, 7)
wait.until(EC.element_to_be_clickable((By.CLASS_NAME, "ergebnis-link")))
```
#### Clicar em um elemento
```
links_jogos[0].click()
```