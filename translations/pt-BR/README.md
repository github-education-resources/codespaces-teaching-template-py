
[![Abrir no GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=526669888)

# Ensine Python no Codespace

_Crie ou estenda um repositório pronto para uso para ensinar Python em minutos_

* **Para quem é?** _Educadores de todos os níveis_.
* **Quanta experiência os alunos precisam?** _Zero_. Este modelo é construído com elementos básicos completos com comentários para que possa ser usado em aulas de iniciante ao avançado.
* **Pré-requisitos:** _Nenhum_. Este modelo fornecerá um Jupyter Notebook funcional com Pandas usando um conjunto de dados para que você possa começar a analisar dados imediatamente, bem como um Notebook de exemplo que você pode usar para ensinar Python com [GitHub Copilot](https://copilot.github.com) , uma poderosa ferramenta de IA que ajuda você a escrever código mais rapidamente.


Com este repositório de modelos, você pode criar rapidamente um ambiente normalizado para ensinar ou aprender Python. Faça com que seus alunos se concentrem no aprendizado, em vez de configurar o ambiente. Este modelo usa Codespaces, um ambiente de desenvolvimento hospedado na nuvem com [Visual Studio Code](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza), um poderoso editor de texto.

Você também terá a chance de experimentar o Copilot para criar um plano de aula usando o arquivo [exemplo-licao.ipynb](./exemplo-licao.ipynb).

🤔 Curioso? Veja o seguinte vídeo onde explicamos todos os detalhes:

[![Ensinando Python com Codespaces](../../images/video-banner.gif)](https://youtu.be/7rMvb03hHpI "Ensinando Python com Codespaces")

<details>
   <summary><b>🎥 Assista ao tutorial em vídeo para saber mais sobre Codespaces </b></summary>
   
   [![Tutorial de Codespaces](https://img.youtube.com/vi/ozuDPmcC1io/0.jpg)](https://aka.ms/CodespacesVideoTutorial "Tutorial de Codespaces")
</details>

🚀 Recursos do Codespaces:

- Ambiente de nuvem repetível que oferece uma experiência de apertar botão.
- Pode ser configurado e personalizado.
- Integra-se com seus repositórios no GitHub e [VSCode](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza)

Como professor, isso significa que você pode criar um ambiente, na nuvem, para sua turma que todos os alunos possam usar com configuração zero ou quase zero, independentemente do sistema operacional que estejam usando.

## 🧑‍🏫 O que é GitHub Codespace e como posso usá-lo em minhas aulas?

Um Codespace é um ambiente de desenvolvimento hospedado na nuvem que você pode configurar. O benefício Codespaces Education oferece aos professores do Global Campus um subsídio mensal gratuito de horas de GitHub Codespaces para usar no [GitHub Classroom](https://classroom.github.com). Saiba mais [aqui](https://docs.github.com/pt/education/manage-coursework-with-github-classroom/integrate-github-classroom-with-an-ide/using-github-codespaces-with-github-classroom) sobre o uso de codespaces do GitHub com o GitHub Classroom.

Se você ainda não é professor do Global Campus, inscreva-se [aqui](https://education.github.com/discount_requests/pack_application) ou, para obter mais informações, consulte [Inscreva-se no GitHub Global Campus como professor](https://docs.github.com/pt/education/explore-the-benefits-of-teaching-and-learning-with-github-education/github-global-campus-for-teachers/apply-to-github-global-campus-as-a-teacher).

## Costumização

Personalize seu projeto para GitHub Codespaces alterando os arquivos de configuração em seu repositório (geralmente conhecido como Configuração-como-Código), que cria uma configuração de codespace repetível para todos os usuários de seu projeto.

Você pode configurar coisas como:

- Extensões, você pode especificar quais extensões devem ser pré-instaladas.
- Dotfiles e configurações.
- Bibliotecas e dependências do sistema operacional

> 💡 Saiba mais sobre [customização e configuração na documentação oficial](https://docs.github.com/pt/codespaces/customizing-your-codespace/personalizing-github-codespaces-for-your-account)


## Modelo do Codespace

Este repositório é um modelo do GitHub. Ele contém o seguinte:

- [examplo-notebook.ipynb](./examplo-notebook.ipynb): um notebook Jupyter usando a biblioteca [Pandas](https://pandas.pydata.org/) para ensinar operações básicas com um pequeno arquivo CSV (separado por vírgula Arquivo de valor) [dataset](../../wine-regions.csv)
- [.devcontainer/Dockerfile](./.devcontainer/Dockerfile): Arquivo de configuração usado pelo Codespaces para determinar o sistema operacional e outros detalhes.
- [.devcontainer/devcontainer.json](./.devcontainer/devcontainer.json), Um arquivo de configuração usado por Codespaces para configurar [Visual Studio Code](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza), como a ativação de extensões adicionais.
- `README.md`. Este arquivo descreve este repositório e o que há nele.

## 🧐 Experimente

Experimente este repositório de modelos usando Codespaces seguindo estas etapas:

1. Crie um repositório a partir deste modelo. Use este [link de criação de repositório](https://github.com/microsoft/codespaces-teaching-template-py/generate). Você pode tornar o repositório privado ou público, você que decide.
1. Navegue até a página principal do repositório recém-criado.
1. Sob o nome do repositório, use o menu suspenso Código e, na guia Codespaces, selecione "Criar Codespace na main".
    ![Criar o Codespace](https://docs.github.com/assets/cb-138303/images/help/codespaces/new-codespace-button.png)
1. Aguarde enquanto o Github inicializa o Codespace:
    ![Criando o Codespace](../../images/Codespace_build.png)


### Inspecione seu ambiente do Codespaces

O que você tem neste ponto é um ambiente pré-configurado onde todas as configurações e bibliotecas que você precisa já estão instalados - uma experiência de configuração zero.

Você também tem um Jupyter Notebook que pode começar a usar sem nenhuma configuração.

> Este ambiente será executado da mesma forma, independentemente de seus alunos estarem no Windows, macOS ou Linux.

Abra seu arquivo Jupyter Notebook [examplo-notebook.ipynb](./examplo-notebook.ipynb) e observe como você pode adicionar código e executá-lo.

## Personalize o Codespace

Vamos fazer alterações em seu ambiente. Abordaremos dois desafios diferentes que você provavelmente deseja fazer:

1. Altere a versão do Python instalada
1. Adicione uma extensão


### Etapa 1: alterar o ambiente Python

Digamos que você queira alterar qual versão do Python está instalada. Isso é algo que você pode controlar.

Abra [.devcontainer/devcontainer.json](./.devcontainer/devcontainer.json) e substitua a seguinte seção:

```json
"VARIANT": "3.8-bullseye"
```

com a seguinte instrução:

```json
"VARIANT": "3.9-bullseye"
```

Essa alteração instrui o Codespaces a usar o Python 3.9 em vez do 3.8.

Se você fizer qualquer alteração na configuração do `devcontainer.json`, uma caixa aparecerá após salvar.

![Recriando Codespace](./images/Codespace_rebuild.png)

Clique em reconstruir. Aguarde até que seu Codespace reconstrua o ambiente VS Code.

### Etapa 2: adicionar uma extensão

Seu ambiente vem com extensões pré-instaladas. Você pode alterar com quais extensões seu ambiente Codespaces começa. Veja como:

1. Abra o arquivo [.devcontainer/devcontainer.json](./.devcontainer/devcontainer.json) e localize o seguinte elemento JSON
**extensões**:

   ```json
   "extensions": [
    "ms-python.python",
    "ms-python.vscode-pylance"
   ]
   ```

1. Adicione _"ms-python.black-formatter"_ à lista de extensões. Ele deve acabar se parecendo com o seguinte:

   ```json
   "extensions": [
    "ms-python.python",
    "ms-python.vscode-pylance",
    "ms-python.black-formatter"
   ]
   ```

   Essa string é o identificador exclusivo do [Black Formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter&WT.mc_id=academic-77460-alfredodeza), uma extensão popular para formatar código Python de acordo com as melhores práticas. Adicionar o identificador _"ms-python.black-formatter"_ à lista permite que os Codespaces saibam que essa extensão deve ser pré-instalada na inicialização.

   Aviso: Ao alterar qualquer configuração no json, aparecerá uma caixa após salvar.

   ![Recriando o Codespace](../../images/Codespace_rebuild.png)

   Clique em reconstruir. Aguarde seu codespace reconstruir o ambiente do VS Code.

Para encontrar o identificador exclusivo de uma extensão:

- Navegue até a página da extensão, por exemplo [https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter](https://marketplace.visualstudio.com/items?itemName=ms- python.black-formatter&WT.mc_id=academic-77460-alfredodeza)
- Localize o campo *Identificador exclusivo* na seção **Mais informações** à sua direita.

## 🤖 Use o Copilot para criar uma aula para os alunos
O GitHub Copilot agora está disponível no GitHub Codespaces. Você pode usar o Copilot para criar uma aula para seus alunos. Este repositório inclui a extensão para Copilot para que você possa usá-lo imediatamente. Certifique-se de que sua conta tenha acesso ao Copilot. Caso não tenha acesso, você pode [solicitar acesso aqui](https://github.com/login?return_to=%2Fgithub-copilot%2Fsignup).

O GitHub Copilot é gratuito para alunos e professores. [Saiba mais](https://education.github.com/pack/offers). Siga [estas etapas](https://techcommunity.microsoft.com/t5/educator-developer-blog/step-by-step-setting-up-github-student-and-github-copilot-as-an/ba- p/3736279?WT.mc_id=academic-0000-alfredodeza) para verificar sua associação de aluno ou professor e habilitar o Copilot gratuitamente.

### Passo 1: Escreva uma descrição para sua aula
Abra o arquivo [examplo-notebook.ipynb](./examplo-notebook.ipynb) e escreva uma descrição para sua lição na primeira célula. Certifique-se de que o Copilot esteja ativado clicando no ícone do Copilot na barra de status e verificando se você está conectado ao GitHub.

Edite a primeira célula e comece a digitar `Para esta lição`. O Copilot irá sugerir uma descrição para sua aula. Selecione a sugestão e pressione `Tab` para aceitá-la.

A célula agora deve ser semelhante a esta:

```markdown
# Crie uma aula usando o GitHub Copilot
Nesta lição, você usará o GitHub Copilot para criar uma lição para os alunos aprenderem a escrever funções em Python. Você usará o Copilot para escrever código e usará o Copilot para escrever texto.
```

Tudo bem se o Copilot não sugerir uma réplica exata do texto acima. Você pode editar o texto para torná-lo mais adequado para sua lição.

### Passo 2 Adicione etapas à sua lição
Adicione uma nova célula abaixo da célula de descrição e comece a digitar `### Etapa 1: Habilitar` para criar uma nova etapa em sua lição. O Copilot irá sugerir uma etapa para sua aula. Selecione a sugestão e pressione `Tab` para aceitá-la.

A célula agora deve ser semelhante a esta:

```markdown
## Passo 1: Habilitar GitHub Copilot
Habilite o Copilot seguindo as instruções na [documentação do GitHub Copilot](https://docs.github.com/pt/codespaces/developing-with-codespaces/using-codespaces-with-github-copilot). Se você é um estudante, pode obter um [GitHub Student Developer Pack] gratuito (https://education.github.com/pack) para obter acesso ao Copilot.
```

Continue adicionando mais etapas e digitando para obter sugestões mais precisas para o conteúdo de seu interesse. Por exemplo, esta é uma etapa sugerida pelo Copilot para a próxima etapa da lição:

```markdown
## Passo 3: Crie desafios para esta lição
Você ensinará os alunos a escrever funções em Python.
```

Você pode usar o exemplo acima para ver o que o Copilot pode sugerir e preencher automaticamente. Sinta-se à vontade para adicionar quantas etapas achar necessárias para sua lição.

### Passo 3: adicione desafios de código para os alunos
Adicione uma nova célula de código abaixo da última etapa e comece com um comentário Python que descreva o desafio. Por exemplo, você pode escrever `# crie um desafio para um aluno escrever uma função que retorne a soma de dois números`. O Copilot irá sugerir uma solução para o desafio. Selecione a sugestão e pressione `Tab` para aceitá-la. Para cada nova linha, você pode pressionar `Return` (ou `Enter`) para obter uma nova sugestão.

Esta é uma amostra do que o Copilot sugeriu para o desafio acima:

```python
# create a challenge for a student to write a function that returns the sum of two numbers
"""
In this challenge, you'll write a function that returns the sum of two numbers.
You'll use the `sum` function to add the two numbers.
Start by writing a function that takes two numbers as parameters.
Then, use the `sum` function to add the two numbers.
Finally, return the sum of the two numbers.
"""
```

Novamente, seu desafio pode não ser exatamente igual ao anterior. Você pode editar o desafio para torná-lo mais adequado para sua aula.

Crie quantas células de código com prompts de exemplo para sua lição.

### Etapa 4: crie um questionário para os alunos
Adicione uma nova célula abaixo para escrever Markdown (não código!) e comece escrevendo `### Quiz`. Em seguida, adicione um comentário _HTML_ para criar um prompt para que o GitHub Copilot entenda que tipo de questionário você deseja criar. Por exemplo, você poderia usar algo parecido com isto:

```html
<!-- generate a quiz of 5 questions about using Python functions with a mix of variable arguments and keyword arguments -->
```

O Copilot pode não sugerir um teste para você imediatamente. Se for esse o caso, adicione novas linhas ao comentário e pressione `Return` (ou `Enter`) e comece a enumerar as perguntas que deseja fazer. Por exemplo, você poderia escrever:

```markdown
1. Qual é a saída do seguinte código?
```

Se você está procurando uma pergunta específica sobre um tópico, pode ser:

```markdown
2. Ao criar uma função que
```

Copilot sugeriu uma pergunta usando argumentos variáveis, que é o objetivo do desafio:

```markdown
3. Quando você cria uma função que aceita um número variável de argumentos, qual é o nome do parâmetro que você usa para acessar os argumentos?
```

Por fim, revise as células e faça as alterações necessárias. Você também pode adicionar mais etapas, desafios e perguntas à sua lição.

Parabéns! Você criou uma lição para os alunos aprenderem a escrever funções em Python usando o GitHub Copilot. Você pode usar o Copilot para ajudá-lo na documentação, escrever exemplos ou desafios como neste repositório. Mesmo esta seção inteira foi escrita usando o Copilot!

## Saiba mais

- [GitHub Codespaces docs - Visão geral](https://docs.github.com/pt/codespaces/overview)
- [GitHub Codespaces docs - Início rápido](https://docs.github.com/pt/codespaces/getting-started/quickstart)
- [Usando GitHub Codespaces com GitHub Classroom](https://docs.github.com/pt/education/manage-coursework-with-github-classroom/integrate-github-classroom-with-an-ide/using-github-codespaces-with-github-classroom)



### 🔎 Encontrou um problema ou tem uma ideia de melhoria?
Ajude-nos a deixar este repositório melhor [informando-nos e abrindo uma issue!](/../../issues/new).
