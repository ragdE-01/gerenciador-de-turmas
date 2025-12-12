# gerenciador-de-turmas
 
Sistema simples em Python para gerenciar turmas, alunos e notas. Projeto em evolução
 
Um sistema em Python que gerencia turmas, alunos e notas diretamente pelo terminal. Ele salva todos os dados em arquivos .txt com estrutura própria, permitindo registrar novas turmas, adicionar alunos, ajustar notas e recuperar tudo mesmo após fechar o programa. O foco é manter todas as operações claras, diretas e fáceis de acompanhar, garantindo persistência e organização dos dados de forma prática.

## Funcionalidades
- Criar turmas
- Listar turmas já registradas
- Adicionar alunos a uma turma
- Registrar e modificar notas dos alunos
- Salvar todos os dados em arquivos `.txt`
- Carregar automaticamente as turmas e alunos existentes
- Organização persistente dos dados entre execuções

## Como os dados são armazenados
O sistema utiliza um único arquivo de texto para guardar todas as informações.
Esse arquivo usa uma estrutura própria, baseada em:

Uma assinatura no topo, que identifica que o arquivo pertence ao sistema.

Blocos nomeados, cada um representando uma categoria de dados (TURMAS, ALUNOS, MATERIAS_EXISTENTES...).

Chaves { }, que indicam início e fim de cada bloco ou subbloco.

## Como executar
1. Certifique-se de ter o Python instalado (3.8+)
2. Baixe ou clone este repositório
3. Execute o arquivo principal ou o nome do arquivo que inicia o sistema.

## Estrutura do Projeto

Quando você baixa o repositório, apenas os arquivos do sistema aparecem:

SYS_gerenciador_alunos/
│
├── gerenciador_alunos.py       
└── mod_gerenciador_alunos.py   

Após executar o sistema pela primeira vez e salvar as alterações, um arquivo de registros é criado automaticamente:

SYS_gerenciador_alunos/
│
├── gerenciador_alunos.py
├── mod_gerenciador_alunos.py
├── registros_gerenciador_alunos_0.txt  
└── __pycache__/         

## Fluxo de uso
1.Registre as matérias.
Sem matérias, o sistema não permite criar turmas.

2.Crie as turmas.
Ao registrar uma turma, você escolhe quais matérias ela terá.
O sistema só permite criar turmas após existir pelo menos uma matéria.

3.Cadastre os alunos.
Só é possível registrar um aluno após existir pelo menos uma turma.
Cada aluno é vinculado a uma turma e recebe automaticamente o conjunto de matérias dessa turma.

4.Use o menu para consultar e alterar dados.
É possível verificar médias, ajustar notas e revisar informações em geral.

5.Finalize o sistema pela opção "Fechar e salvar".
Como ainda não existe salvamento automático, essa opção garante que todas as alterações sejam gravadas no arquivo de dados.

## Melhorias planejadas
1.Tornar o parser mais tolerante a erros no arquivo (validações/backup)
2.Exportar/importar em JSON ou CSV para interoperabilidade
3.Adicionar interface simples no terminal (menu mais claro)

## Observações
Este projeto é uma base de estudos: foi criado para praticar organização de dados, parsing, fluxo de I/O e lógica de programa.
Se você editar manualmente os arquivos de registro, certifique-se de manter a estrutura de blocos exatamente como o exemplo para evitar falhas no carregamento.
