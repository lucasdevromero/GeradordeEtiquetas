## Gerador de Etiquetas para Impressão

Este projeto é um **Gerador de Etiquetas** baseado em HTML, CSS e JavaScript, que permite a criação e impressão de etiquetas contendo **Códigos de Barras** e **QR Codes**. O sistema oferece uma interface amigável para inserir os dados, validá-los em tempo real, e gerar uma visualização das etiquetas para impressão.

### Funcionalidades:

1. **Entrada de Dados**:
   - O usuário pode inserir dois tipos de dados:
     - **Códigos de Barras (WM)**: São inseridos na primeira área de texto, um código por linha.
     - **QR Codes**: São inseridos na segunda área de texto, também um código por linha.
   - A validação verifica se o número de códigos de barras é igual ao número de QR codes e se os dados inseridos estão no formato correto.

2. **Validação de Dados**:
   - **Campos Obrigatórios**: Garante que ambos os campos de entrada não fiquem vazios.
   - **Verificação de Formato**: Os QR codes e códigos de barras são validados para garantir que sigam o formato numérico correto.
   - **Correspondência no Mapeamento**: Verifica se cada código de QR possui uma correspondência válida em um mapeamento predefinido (ex: QR code “123” mapeado para “Doca 1”).
   - **Habilitação do Botão de Geração**: O botão "Gerar Etiquetas" é habilitado apenas quando os campos estão corretamente preenchidos e validados.

3. **Geração de Etiquetas**:
   - Quando os dados são validados corretamente, o botão "Gerar Etiquetas" permite abrir uma nova janela com uma pré-visualização das etiquetas.
   - Cada etiqueta gerada contém:
     - **Índice**: Exibe o número da etiqueta (em formato numerado).
     - **Código de Barras**: Exibe o código de barras gerado a partir dos dados inseridos.
     - **QR Code**: Exibe o QR code gerado para o código correspondente.
     - **Data e Hora de Impressão**: A data e hora de quando as etiquetas foram geradas.
     - **Logo da Empresa**: Exibe o logo da empresa, que pode ser personalizado.

4. **Estilo e Layout**:
   - O design utiliza **CSS Flexbox** para disposição dos campos de entrada e das etiquetas geradas. O layout é adaptável e responsivo, funcionando bem em dispositivos de diferentes tamanhos.
   - As etiquetas geradas possuem um tamanho fixo de **80mm x 50mm**, adequado para impressão em papel adesivo A4 com múltiplas etiquetas por página.
   
5. **Comando de Impressão**:
   - Após a visualização das etiquetas, a janela de pré-visualização oferece a opção de imprimir diretamente as etiquetas geradas.

### Tecnologias Utilizadas:

- **HTML**: Estrutura básica da página e dos campos de entrada.
- **CSS**: Estilos para formatação da página e layout das etiquetas.
- **JavaScript**: Funções para validação dos dados, atualização dos índices e geração das etiquetas para impressão.

### Como Usar:

1. Abra o arquivo index.html em um navegador de sua escolha.
2. Insira os **Códigos de Barras** e **QR Codes** nos campos de texto fornecidos.
3. O botão "Gerar Etiquetas" será habilitado assim que os dados forem corretamente validados.
4. Clique em "Gerar Etiquetas" para visualizar a pré-visualização e imprimir suas etiquetas.

### Customização:

- **Logo da Empresa**: O logo é exibido no topo esquerdo das etiquetas. Você pode personalizar a URL da imagem do logo modificando o atributo src na tag <img> da classe .logo.
- **Mapeamento de QR Codes**: O mapeamento de QR codes pode ser alterado no objeto mapeamentoQR dentro do script JavaScript. Adicione ou remova os códigos conforme necessário.
- **Tamanho da Etiqueta**: O tamanho das etiquetas foi configurado para **80mm x 50mm**. Você pode ajustar o tamanho das etiquetas alterando as propriedades CSS.

### Contribuições:

Contribuições são bem-vindas! Se você tiver alguma melhoria ou correção, fique à vontade para abrir um **Pull Request**.

---
