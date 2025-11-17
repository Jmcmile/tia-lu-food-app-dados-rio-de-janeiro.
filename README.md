🍔 Sistema de Gerenciamento de Pedidos

👥 Equipe

Jamile Martins Coutrim

📖 Descrição
O sistema é uma aplicação de console que simula um ambiente completo de pedidos para uma lanchonete. Ele permite cadastrar itens no menu, criar pedidos, consultar status, 
organizar filas e salvar todos os dados utilizando JSON. Também inclui estrutura avançada com mapas (dict), algoritmo de ordenação próprio (insertion sort) e um indexador baseado em árvore AVL para gerenciamento e
busca eficiente dos pedidos.

⚙️ Estrutura e Funcionalidades

A aplicação segue uma arquitetura modular organizada em arquivos e funções separadas, garantindo manutenção simples e expansão futura.

Principais componentes:

menu.json → Armazena os itens do cardápio.
pedidos.json → Armazena pedidos criados durante o uso.
Módulo de Ordenação (Insertion Sort) → Ordena cardápio ou pedidos por preço, nome ou ID.
Árvore AVL → Armazena e indexa pedidos para busca rápida (por ID).
Sistema de Filas → Garante ordem de atendimento correta.
Funções Modulares → Cada ação do sistema possui sua função exclusiva.

🔹 Gerenciar Menu de Pedidos

O sistema possui um módulo para gerenciar o cardápio da lanchonete:

Funções incluídas:

✔ Adicionar novos itens ao menu
✔ Remover itens existentes
✔ Editar informações (preço, nome, categoria)
✔ Listar itens por categoria
✔ Ordenar itens usando o algoritmo insertion sort
✔ Salvar e carregar automaticamente o menu via JSON

🔹 Fluxo de Pedidos e Filas

O sistema trabalha com duas filas:
Fila de Pedidos Criados
Sempre que um cliente faz um pedido, ele entra nessa fila.
Fila de Pedidos Prontos / Entrega
Pedidos concluídos são movidos para esta segunda fila.

Processo:

O usuário escolhe itens do menu
O sistema gera automaticamente um ID único
O pedido é salvo e também indexado na árvore AVL
O pedido entra na fila de produção
Conforme os pedidos vão sendo concluídos, passam para a fila de retirada

🔹 Fluxo de Status do Pedido

Cada pedido passa por 4 estados:
Aguardando Preparo
Em Preparo
Pronto
Finalizado/Retirado
O sistema permite:
Atualizar status manualmente
Exibir todos os pedidos de uma determinada etapa
Mover automaticamente entre filas

🔹 Consultas

O sistema oferece múltiplas consultas:

1. Buscar Pedido por ID (via árvore AVL)

Busca extremamente rápida, mesmo com muitos pedidos.

2. Listar todos os pedidos

Com ordenação opcional por:
Nome
Preço
ID
(Usando insertion sort)

3. Listar status dos pedidos
Todos os que estão aguardando
Todos que estão sendo preparados
Todos que estão prontos
Todos finalizados

4. Listar itens do menu por categoria

Salgados
Doces
Bebidas

🛠️ Tecnologias Utilizadas

O sistema utiliza:
Tecnologia / Conceito	Uso

Python 	Linguagem principal
JSON 	Armazenamento persistente dos dados
Mapas  (dict)	Representação de cardápio e pedidos
Funções  Modulares	Organização do código
Insertion Sort 	Ordenação personalizada
Árvore AVL 	Indexação eficiente de pedidos
Filas (Queue) 	Controle de operação de produção

▶️Como Executar

Clonar o:

python sistema_pedidos.py
