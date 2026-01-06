# 🏛️ Plugin: Institutional Access Bar Integration

## 🎯 Contexto Técnico
Ao desenvolver soluções WordPress para o setor público, surgiu a necessidade de criar um sistema modular para integração de elementos de identidade visual obrigatórios. Inserir esse tipo de código diretamente no tema gerava problemas de manutenção e risco de quebra durante atualizações.

## 🛠️ Solução Arquitetural
Desenvolvi este plugin para desacoplar a lógica de integração da camada visual do tema, seguindo princípios de modularidade e manutenibilidade.

### Diferenciais Técnicos:
- **Hook Strategy:** Utiliza `wp_body_open` (WordPress 5.2+) para injeção moderna de scripts
- **Z-Index Management:** CSS injetado dinamicamente para controle de camadas
- **Performance Optimization:** Carregamento assíncrono via `defer` sem bloquear renderização
- **Filter Hooks:** Implementa filtros para customização (ex: URL do script, estilos CSS)

![Preview da barra](./screenshot.jpeg)

## 📁 Estrutura do Código
```php
// Exemplo da arquitetura modular
add_action('wp_body_open', 'inst_adicionar_barra');
add_action('wp_head', 'inst_estilos_barra');
add_filter('inst_barra_script_url', 'customizar_url_script');