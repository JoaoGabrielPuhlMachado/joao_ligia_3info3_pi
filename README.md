# Modelo 1: Ponto de Vendas (PDV)
**Gerenciamento de vendas para uma padaria**

<font size=4>

O nosso cliente, Sr Genival, tem uma padaria de bairro chamada Padaria Céu e, devido a qualidade de seus produtos, ela está crescendo rapidamente. Recentemente, ele contratou mais funcionários para atendimento, caixa, panificação, etc. Assim, atualmente, ele consegue concentrar seus esforços para melhorar a gestão da padaria. Para isso, ele quer instalar um sistema de controle de vendas que permita ao caixa lançar as vendas realizadas. Como sua intenção é melhorar a gestão do negócio, é muito importante que ele consiga ter relatórios, como por exemplo, de vendas.

</font>

# Introdução:

<font size=4>

A Padaria Céu existe há 20 anos, está crescendo rapidamente e contratou novos funcionários, por isso precisa de um software. O seu dono, Sr Genival, cuida da gestão da padaria e faz o controle de estoque, no total há 5 funcionários: duas atendentes, duas pessoas responsáveis por assar os pães, preparar o que é necessário e um caixa.

</font>

# Situação problema:

<font size=4>

- O gerente começa o dia verificando e anotando se tem os produtos necessários para o dia e semana, caso algo precise ser comprado logo. O gerente olha o estoque e confere a quantidade de seus produtos, caso alguma coisa esteja quase ou em falta, ele encomenda este produto.

- O cliente chega ao balcão e faz seu pedido a uma das atendentes, ela anota o pedido em uma comanda e entrega ao cliente. O cliente vai ao caixa e entrega a comanda para o funcionário, que verifica se o cliente deseja algo mais e solicita a forma de pagamento.

- O cliente informa como deseja pagar e o caixa põe o dinheiro no caixa, caso seja cartão ele entrega a nota fiscal ao cliente se solicitado.
Ao final do dia, a caixa separa as comandas e o gerente anota cada valor, nome do produto e quantia do produto vendido.

</font>

# Conclusão:

<font size=4>

Para melhorar o funcionamento da padaria, o software deve permitir que a atendente marque o que foi pedido no sistema gerando uma comanda, o sistema calcula o valor total da comanda/pedido e agiliza o pagamento no caixa. Todos os pedidos ficarão registrados no sistema e no final do dia o gerente tem a possibilidade de gerar um relatório contendo: Entrada e saída de produtos, produtos mais vendidos e menos vendidos,  faturamento diário ou semanal.  Para melhorar a gestão financeira e produtos e gerenciamento dos funcionários. 

</font>

# Proposta:

<font size=4>

O software irá controlar todo o estoque organizando os produtos e filtrando por menor preço, maior preço, mais vendido, menos vendido, ordem alfabética crescente ou decrescente.

O sistema será dividido em 3 níveis de acesso: atendente, caixa, gerente.
A atendente poderá apenas visualizar e adicionar os produtos dos clientes a uma comanda virtual, após gerada essa comanda terá as informações dos produtos e um número para identificar de qual cliente é a comanda;

A comanda será criada após o atendente confirmar tudo que o cliente deseja, com um número de identificação igual ao da ficha retirada pelo cliente para ser atendido, essa comanda terá o nome do cliente, quais produtos ele pediu, a quantidade deles, o valor deles e o total. Sendo possível a edição desses itens após o cliente se redirecionar ao caixa e o funcionário confirmar seu pedido. Itens do balcão do caixa ou geladeira como: balas, chicletes, água e refrigerantes serão escaneados pelo caixa após o cliente entregá-los e será registrado na comanda final, resolvendo o problema de produtos não listados na comanda inicial da atendente;

A caixa poderá visualizar e adicionar os produtos igual a atendente, porém também poderá editar os produtos caso o cliente queira adicionar ou remover algum produto. Receberá a comanda da atendente com o número e irá chamar o cliente com esse número, vai perguntar ao cliente se isso é tudo que ele quer e depois perguntar a forma de pagamento. Finalizado o pagamento, a caixa irá fazer a nota fiscal e entregar ao cliente caso desejado;

