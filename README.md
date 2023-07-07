# Gerenciamento de vendas para uma padaria

Um modelo para o desenvolvimento do Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari. Um projeto criado para transformar uma padaria em algo mais tecnológico, um sistema para gerenciar o fluxo de vendas, visualizar, adicionar, editar e deletar pedidos, com níveis de acesso: Administrador e Cliente.

Professores: Marco André Mendes e Alann Perini.

Equipe:

    João Gabriel Puhl Machado
    Lígia de Angelis Gadotti

Links do projeto:

    Documentação (esse documento)
    Backend: [Repositório e Publicação](https://github.com/JoaoGabrielPuhlMachado/ligiaroupas-django)
    Frontend: [Repositório e Publicação](https://github.com/JoaoGabrielPuhlMachado/ligiaroupas-vue-3)


# Situação problema 

<font size=4>

A nossa cliente, Lígia, quer abrir uma loja online de roupas chamada Lígia Roupas. Ela precisa de um site que permita que seus clientes visualizem os produtos, categorias de roupas e suas marcas, de maneira prática. Lígia irá administrar o site, junto de seus funcionários.

</font>

# Proposta:

<font size=4>

O sistema será dividido em 2 níveis de acesso: administradores e clientes.

O administrador pode adicionar, editar, ver e deletar produtos, categorias, marcas, tamanhos e cores.

O cliente pode ver os produtos, marcas, categorias, tamanhos, cores, perfil e deletar seu perfil

O software irá controlar todo o estoque, organizando os produtos e filtrando por menor preço, maior preço, mais vendido, menos vendido, ordem alfabética crescente ou decrescente.

O administrador começa o dia verificando e anotando se tem os produtos necessários para o dia e semana, caso algo precise ser comprado logo. O administrador olha o estoque e confere a quantidade de seus produtos, caso alguma coisa esteja quase ou em falta, ele encomenda este produto. Ele também confere as marcas de roupa que a loja possui e adiciona ou remove esta marca caso a loja não tenha mais produtos da determinada marca.

O cliente acessa o site e olha todos os produtos disponíveis, podendo filtrá-los por marca e/ou categoria, ao escolher certo produto, irá ser automaticamente enviado para seu carrinho e decidir se irá adicionar mais produtos ou se irá pagar. O cliente ao acessar seu carrinho, poderá conferir todos os produtos que pediu e suas quantidades, ao selecionar pagamentos, terá uma aba para informar seus dados pessoais como: nome, email, telefone, endereço, cpf. Após informado seus dados, deverá escolher como pagar: cŕedito, débito, pix ou boleto, informando o que é pedido, como dados do seu cartão (número, código de segurança e nome inscrito no cartão).

Ao finalizar a compra, o cliente irá receber um email informando seus dados e seus produtos pedidos, também confirmando seu pagamento (aprovado ou em andamento), irá receber o rastreamento do pedido após o envio desse pedido.

O Administrador irá receber o pedido do cliente, conferir tudo que foi requisitado e mandar o funcionário separar e preparar o produto do cliente. 

</font>

# Regras de negócio

<font size=4>

- **RN01 - Criação do pedido:** O pedido será criado pelo cliente, que escolhe os produtos, a quantidade e o tamanho e adiciona eles ao carrinho. 

- **RN02 - Acessar o carrinho:** O cliente acessa seu carrinho e confere todos os produtos que pediu e suas quantidades. Ele pode finalizar a sua compra, deletar algo ou continuar escolhendo roupas.

- **RN03 - Pagamento:** Depois de finalizar o carrinho o cliente informa seus dados pessoais (nome, email, telefone, endereço, cpf) e escolhe o metódo de pagamento, que pode ser cŕedito, débito, pix ou boleto. Caso for escolhido o cartão de crédito, o cliente informa os dados do cartão (número, código de segurança e nome inscrito no cartão).

- **RN04 - Confirmação do pedido:** o cliente recebe um email informando seus dados e seus produtos pedidos, também confirmando status de pagamento (aprovado ou em andamento) e rastreia o produto após seu envio.

- **RN05 - Envio do pedido:** O Administrador recebe o pedido do cliente, confere tudo que foi requisitado e manda o funcionário separar e preparar o produto do cliente.

</font>

# Requisitos funcionais

<font size=4>

**Entrada**

- **RF01 - CRUD de produtos:** O sistema deve permitir o criar, editar, visualizar e deletar: produtos, categorias, marcas, tamanhos e cores disponíveis na loja.**Usuários:** Administrador.
  
- **RF02 - Visualização de produtos:** O sistema deve permitir o cliente visualizar: produtos, categorias, marcas, tamanhos e cores disponíveis na loja. **Usuários:** Cliente.
  

**Processamento**

- **RF03 - Carrinho:** O sistema deve permitir que o cliente selecione o produto desejado e adicione ele ao carrinho.


- **RF04 - Pedido:** O sistema deve criar uma nota fiscal com as informações contidas no carrinho após o cliente finalizar o pedido.

- **RF05 - Controle de estoque:** O sistema deve manter um registro atualizado do estoque de produtos da loja de roupa, permitindo ao administrador verificar a quantidade de produtos disponíveis e identificar quando é necessário fazer novos pedidos aos fornecedores.

- **RF06 - Edição do carrinho:** O sistema deve permitir que os clientes editem o carrinho, adicionando ou removendo produtos, caso o cliente deseje fazer alterações no pedido.

- **RF07 - Formas de pagamento:** O sistema deve permitir que o cliente escolha a forma de pagamento como: dinheiro, pix, cartão de crédito ou débito, e gere a nota fiscal correspondente.

**Saída**

- **RF08 - Relatórios de vendas:** O sistema deve permitir que o administrador gere relatórios de vendas, incluindo informações como entrada e saída de produtos, produtos mais vendidos e menos vendidos, faturamento diário ou semanal, e outros filtros selecionados pelo gerente.

- **RF09 - Gerenciamento de informações gerais:** O sistema deve permitir que o gerente organize e filtre as informações de entrada e saída de produtos, notas fiscais, recibos e lucro da loja por dia, semana, mês ou ano, de acordo com os tipos de filtros desejados.
  
- **RF10 - Envio de email:** O sistema deve enviar um email para o cliente utilizando o email informado do mesmo, contendo informações da nota fiscal como: nome dos produtos, quantidade, método de pagamento, endereço de entrega, valor total da compra e individual dos produtos, rastreamento do pedido e número do pedido.

</font>

# Requisitos Não Funcionais
<font size=4>

- **RNF01 - Tempo máximo de resposta:** O sistema deve ter um tempo máximo de resposta de 5 segundos em condições normais de uso para uma solicitação do usuário.

- **RNF02 - Backup e recuperação de dados:** O sistema deve ser capaz de realizar backup e recuperação de dados de forma eficiente para garantir a disponibilidade do serviço em caso de falhas técnicas.

- **RNF03 - Compatibilidade com diferentes navegadores e dispositivos:** O sistema deve garantir a compatibilidade com diferentes navegadores e dispositivos para atender às necessidades dos usuários, como: chrome, opera, firefox, edge e etc.

- **RNF04 - Interface responsiva:** A interface do sistema deve ser responsiva, permitindo que os usuários acessem o sistema de forma eficiente em diferentes dispositivos e tamanhos de tela.

- **RNF05 - Segurança dos dados:** O sistema deve garantir a segurança dos dados dos usuários, protegendo-os contra acessos não autorizados e ataques cibernéticos.

- **RNF06 - Manutenção periódica:** O sistema deve passar por manutenção periódica pelo menos uma vez a cada 1 ou 3 meses para garantir a estabilidade e confiabilidade do sistema.

</font>

# Casos de Uso
<font size=4>

    Link do Diagrama: 

</font>

