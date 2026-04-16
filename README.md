# ⚡ Catálogo de Scooters Elétricas

Site de fichas técnicas para GitHub Pages — limpo, rápido e fácil de manter.

---

## 🚀 Como publicar no GitHub Pages

1. Crie um repositório no GitHub
2. Faça upload de **todos os arquivos** (mantendo a estrutura de pastas)
3. Vá em **Settings → Pages → Deploy from a branch → main → / (root)**
4. Em ~2 minutos o site estará em:  
   `https://SEU_USUARIO.github.io/NOME_DO_REPO/`

> O GitHub Pages roda Jekyll automaticamente — nenhuma instalação necessária.

---

## ✏️ Como adicionar uma nova scooter

**Só crie um arquivo `.md` novo na pasta `_scooters/`** — é só isso!

### Passo a passo

1. Vá até a pasta `_scooters/`
2. Crie um arquivo com o nome do modelo, ex: `nova-scooter.md`
3. Cole o template abaixo e preencha os dados
4. Faça commit — a scooter aparece automaticamente no catálogo

### Template para copiar

```markdown
---
nome: Nome Completo da Scooter
marca: Marca
ano: 2024
foto: https://link-para-a-foto.jpg

# Aparece no card principal
velocidade: "XX km/h"
autonomia: "XXX km"
peso: "XX kg"

badge: Destaque          # opcional — remova a linha se não quiser

descricao: >
  Descrição curta da scooter, aparece no detalhe.
  Pode ter duas linhas.

# Especificações — adicione ou remova campos livremente
specs:
  Motor: "500 W"
  Bateria: "48 V / 20 Ah"
  Autonomia: "até 60 km"
  Velocidade máxima: "35 km/h"
  Tempo de carga: "5 horas"
  Peso: "16 kg"
  Carga máxima: "120 kg"
  Aro do pneu: "10 polegadas"
  Resistência: "IPX5"
  Freio: "Disco dianteiro"
  # Adicione qualquer spec extra aqui!

# Peças de reposição — adicione quantas quiser, ou remova a seção
pecas:
  - nome: "Pneu 10\""
    codigo: SKU-001
    preco: "R$ 90,00"
  - nome: "Câmara de ar"
    codigo: SKU-002
    preco: "R$ 20,00"
---

## Observações

Escreva aqui qualquer texto em **Markdown** que quiser.
Aparece na seção de observações do detalhe.

- Dica de manutenção
- Compatibilidade com acessórios
- Avisos importantes
```

---

## 📁 Estrutura do projeto

```
.
├── _config.yml          ← configuração do Jekyll (não edite)
├── index.html           ← página do catálogo (não edite)
├── README.md            ← este arquivo
└── _scooters/           ← PASTA DAS SCOOTERS
    ├── xiaomi-mi-pro-2.md
    ├── segway-ninebot-max.md
    ├── kaabo-wolf-warrior.md
    └── sua-nova-scooter.md   ← adicione aqui!
```

---

## 🎨 Dicas rápidas

**Usar foto local em vez de URL:**
```yaml
foto: imagens/minha-scooter.jpg
```
(Crie a pasta `imagens/` na raiz do projeto)

**Cores do badge** — o badge aparece automático sobre a foto quando o campo existe:
```yaml
badge: Mais Vendida
badge: Novo
badge: Off-Road
badge: Promoção
```

**Testar localmente** (opcional — requer Ruby):
```bash
gem install bundler jekyll
jekyll serve
# Acesse http://localhost:4000
```
