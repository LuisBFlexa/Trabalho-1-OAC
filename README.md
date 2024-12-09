# Montador Assembly MIPS para Formato MIF

Este projeto consiste em um montador (assembler) desenvolvido em Assembly MIPS que converte código fonte Assembly MIPS (.asm) para o formato MIF (Memory Initialization File), implementado como parte da disciplina de Organização e Arquitetura de Computadores da Universidade de Brasília (UnB).

## 📋 Descrição

O programa é capaz de converter arquivos fonte Assembly MIPS (.asm) em arquivos no formato MIF, gerando dois arquivos de saída separados:
- Um para a seção .text
- Um para a seção .data

O montador suporta um conjunto específico de instruções MIPS, incluindo o grupo básico obrigatório e o conjunto de instruções do Grupo 3.

### Conjunto de Instruções Suportadas

#### Grupo Básico (Obrigatório)
- `lw $t0, OFFSET($s3)`
- `add/sub/and/or/nor/xor $t0, $s2, $t0`
- `addi/andi/ori/xori $t2, $t3, -10`
- `add $t0, $t2, 1000`
- `sw $t0, OFFSET($s3)`
- `j LABEL`
- `jr $t0`
- `jal LABEL`
- `jalr $t1`
- `beq/bne $t1, $zero, LABEL`
- `slt $t1, $t2, $t3`
- `lui $t1, 0xXXXX`
- `addu/subu $t1, $t2, $t3`
- `sll/srl $t2, $t3, 10`
- `sllv $t1, $t2, $t3`
- `mult $t1, $t2`
- `div $t1, $t2`
- `mfhi/mflo $t1`

#### Grupo 3
- `lbu $t2, OFFSET($s5)`
- `bnel $t1, $t5, LABEL`
- `msub $t1, $t2`
- `tne $t5, $t6`
- `eret`
- `ll $t5, OFFSET($s1)`
- `madd $t2, $t3`
- `lh $t1, OFFSET($s5)`
- `movn $t1, $t2, $t4`
- `b LABEL`

## 🚀 Como Usar

1. Certifique-se de ter o MARS (MIPS Assembler and Runtime Simulator) instalado em sua máquina
2. Clone este repositório
3. Abra o arquivo fonte (.asm) no MARS
4. Execute o programa fornecendo um arquivo de entrada .asm
5. O programa gerará dois arquivos de saída .mif (um para .text e outro para .data)

### Formato de Entrada
- Arquivos fonte em Assembly MIPS com extensão .asm
- O código deve estar organizado nas seções .text e .data
- Suporte para valores imediatos em decimal e hexadecimal (0xXXXXXXXX)

### Formato de Saída
- Arquivos no formato MIF (Memory Initialization File)
- Mantém o mesmo nome do arquivo de entrada, alterando apenas a extensão para .mif
- Geração de dois arquivos separados para as seções .text e .data

## ⚙️ Características

- Interface para entrada de arquivos e saída (visual ou terminal)
- Suporte completo aos registradores inteiros da CPU
- Tratamento de máscaras de registradores
- Suporte a números inteiros sinalizados e não-sinalizados
- Tratamento de valores hexadecimais de 32 bits
- Tratamento de erros para opcodes desconhecidos e instruções inexistentes

## 📚 Estrutura do Projeto

```
.
├── README.md
├── src/
│   └── montador.asm      # Arquivo fonte principal
├── examples/
│   ├── input.asm         # Exemplo de arquivo de entrada
│   ├── output_text.mif   # Exemplo de saída para seção .text
│   └── output_data.mif   # Exemplo de saída para seção .data
└── docs/
    └── relatorio.pdf     # Relatório de desenvolvimento e análise
```

## 👥 Equipe

- Enzo Bittencourt Luz
- Giovanna Amaral Franceschi
- Luis Antonio Benjamim Flexa

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 🎯 Objetivos do Projeto

- Familiarização com a linguagem Assembly MIPS
- Desenvolvimento de metodologias de aplicações eficientes e otimizadas
- Compreensão do funcionamento de sistemas computacionais
- Desenvolvimento de capacidade de observação, análise e compreensão das metodologias de organização e arquitetura de computadores

---
Desenvolvido como projeto da disciplina de Organização e Arquitetura de Computadores - UnB