O gerente terá acesso aos 2 níveis anteriores e poderá olhar toda entrada e saída de produtos com todas as informações deles como: Valor, quantidade, quais foram vendidos (separados por menos e mais vendidos). Acesso as notas fiscais e recibos de cada cliente, todo o dinheiro/lucro da padaria.
Tudo isso organizado e filtrado por dia/semana/mês/ano em uma planilha ordenada, selecionando quais tipos de filtros são desejados. O gerente também poderá agendar e pedir novos produtos e itens para a padaria contatando um fornecedor e definindo um dia para a entrega de seus produtos.

</font>

# Regras de negócio

<font size=4>

- RN01 - Criação da comanda: a comanda será criada pela atendente após o cliente falar quais produtos irá comprar.
<br><br>
- RN02 - Conteúdo da comanda: a comanda irá conter as informações do produto comprado (o que é, quantidade, valor), um número de identificação e nome do cliente.
<br><br>
- RN03 - Adicionar mais produtos: o caixa poderá escanear o código de barras e adicionar na comanda  produtos que não são pedidos no balcão (exemplos: balas, água, refrigerantes). Também poderá remover algo que o cliente não queira mais.
<br><br>
- RN04 - Nota fiscal: a nota fiscal será gerada somente após a finalização da venda.
<br><br>
- RN05 - O gerente: Somente o  gerente terá controle das informações de entrada e saída de produtos (valor, quantidade, quais foram vendidos).
<br><br>
- RN06 - Relatório de faturamento : o gerente terá acesso a uma planilha com: notas fiscais e recibos de cada cliente, todo o dinheiro/lucro da padaria, que poderá ser filtrado por: dia/semana/mês/ano.
<br><br>
- RN07 - Registro de produtos: O gerente poderá agendar e pedir novos produtos e itens para a padaria contatando um fornecedor e definindo um dia para a entrega de seus produtos.

</font>

# Requisito Funcional

<font size=4>

- RF01 - Cadastro de produtos: O sistema deve permitir o cadastro de produtos disponíveis na padaria, incluindo nome, descrição, preço, quantidade em estoque e outras informações relevantes.
<br><br>
- RF02 - Controle de estoque: O sistema deve manter um registro atualizado do estoque de produtos da padaria, permitindo ao gerente verificar a quantidade de produtos disponíveis e identificar quando é necessário fazer novos pedidos aos fornecedores.
<br><br>
- RF03 - Comanda virtual: O sistema deve permitir que as atendentes criem uma comanda virtual para cada cliente, registrando os produtos solicitados, a quantidade, o valor e o total da comanda.
<br><br>
- RF04 - Edição da comanda: O sistema deve permitir que as atendentes e caixas editem a comanda virtual, adicionando ou removendo produtos, caso o cliente deseje fazer alterações no pedido.
<br><br>
- RF05 - Escaneamento de produtos: O sistema deve permitir que o caixa escaneie produtos do balcão, como balas, chicletes, água e refrigerantes, para incluí-los na comanda final do cliente.
<br><br>
- RF06 - Formas de pagamento: O sistema deve permitir que o caixa registre a forma de pagamento escolhida pelo cliente, como dinheiro, cartão de crédito ou débito, e gere a nota fiscal correspondente.
<br><br>
- RF07 - Relatórios de vendas: O sistema deve permitir que o gerente gere relatórios de vendas, incluindo informações como entrada e saída de produtos, produtos mais vendidos e menos vendidos, faturamento diário ou semanal, e outros filtros selecionados pelo gerente.
<br><br>
- RF08 - Níveis de acesso: O sistema deve ter três níveis de acesso: atendente, caixa e gerente, com permissões de visualização, adição e edição de produtos e comandas de acordo com o nível de acesso de cada usuário.
<br><br>
- RF09 - Agendamento de pedidos: O sistema deve permitir que o gerente agende e faça pedidos de novos produtos e itens para a padaria, entrando em contato com os fornecedores e definindo data de entrega dos produtos.
<br><br>
- RF10 - Organização e filtragem de informações: O sistema deve permitir que o gerente organize e filtre as informações de entrada e saída de produtos, notas fiscais, recibos e lucro da padaria por dia, semana, mês ou ano, de acordo com os tipos de filtros desejados.

</font>