# Gerenciamento de vendas para uma padaria

Um modelo para o desenvolvimento do Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari. Um projeto criado para transformar uma padaria em algo mais tecnológico, um sistema para gerenciar o fluxo de vendas, visualizar, adicionar e editar pedidos, com níveis de acesso: atendente, caixa, gerente.

Professores: Marco André Mendes e Alann Perini.

Equipe:

    João Gabriel Puhl Machado
    Lígia de Angelis Gadotti

Links do projeto: (Coloque aqui os links para a documentação do projeto e os repositórios e plubicação do backend e frontend.)

    Documentação (esse documento)
    Backend: Repositório e Publicação
    FrontendRepositório e Publicação


# Situação problema 

<font size=4>

O nosso cliente, Sr Genival, tem uma padaria de bairro chamada Padaria Céu e, devido a qualidade de seus produtos, ela está crescendo rapidamente. Recentemente, ele contratou mais funcionários para atendimento, caixa, panificação, etc. Assim, atualmente, ele consegue concentrar seus esforços para melhorar a gestão da padaria. Para isso, ele quer instalar um sistema de controle de vendas que permita ao caixa lançar as vendas realizadas. Como sua intenção é melhorar a gestão do negócio, é muito importante que ele consiga ter relatórios, como por exemplo, de vendas.

</font>

<font size=4>

A Padaria Céu existe há 20 anos, está crescendo rapidamente e contratou novos funcionários, por isso precisa de um software. O seu dono, Sr Genival, cuida da gestão da padaria e faz o controle de estoque, no total há 5 funcionários: duas atendentes, duas pessoas responsáveis por assar os pães, preparar o que é necessário e um caixa.

</font>

<font size=4>

O gerente começa o dia verificando e anotando se tem os produtos necessários para o dia e semana, caso algo precise ser comprado logo. O gerente olha o estoque e confere a quantidade de seus produtos, caso alguma coisa esteja quase ou em falta, ele encomenda este produto.

O cliente chega ao balcão e faz seu pedido a uma das atendentes, ela anota o pedido em uma comanda e entrega ao cliente. O cliente vai ao caixa e entrega a comanda para o funcionário, que verifica se o cliente deseja algo mais e solicita a forma de pagamento.

O cliente informa como deseja pagar e o caixa põe o dinheiro no caixa, caso seja cartão ele entrega a nota fiscal ao cliente se solicitado.

Ao final do dia, a caixa separa as comandas e o gerente anota cada valor, nome do produto e quantia do produto vendido.

</font>

<font size=4>

Para melhorar o funcionamento da padaria, o software deve permitir que a atendente marque o que foi pedido no sistema gerando uma comanda, o sistema calcula o valor total da comanda/pedido e agiliza o pagamento no caixa. Todos os pedidos ficarão registrados no sistema e no final do dia o gerente tem a possibilidade de gerar um relatório contendo: Entrada e saída de produtos, produtos mais vendidos e menos vendidos,  faturamento diário ou semanal.  Com a implantação desse sistema, espera-se melhorar a gestão financeira, a gestão do estoque dos produtos e o gerenciamento dos funcionários. 

</font>

# Proposta:

<font size=4>

O software irá controlar todo o estoque, organizando os produtos e filtrando por menor preço, maior preço, mais vendido, menos vendido, ordem alfabética crescente ou decrescente.

O sistema será dividido em 3 níveis de acesso: atendente, caixa, gerente. 

A atendente poderá apenas visualizar e adicionar os produtos dos clientes a uma comanda virtual. Após gerada, essa comanda terá as informações dos produtos e um número para identificar de qual cliente é a comanda. A comanda será criada após o atendente confirmar tudo que o cliente deseja, com um número de identificação igual ao da ficha retirada pelo cliente para ser atendido. Essa comanda terá o nome do cliente, quais produtos ele pediu, a quantidade deles, o valor deles e o total. Será possível a edição desses itens após o cliente encamimhar-se ao caixa e o funcionário confirmar seu pedido. Itens do balcão do caixa ou geladeira como: balas, chicletes, água e refrigerantes serão escaneados pelo caixa após o cliente entregá-los e serão registrados na comanda final, resolvendo o problema de produtos não listados na comanda inicial da atendente.

A caixa poderá visualizar e adicionar os produtos da mesma forma que a atendente, porém também poderá editar os produtos, caso o cliente queira adicionar ou remover algum produto. A caixa receberá a comanda da atendente com o número e irá chamar o cliente com esse número, perguntará ao cliente se isso é tudo que ele quer e depois perguntará a forma de pagamento. Finalizado o pagamento, a caixa emitirá a nota fiscal e entregará ao cliente, caso desejado.

O gerente terá acesso aos 2 níveis anteriores e terá acesso a toda entrada e saída de produtos com todas as informações deles como: valor, quantidade, quais foram vendidos (separados por menos e mais vendidos). Acesso as notas fiscais e recibos de cada cliente, e informações de faturamento e lucro da padaria. Tudo isso organizado e filtrado por dia/semana/mês/ano em uma planilha ordenada, selecionando quais tipos de filtros são desejados. O gerente também poderá agendar e pedir novos produtos e itens para a padaria contatando um fornecedor e definindo um dia para a entrega de seus produtos.

