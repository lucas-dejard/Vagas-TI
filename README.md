# Vagas-TI
Escopo e subprodutos de teste para o site: https://eureka-testers.onrender.com/#/login

Para esse projeto o Documento que traz a abordagem completa utilizada é o: [Plano de teste do projeto!] e pode ser beixado para melhor vizualização.
Este documento traz como aspectos mais importantes as seguintes abordagens sobre o site:


* Casos de teste. 
* Ferramentas de teste. 
* Modelos de teste. 
* Resultados de teste. 
* Subprodutos de teste. 
* Cobertura de teste. 
* Observações de teste. 

## Casos de teste

* Login/Registro
* Consulta de Vagas
* Filtros
* Alerta de vagas

## Ferramentas

Para esse projeto os testes foram realizados em uma máquina local Linux Ubuntu 22.04.1 LTS com acesso à internet, utilizado o navegador firefox 109.0 (64-bits), com o plugin Screen Recorder 1.0.6 e a ferramenta de captura de interações Katalon Recorder 5.5.3.

## Modelos

Não vou colocar todos os modelos aqui pois eles são muitos e podem ser vistos no [Plano de teste do projeto!]
Porém, seguem alguns dos exemplos realizados:


| Númeração | Cenário | Localização | Pré-condição | Procedimento | Resultado esperado:
| ------------- |:-------------:| -----:| ------------- |:-------------:| -----:|
| 1 | Criar Conta | Tela de login > Pop up de Criar Conta | Nome, e-mail, senha e confirmação de senha válidos | Preencher: - nome - e-mail - senha - confirmação de senha|Usuário criado com sucesso!. |
|2  | Criar conta duplicada inválido| Tela de login > Pop up de Criar Conta | Nome, e-mail, senha e confirmação de senha pré-cadastrados. | Preencher: - nome- e-mail - senha - confirmação de senha | Falha no cadastro. |
|3 | Criar conta, senha  inválida | Tela de login > Pop up de Criar Conta | Nome, e-mail e confirmação de senha válidos. Senha inválida. | Preencher: - nome - e-mail - senha - confirmação de senha | Indicar o erro do usuário(senha inválida) e não cadastrar. |
|4 | Criar conta, nome inválido | Tela de login > Pop up de Criar Conta | e-mail, senha e confirmação de senha válidos. Nome inválido. | Preencher: - nome - e-mail - senha - confirmação de senha | Indicar o erro do usuário(nome inválido) e não cadastrar. |
|5 | Criar conta, e-mail inválido | Tela de login > Pop up de Criar Conta | Nome, senha e confirmação de senha válidos, E-mail inválido. | Preencher: - nome - e-mail - senha - confirmação de senha | Indicar o erro do usuário(e-mail inválido) e não cadastrar. |


## Resultados

Não vou colocar todos os resultados aqui pois eles são muitos e podem ser vistos no [Plano de teste do projeto!]
Porém, seguem alguns dos exemplos obtidos:


|Númeração|Resultado <br/> Esperado\|Obtido|  Sucesso  |Considerações|
| ------------- |:----------------:|:--------:| ------------- |
|6|Indicar o erro do usuário(confirmação de senha inválido) e não cadastrar. <br/> \| <br/> Ele não confirma que a senha escolhida são iguais nos dois campos de senha.|Falha ❌|Confirmação de senha com caracteres a mais do que o possível na senha
|7|Login na página de consulta! <br/> \| <br/> Login na página de consulta! | Sucesso ✅|
|8|Indicar o erro do usuário(senha inválida) e não logar. <br/> \| <br/> Indica o erro(senha inválida) e não faz o login |Sucesso ✅|
|9| Indicar o erro do usuário(e-mail inválido) e não logar. <br/> \| <br/> Indica o erro(e-mail inválido) e não faz o login|Sucesso ✅|
|10| Listar vagas(por padrão o “não remoto” é selecionado). <br/> \| <br/> Listar vagas(por padrão o “não remoto” é selecionado).|Sucesso ✅ |O não remoto poderia ser opcional e não por padrão

## Subprodutos
Os subprodutos tais como: scripts, imagens e vídeos resultados dos testes executados estão disponíveis neste repositório em suas respectivas pastas.
#### Imagens e vídeos relacionados aos casos de teste descritos neste documento possuem a numeração relacionada!


### Algumas gravações dos testes Manuais realizados:
[02 - Criando conta duplicada.webm](https://user-images.githubusercontent.com/34687381/214885975-32e7e618-dc83-4f35-9f9f-b03b92412908.webm)

[06 - Confirmação senha.webm](https://user-images.githubusercontent.com/34687381/214886017-63099083-fbf8-4f3d-a634-61fd4cdc72a1.webm)

![Captura de tela de 2023-01-12 23-30-11](https://user-images.githubusercontent.com/34687381/214886224-f6273a2b-f0bf-470c-934e-620e7751989c.png)

![Captura de tela de 2023-01-10 20-56-33](https://user-images.githubusercontent.com/34687381/214886313-8de6804b-619d-4398-a531-29f4765d0e17.png)

## Cobertura

O nível de cobertura de testes é medido pela “%” porcentagem dos casos de teste executados com sucesso.

|Aceitação Completa |Acima de 95% dos casos de teste executados com sucesso!|O programa está pronto para o deploy!|
| ------------- |:----------------:|:--------:|
|Meio nível de aceitação|De 70 até 95% dos casos executados com sucesso|O programa pode ser liberado para o PO como um protótipo.|
|Inaceitável|Até 70% de casos executados com sucesso.|Qualidade insuficiente.|

##### O projeto atual se encontra com 65% dos seus testes executados com sucesso, o que o coloca em inaceitável!

## Observações

Login/registro:
A confirmação de senha possui o campo para 10 caracteres, porém só é possível senhas até 8.
![image](https://user-images.githubusercontent.com/34687381/214888268-6372d25f-6540-4144-a1ac-137dfcc60b28.png)


Listar vagas:
No momento é apenas possível escolher entre “Remoto sim” e “Remoto não” acredito que poderia ter a opção de listar ambas!
![image](https://user-images.githubusercontent.com/34687381/214888447-9c43e150-d197-4eb1-b058-834e2a04996c.png)

Entre Outras Observações recomendo baixar e ler o [Plano de teste do projeto!]


<br/> 

[//]: <> (Links)

[Plano de teste do projeto!]: https://github.com/lucas-dejard/Vagas-TI/blob/main/Escopo%20-%20Vagas%20TI!.docx
