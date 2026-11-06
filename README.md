# jogo_da_memoria_c++
Jogo da Memória em C++

Jogo da memória para terminal, feito em C++ como trabalho da disciplina de Algoritmos e Programação 2 do curso de Ciência da Computação da Univali.

O tabuleiro é uma matriz de inteiros em que cada número aparece duas vezes. O jogador escolhe duas posições por jogada e ganha ponto quando os valores são iguais.

Funcionalidades
1 ou 2 jogadores, com cadastro de nome
Dois modos de jogo:
Normal: 24 cartas (tabuleiro 4x6, números de 1 a 12)
Rápido: 18 cartas (tabuleiro 3x6, números de 1 a 9)
Embaralhamento aleatório das cartas a cada partida
Tabuleiro exibido no terminal, com as cartas ainda não descobertas aparecendo como 0
Pares encontrados permanecem visíveis no tabuleiro
Validação de posições fora do tabuleiro
Placar atualizado a cada rodada e resultado final com o vencedor
Como jogar
Informe a quantidade de jogadores (1 ou 2) e o nome de cada um.
Escolha o modo: 1 para normal ou 2 para rápido.
Na sua vez, informe linha e coluna (começando em 1) da primeira e da segunda carta.
O programa mostra os valores das duas cartas. Se forem iguais, você marca 1 ponto e o par fica visível no tabuleiro.
O jogo termina quando todos os pares forem encontrados, e o placar final é exibido.

Exemplo do tabuleiro durante o jogo:

TABULEIRO DO JOGO DA MEMORIA:
   1  2  3  4  5  6
1 [0][0][7][0][0][0]
2 [0][0][0][0][0][0]
3 [0][0][7][0][0][0]
4 [0][0][0][0][0][0]
Como compilar e executar

Requer um compilador C++ (por exemplo, o g++). O projeto usa apenas bibliotecas padrão (iostream, string, cstdlib, ctime), então funciona em Windows, Linux e macOS.

bash
g++ TrabalhoM1PauloRafael.cpp -o jogo_da_memoria
./jogo_da_memoria

No Windows, execute jogo_da_memoria.exe.

Estrutura do código

O programa é dividido em sub-rotinas, cada uma responsável por uma tarefa do jogo:

Sub-rotina	Função
qtdJogadores	Lê a quantidade de jogadores
cadastroJogadores	Lê o nome dos jogadores
modoJogo	Lê o modo de jogo (normal ou rápido)
inicialiazarTabuleiro...	Zera a matriz do tabuleiro e a matriz de cartas visíveis
embaralharCartas...	Embaralha o vetor de cartas com rand()
preencherTabuleiro...	Distribui as cartas embaralhadas na matriz
exibirTabuleiro...	Desenha o tabuleiro no terminal
jogarNormal / jogarRapida	Controlam as rodadas, a pontuação e o fim do jogo

Os dois modos têm sub-rotinas próprias (sufixos Normal e Rapida), com tamanhos definidos por constantes no início do arquivo.

Tecnologias e conceitos
C++
Matrizes e vetores
Funções e procedimentos, com parâmetros por referência
Estruturas de repetição e condicionais
Números aleatórios (srand e rand)
Entrada e saída pelo terminal
Melhorias planejadas
Exibir o tabuleiro completo por alguns segundos no início da partida, antes de virar as cartas
Avisar quando o jogador escolher uma carta já descoberta
Permitir sair no meio do jogo e contar o número de jogadas de cada jogador
Passar a vez ao outro jogador apenas quando errar
Unificar os modos normal e rápido em um único conjunto de funções, para reduzir código repetido
Corrigir a condição de término do modo rápido, que deve encerrar com 9 pares
Limpar a tela entre as jogadas
Autores
Paulo Conceição