</font>

# Regras de negócio

<font size=4>

- **RN01 - Criação da comanda:** a comanda será criada pela atendente após o cliente falar quais produtos deseja comprar. 

- RN02 - Conteúdo da comanda: a comanda irá conter as informações do produto comprado. **Produtos precisam estar no sistema.**

- RN03 - Adicionar mais produtos: o caixa poderá escanear o código de barras e adicionar na comanda  produtos que não são pedidos no balcão (exemplos: balas, água, refrigerantes). Também poderá remover algo que o cliente não queira mais.

- RN04 - Nota fiscal: a nota fiscal será gerada somente após a finalização da venda.

- RN05 - Controle de produtos: Somente o  gerente terá controle das informações de entrada e saída de produtos (valor, quantidade, quais foram vendidos).

- RN06 - Relatório de faturamento: o gerente terá acesso a uma planilha com: notas fiscais e recibos de cada cliente, todo o dinheiro/lucro da padaria, que poderá ser filtrado por: dia/semana/mês/ano.

- RN07 - Registro de produtos: O gerente poderá agendar e pedir novos produtos e itens para a padaria contatando um fornecedor e definindo um dia para a entrega de seus produtos.

**modificar para regras+++++++++++++++++**
- RF08 - Níveis de acesso: O sistema deve ter três níveis de acesso: atendente, caixa e gerente, com permissões de visualização, adição e edição de produtos e comandas de acordo com o nível de acesso de cada usuário.



</font>

# Requisitos funcionais

<font size=4>

**Entrada**

- **RF01 - Cadastro de produtos:** O sistema deve permitir o cadastro de produtos disponíveis na padaria. **Dados Necessários:** nome, descrição, preço, quantidade em estoque e outras informações relevantes.**Usuários:** Gerente


**Processamento**

- RF09 - Agendamento de pedidos: O sistema deve permitir que o gerente agende e faça pedidos de novos produtos e itens para a padaria, entrando em contato com os fornecedores e definindo data de entrega dos produtos.


- RF03 - Comanda virtual: O sistema deve permitir que as atendentes criem uma comanda virtual para cada cliente, registrando os produtos solicitados, a quantidade, o valor e o total da comanda.

- RF02 - Controle de estoque: O sistema deve manter um registro atualizado do estoque de produtos da padaria, permitindo ao gerente verificar a quantidade de produtos disponíveis e identificar quando é necessário fazer novos pedidos aos fornecedores.

- RF04 - Edição da comanda: O sistema deve permitir que as atendentes e caixas editem a comanda virtual, adicionando ou removendo produtos, caso o cliente deseje fazer alterações no pedido.

- RF05 - Escaneamento de produtos: O sistema deve permitir que o caixa escaneie produtos do balcão, como balas, chicletes, água e refrigerantes, para incluí-los na comanda final do cliente.

- RF06 - Formas de pagamento: O sistema deve permitir que o caixa registre a forma de pagamento escolhida pelo cliente, como dinheiro, cartão de crédito ou débito, e gere a nota fiscal correspondente.


**Saída**

- RF07 - Relatórios de vendas: O sistema deve permitir que o gerente gere relatórios de vendas, incluindo informações como entrada e saída de produtos, produtos mais vendidos e menos vendidos, faturamento diário ou semanal, e outros filtros selecionados pelo gerente.

- RF10 - Gerenciamento de informações gerais: O sistema deve permitir que o gerente organize e filtre as informações de entrada e saída de produtos, notas fiscais, recibos e lucro da padaria por dia, semana, mês ou ano, de acordo com os tipos de filtros desejados.

</font>

# Requisitos Não Funcionais
<font size=4>

**- RNF01 - Tempo máximo de resposta:** O sistema deve ter um tempo máximo de resposta de 5 segundos em condições normais de uso para uma solicitação do usuário.

- RNF02 - Backup e recuperação de dados: O sistema deve ser capaz de realizar backup e recuperação de dados de forma eficiente para garantir a disponibilidade do serviço em caso de falhas técnicas.

- RNF03 - Compatibilidade com diferentes navegadores e dispositivos: O sistema deve garantir a compatibilidade com diferentes navegadores e dispositivos para atender às necessidades dos usuários.**Quais???**

- RNF04 - Interface responsiva: A interface do sistema deve ser responsiva, permitindo que os usuários acessem o sistema de forma eficiente em diferentes dispositivos e tamanhos de tela.

- RNF05 - Segurança dos dados: O sistema deve garantir a segurança dos dados dos usuários, protegendo-os contra acessos não autorizados e ataques cibernéticos.

- RNF06 - Manutenção periódica: O sistema deve passar por manutenção periódica pelo menos uma vez a cada 1 ou 3 meses para garantir a estabilidade e confiabilidade do sistema.

</font>
