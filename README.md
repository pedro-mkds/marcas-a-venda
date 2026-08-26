# Marcas à venda

Sites estáticos para apresentar as marcas Duke e Mais X, seus ativos digitais e os canais de contato para negociação.

## Estrutura

```text
.
|-- duke/    # meuduke.com.br e dukebank.com.br
|-- maisx/   # maisx.com.br
|-- index.html
`-- styles.css
```

Cada pasta é um site independente, sem banco de dados, instalação ou etapa de build. O catálogo na raiz serve apenas como visão geral do portfólio.

## Contato configurado

- WhatsApp: `+55 54 9671-7728`
- E-mail: `paulinhomarcondes@gmail.com`

## Publicação no Cloudways

O mesmo repositório pode ser conectado às duas aplicações do Cloudways. Em cada aplicação, faça a implantação do repositório na raiz de `public_html/` e altere o Webroot conforme a marca:

| Aplicação / domínio | Webroot |
| --- | --- |
| `meuduke.com.br` | `duke` |
| `dukebank.com.br` | `duke` |
| `maisx.com.br` | `maisx` |

Para a Duke, use `meuduke.com.br` como domínio principal e configure `dukebank.com.br` como domínio adicional ou redirecionamento para o principal. O HTML já declara `meuduke.com.br` como endereço canônico.

Passos resumidos:

1. Crie ou abra a aplicação no Cloudways.
2. Em **Deployment via Git**, gere a chave SSH.
3. No GitHub, adicione essa chave em **Settings > Deploy keys** do repositório.
4. No Cloudways, informe o endereço SSH do repositório e selecione a branch `main`.
5. Faça o deploy em `public_html/`.
6. Em **Application Settings**, altere o Webroot para `duke` ou `maisx`.
7. Associe o domínio e emita o certificado SSL.

Referências oficiais:

- [Implantação via Git no Cloudways](https://support.cloudways.com/en/articles/5124087-how-to-deploy-code-to-your-application-using-git-on-cloudways-flexible)
- [Alteração do Webroot](https://support.cloudways.com/en/articles/5124748-how-to-change-the-web-root-of-an-application)

## Visualização local

Abra `index.html`, `duke/index.html` ou `maisx/index.html` diretamente no navegador. Como os sites são estáticos, não é necessário iniciar um servidor.
