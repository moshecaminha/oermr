# OERMR — Observatório Econômico Regional

> Plataforma pública oficial do **SindiEmpresas** que reúne indicadores econômicos, cadastros empresariais e análises da **Região Metropolitana do Recife** e **Mata Sul / Litoral Sul** de Pernambuco.

🌐 **Acesse**: [https://SEU-USUARIO.github.io/oermr/](https://SEU-USUARIO.github.io/oermr/)

---

## 🎯 O que é

O OERMR é uma plataforma de inteligência econômica que consolida dados oficiais e cadastros públicos de **21 municípios pernambucanos** (14 RMR + 7 Mata Sul/Litoral Sul) em uma interface única e acessível.

### Recursos principais

- 🗺️ **Mapa satélite interativo** com bolhas proporcionais por município
- 📊 **Indicadores oficiais em tempo real** (IBGE, ANTAQ, MTE, MDIC)
- 🏛️ **Cards dos polos econômicos**: Suape (90 empresas, R$ 74,5 Bi) e Porto Digital (541 empresas, R$ 7,4 Bi)
- 🔍 **Canal de Negócios B2B** — busca por setor, município, tag
- 📈 **Rankings e análises comparativas** RMR vs Mata Sul
- 💼 **Editais e licitações** dos principais portais oficiais
- 📄 **Relatório executivo PDF** auto-gerado
- 🔄 **Varredura massiva** de empresas via Casa dos Dados (Receita Federal)

### Fontes oficiais

| Fonte | Dado |
|---|---|
| **IBGE / SIDRA** | CEMPRE, PNAD-C, PIB Municipal, Estimativa de População |
| **ANTAQ** | Movimentação portuária mensal |
| **MTE / CAGED** | Empregos formais |
| **MDIC / ComexStat** | Comércio exterior |
| **Suape Oficial** | Cadastro de empresas do complexo industrial |
| **Porto Digital / Softex-PE** | Balanço anual do distrito de inovação |
| **Receita Federal** (via Casa dos Dados) | Cadastros empresariais (CNPJ) |

---

## 🚀 Como atualizar a base de empresas

A plataforma carrega automaticamente o arquivo `empresas-base.json` ao abrir. Para atualizar:

1. **Localmente**, na sua máquina, abra a plataforma e rode a **Varredura Massiva** (Admin ⚙ → Configurações)
2. Aguarde a varredura concluir (5-10 min)
3. Vá em **Backup → Baixar JSON**
4. Renomeie o arquivo baixado para `empresas-base.json`
5. Faça commit do novo arquivo neste repositório (substitui o anterior)
6. Em ~2 minutos, todos os usuários veem a base atualizada

```bash
# Via Git
git add empresas-base.json
git commit -m "Atualização base: $(date +%Y-%m-%d)"
git push
```

---

## 🛠️ Estrutura

```
oermr/
├── index.html              # Aplicação principal (HTML+CSS+JS standalone)
├── empresas-base.json      # Base de empresas (carregada automaticamente)
└── README.md               # Este arquivo
```

A aplicação é **100% client-side**: sem backend, sem banco de dados externo. Funciona offline depois de carregada.

---

## 🔐 Acesso administrativo

Botão **⚙** no canto inferior esquerdo da página.

- **Usuário**: `admin`
- **Senha**: `sindiempresas2026`

Permite:
- Configurar API key da Casa dos Dados
- Rodar varredura massiva
- Exportar/importar base
- Aprovar cadastros pendentes
- Limpar cache

---

## 📝 Licença

Este projeto é mantido pelo **SindiEmpresas** como serviço público gratuito à comunidade empresarial pernambucana.

Os dados consolidados são de fontes oficiais públicas. As empresas listadas têm origem em cadastros públicos da Receita Federal e curadorias oficiais (Suape, Porto Digital).

---

**Contato**: SindiEmpresas · contato@sindiempresas.org.br
