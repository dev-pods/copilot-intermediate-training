# Guia de Demonstração: Práticas de Codificação com Copilot Chat

Este guia fornece um passo a passo detalhado sobre como utilizar o GitHub Copilot Chat para implementar e validar uma função utilitária dentro do repositório PowerBI JavaScript. O foco está na eficiência, manutenção e melhores práticas.

---

## Pré-requisitos

1. **Configuração do Repositório**:
   - Clone o [Repositório PowerBI JavaScript](https://github.com/microsoft/PowerBI-JavaScript).
   - Instale o [Visual Studio Code](https://code.visualstudio.com/) com as extensões GitHub Copilot e Copilot Chat.

2. **Ambiente de Desenvolvimento**:
   - Certifique-se que Node.js e npm estejam instalados.
   - Confirme que o Jest esteja configurado para testes.

---

## Tarefa 1: Implementar a Função Utilitária `calculatePercentage`

### Objetivo
Criar uma função utilitária reutilizável que calcule porcentagens, tratando casos excepcionais como divisão por zero.

### Passos

1. **Identificar o Arquivo de Utilitários**:
   - Use `@workspace` para localizar o arquivo correto para funções utilitárias:
     `@workspace, onde devo colocar uma nova função utilitária para cálculos de porcentagem?`

2. **Criar a Função**:
   - Peça ao Copilot Chat para gerar a função:
     `Você pode escrever uma função utilitária chamada calculatePercentage em JavaScript que aceita dois argumentos, part e total, e calcula a porcentagem? Garanta que a função trate casos onde total é zero, retornando 0.`

3. **Tratar Casos Excepcionais**:
   - Consulte o Copilot Chat para casos excepcionais adicionais:
     `Quais são alguns casos de teste adicionais que devo incluir para esta função utilitária?`

4. **Documentar a Função**:
   - Adicione uma descrição da função e seus parâmetros:
     `Refatorar o seguinte arquivo para incluir uma breve descrição do propósito da função e seus parâmetros.`

---

## Tarefa 2: Gerar Testes Unitários

### Objetivo
Escrever e executar testes unitários usando Jest para validar a funcionalidade de `calculatePercentage`.

### Passos

1. **Configurar o Ambiente de Teste**:
   - Execute:
     ```
     npm test
     ```
   - Se o Jest não estiver instalado, use:
     ```
     npm install jest
     ```

2. **Criar um Arquivo de Teste**:
   - Localize o diretório de testes com `@workspace`:
     `@workspace, onde está o diretório de testes atual?`
   - Crie `calculatePercentage.test.js` no diretório.

3. **Escrever Testes Unitários**:
   - Peça ao Copilot Chat para gerar casos de teste:
     `Crie testes unitários para a função calculatePercentage que criamos.`

4. **Executar os Testes**:
   - Execute:
     `npm test calculatePercentage.test.js`

5. **Depurar e Iterar**:
   - Use o Copilot Chat para solucionar problemas em testes que falham:
     `Por que esse teste está falhando e como posso corrigi-lo?`

---

## Tarefa 3: Refatorar e Adicionar Comentários

### Objetivo
Melhorar a legibilidade do código adicionando comentários robustos e aderindo às convenções de nomenclatura.

### Passos

1. **Localizar Arquivos Modificados**:
   - Use `@workspace` para encontrar arquivos alterados:
     `@workspace, quais arquivos eu modifiquei até agora para esta tarefa?`

2. **Adicionar Comentários**:
   - Solicite ao Copilot Chat para adicionar comentários explicativos:
     `Adicione comentários robustos para o seguinte arquivo que explica o que cada parte do código está fazendo.`

3. **Refatorar para Convenções de Nomenclatura**:
   - Atualize para camelCase ou outras convenções, se necessário.

---

## Tarefa 4: Deployment e Consumo

### Objetivo
Demonstrar a funcionalidade de `calculatePercentage` em um arquivo JavaScript independente.

### Passos

1. **Criar um Arquivo Consumidor**:
   - Navegue até a raiz do repositório.
   - Crie `consumeCalculatePercentage.js`.

2. **Importar a Função**:
   ```javascript
   const { calculatePercentage } = require('./path/to/utilities');
   ```

3. **Escrever Casos de Uso de Exemplo**:
   ```javascript
   console.log('Example 1:', calculatePercentage(50, 100)); // Expected Output: 50
   console.log('Example 2:', calculatePercentage(23, 0));  // Expected Output: 0
   console.log('Example 3:', calculatePercentage(7, 20));  // Expected Output: 35
   ```

4. **Executar o Arquivo**:
   ```
   node consumeCalculatePercentage.js
   ```

5. **Documentar o Arquivo**:
   - Adicione um bloco de comentário explicando seu propósito:
     ```javascript
     /**
      * Este é um arquivo de demonstração simples para consumir a função utilitária calculatePercentage.
      * Ele demonstra a funcionalidade da função com casos de uso básicos.
      */
     ```

6. **Aprimorar a Demonstração**:
   - Use o Copilot Chat para sugestões e refatoração.
   - Opcionalmente, adicione tratamento de erros:
     ```javascript
     try {
       console.log('Example 4:', calculatePercentage('invalid', 20));
     } catch (error) {
       console.error('Error:', error.message);
     }
     ```

---

## Resumo

Esta demonstração apresentou o poder do GitHub Copilot Chat na implementação, teste e documentação de uma função utilitária reutilizável. Seguindo estes passos, você irá:
- Desenvolver código limpo e de fácil manutenção.
- Aproveitar a IA para otimizar processos de desenvolvimento.
- Garantir funcionalidade robusta através de testes abrangentes e documentação.

### Recursos
- [Repositório PowerBI JavaScript](https://github.com/microsoft/PowerBI-JavaScript)
- [Documentação do Jest](https://jestjs.io/docs/getting-started)
