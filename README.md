# Plugin WordPress - Barra do Governo Federal

Plugin para integração automática da Barra de Identidade Visual do Governo Federal no topo de qualquer tema WordPress, sem necessidade de alterar arquivos do tema.

## Objetivo

Garantir a inclusão padronizada da barra institucional exigida em portais públicos, evitando:

- Alterações diretas no `header.php`
- Quebras após atualização de tema
- Problemas de manutenção em múltiplos sites

## Implementação

A barra é inserida através do hook nativo:

- `wp_body_open` (WordPress 5.2+)

O tema não precisa ser modificado.

## Características Técnicas

- Injeção via hook nativo
- Script carregado com `defer`
- CSS aplicado dinamicamente para controle de sobreposição (`z-index`)
- Estrutura desacoplada do tema

## Contexto de Uso

Desenvolvido para ambientes institucionais do setor público.

![Preview da barra](./screenshot.jpeg)