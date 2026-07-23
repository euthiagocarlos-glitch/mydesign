# Simulado CAC — Prova Teórica (Registro • Tipo I)

Sistema simples para estudar a **prova teórica** do CAC (Certificado de
Registro / registro de tiro), voltado a **arma curta de uso permitido**
(revólver e pistola — **Tipo I**, categoria de **registro**, não porte).

Baseado na **Cartilha de Armamento e Tiro** (SAT/ANP – CONAT/DARM).

## Como usar

Abra o arquivo **`index.html`** no navegador do celular (ou toque duas vezes
para abrir). É um único arquivo, funciona **offline**, sem instalar nada.

Dica: no celular, use "Adicionar à tela de início" para virar um atalho.

## O que o sistema faz

- Monta uma prova com a **estrutura oficial (20 questões)**:
  - Normas de segurança — **6 questões**
  - Nomenclatura e funcionamento de peças — **6 questões**
  - Conduta no estande — **3 questões**
  - Legislação (Lei 10.826/03 e Decreto 5.123/04) — **5 questões**
- **Múltipla escolha** com seleção por toque.
- Botão **Corrigir** — mostra nota, aprovado/reprovado (mínimo **60% = 12/20**)
  e o acerto por seção, com a explicação de cada questão.
- Botão **🔄 Nova prova (renovar)** — sorteia **novas questões** de cada tema
  e embaralha as alternativas, girando o banco a cada rodada.
- Seletor de nível **Padrão / Difícil** no topo:
  - **Padrão** — questões de prova reais, parafraseadas, com cenários.
  - **Difícil** — raciocínio combinado, comparação entre conceitos próximos
    (ex.: *ação dupla* × *dupla ação*), análise de afirmativas (I, II, III),
    questões "assinale a INCORRETA" e itens numéricos de legislação.

## Bancos de questões

Há dois bancos independentes no `<script>`:
- `BANK` — nível **Padrão**.
- `BANK_HARD` — nível **Difícil**.

Ambos seguem a mesma estrutura oficial (6 / 6 / 3 / 5 = 20 questões).

## Editar / adicionar questões

Todas as questões ficam no objeto `BANK`, dentro do `<script>` em
`index.html`. Cada questão tem o formato:

```js
{ q:"enunciado", options:["correta", "errada", "errada", "errada"], e:"explicação" }
```

> A **primeira** alternativa (`options[0]`) é sempre a correta — o sistema
> embaralha a ordem na tela automaticamente. Basta manter esse padrão ao
> incluir novas perguntas.
