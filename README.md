# Gerador de contratos a partir da proposta comercial

Lê o PDF de uma proposta (pedido de venda) e monta o contrato de prestação de serviços e fornecimento de material em `.docx`, com conferência campo a campo e histórico de versões.

> **O código e os modelos de contrato não são públicos.** Este repositório traz a arquitetura em [ESTRUTURA.md](ESTRUTURA.md).

## O problema

Cada contrato era remontado à mão a partir da proposta: copiar cliente, itens, valores e parcelas para um modelo do Word, ajustar cláusulas e conferir tudo de novo. Lento e sujeito a erro de digitação.

## A solução

1. O PDF da proposta é lido **pela posição do texto na página** (cliente, itens, totais, parcelas), e não por padrões frágeis de texto corrido.
2. O sistema sugere os campos do contrato e aponta o que depende de decisão humana.
3. A pessoa confere campo a campo numa prévia que usa as mesmas regras do gerador.
4. O `.docx` sai a partir do modelo, preservando a formatação.
5. Cada contrato guarda versões, anexos e as diferenças entre elas.

Também é possível **incluir um modelo novo soltando um `.docx`** na tela: o sistema o converte para o padrão interno de campos.

## Decisões de engenharia

- **PHP 8 com SQLite e servidor embutido**: roda local com um duplo clique, sem instalar nada, e também em qualquer hospedagem PHP.
- **Leitura de PDF no navegador** (pdf.js) com reconstrução de linhas e células pelas coordenadas.
- **Edição de texto sem perder formatação**: a troca de trechos no `.docx` preserva negrito e sublinhado.
- **Extenso, datas e validação de CPF/CNPJ** em utilitários próprios e testados.

## Stack

PHP 8 · SQLite · JavaScript (pdf.js) · HTML · CSS · Git
