# Estrutura do projeto

Mapa das pastas e arquivos de código. O código-fonte não é publicado neste repositório
(é software de uso interno de uma empresa real); aqui fica a arquitetura.

```text
├── app/   # leitura da proposta, montagem do contrato, geração do .docx, histórico
│   ├── contrato/
│   │   ├── Exigencias.php
│   │   ├── Montagem.php
│   │   ├── Redacao.php
│   │   └── TextosEditados.php
│   ├── docx/
│   │   ├── DocxModelo.php
│   │   ├── Previa.php
│   │   └── RubricaWord.php
│   ├── historico/
│   │   ├── Banco.php
│   │   └── Historico.php
│   ├── modelos/
│   │   ├── CadastroModelos.php
│   │   ├── Clausulas.php
│   │   ├── ImportadorModelo.php
│   │   └── Trechos.php
│   ├── proposta/
│   │   ├── LeitorBling.php
│   │   └── Linhas.php
│   ├── util/
│   │   ├── Datas.php
│   │   ├── Documento.php
│   │   ├── Extenso.php
│   │   └── Texto.php
│   ├── Api.php
│   ├── Config.php
│   └── inicio.php
├── public/   # tela e API
│   ├── assets/
│   │   ├── css/
│   │   │   └── app.css
│   │   └── js/
│   │       ├── lib/
│   │       │   ├── pdf.min.js
│   │       │   └── pdf.worker.min.js
│   │       ├── api.js
│   │       ├── app.js
│   │       ├── contrato.js
│   │       ├── estado.js
│   │       ├── modelos.js
│   │       ├── pdf.js
│   │       ├── previa.js
│   │       ├── util.js
│   │       └── visualizador.js
│   ├── api.php
│   ├── index.php
│   └── roteador.php
├── scripts/
│   ├── conferir_ui.ps1
│   ├── gerar_fixtures.ps1
│   └── rubricar.ps1
└── tests/
    ├── pagina_extrair.html
    ├── pagina_fluxo_curto.html
    ├── pagina_fluxo_edicao.html
    ├── pagina_fluxo_importar.html
    ├── pagina_fluxo_ui.html
    ├── rodar.php
    ├── testes_exigencias.php
    └── testes_modelo_novo.php
```

## Tamanho (linhas, sem bibliotecas de terceiros)

| Linguagem | Linhas |
|---|---:|
| PHP | 9.217 |
| JavaScript | 2.940 |
| CSS | 673 |
| HTML | 471 |
| PowerShell | 250 |

_Arquivos: 48._
