# Árvores do Aretê · Búzios

<!-- project-badges:start -->
![WebGIS: OpenLayers](https://img.shields.io/static/v1?label=WebGIS&message=OpenLayers&color=forestgreen&style=flat)
![Exportação: qgis2web](https://img.shields.io/static/v1?label=Exporta%C3%A7%C3%A3o&message=qgis2web&color=blue&style=flat)
[![Autoria: Rebeca Diniz Moura](https://img.shields.io/static/v1?label=Autoria&message=Rebeca%20Diniz%20Moura&color=8b5cf6&style=flat)](https://github.com/RebecaGis)
<!-- project-badges:end -->


Mapa web interativo de árvores do empreendimento Aretê, em Búzios, com camadas geográficas exportadas do QGIS.

## Conteúdo

- Camadas `Arvores_Comuns` e `Arvores_EN`, com estilos e legendas próprios.
- Consulta aos atributos das feições pelo mapa.
- Interface cartográfica baseada em OpenLayers e qgis2web.

Os nomes das camadas reproduzem os arquivos publicados. A classificação técnica e o significado de EN devem ser confirmados com a documentação do levantamento.

## Executar localmente

Requer Python 3 para servir os arquivos estáticos:

```bash
git clone https://github.com/RebecaGis/Buzios_Arete_Supress-o.git
cd Buzios_Arete_Supress-o
python -m http.server 8000
```

Abra http://localhost:8000. O servidor local não altera a publicação existente. Recursos externos e mapas base podem depender de internet.

## Estrutura

| Caminho | Finalidade |
| --- | --- |
| `index.html` | Página do mapa |
| `layers/` | Dados e configuração das camadas |
| `styles/` | Estilos e legendas |
| `resources/` | Bibliotecas JavaScript e folhas de estilo |
| `webfonts/` | Fontes utilizadas pela interface |

## Manutenção e dados

Mantenha os caminhos relativos entre as pastas ao copiar o mapa. Alterações nos dados devem ser feitas a partir de uma base validada, com conferência de atributos, sistema de referência e estilos antes de publicar.

O repositório contém a exportação web; não inclui projeto QGIS de origem. Data do levantamento, metodologia, autoria dos dados e condições de reutilização precisam ser documentadas antes de usos técnicos externos.
