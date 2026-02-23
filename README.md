# Plugin WordPress - Barra do Governo Federal

Plugin desenvolvido para integrar a Barra do Governo Federal brasileiro no topo de qualquer tema WordPress, sem acoplamento direto ao tema.

## Objetivo

Permitir a inclusão padronizada da barra institucional exigida em portais públicos, evitando:

- Alterações diretas no header.php
- Quebras durante atualização de tema
- Dificuldade de manutenção em múltiplos sites

## Como funciona

O plugin injeta a barra utilizando o hook nativo:

- wp_body_open (WordPress 5.2+)

Isso garante compatibilidade com boas práticas modernas do WordPress.

## Características Técnicas

- Injeção via hook nativo
- Script carregado com defer
- CSS aplicado dinamicamente para controle de sobreposição (z-index)
- Filtros disponíveis para customização (URL do script e estilos)

## Contexto de Uso

Criado para ambientes institucionais do setor público, onde a padronização visual e a separação entre lógica e apresentação são essenciais para manutenção e governança.