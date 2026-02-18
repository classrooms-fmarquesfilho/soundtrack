# 🎵 Trilhas Sonoras

Trilhas sonoras geradas ao vivo com [TidalCycles](https://tidalcycles.org) para sessões de coding, aulas e projetos audiovisuais. Todas as trilhas são código aberto — você pode ouvir, modificar e redistribuir.


---

## 🗂️ Trilhas disponíveis

| Arquivo | Título | Estética | BPM | Uso |
|---|---|---|---|---|
| [`ainda-compila.tidal`](ainda-compila.tidal) | Ainda Compila | Ambient-Ethereal + Lo-fi + Glitch | 70 | Coding ao vivo, fundo de aula |

---

## 🛠️ Requisitos

- **[SuperCollider](https://supercollider.github.io/)** (>= 3.12) com **SuperDirt** instalado
- **[TidalCycles](https://tidalcycles.org/docs/getting-started/installation)** (>= 1.9)
- Editor: [VS Code + extensão TidalCycles](https://marketplace.visualstudio.com/items?itemName=tidalcycles.vscode-tidalcycles), Emacs, Vim ou Pulsar


## ▶️ Como usar

**1. Inicie o SuperCollider**

Se estiver usando uma interface de áudio externa:
```supercollider
s.options.inDevice = "<in-device>";
s.options.outDevice = "<out-device>";
s.reboot;
SuperDirt.start;
```

Se não precisar de input:
```supercollider
s.options.numInputBusChannels = 0;
s.reboot;
SuperDirt.start;
```

**2. Abra o arquivo no VS Code**

```bash
code ainda-compila.tidal
```

**3. Configure o VS Code para reconhecer `.tidal`**

No `settings.json` (`Cmd+Shift+P` → "Open User Settings JSON"):
```json
"files.associations": {
    "*.tidal": "haskell"
}
```

**4. Avalie a linha de BPM** (cursor na linha + `Cmd+Enter`):

```haskell
setcps (70/60/4)
```

**5. Entre com as camadas gradualmente**

Cada arquivo tem uma seção **"Ordem de entrada recomendada"** nos comentários. Use `Cmd+Enter` para avaliar blocos multilinhas — `Shift+Enter` avalia só a linha atual e vai gerar erros em patterns multilinhas.

**6. Para desligar camadas individualmente:**

```haskell
silence d1   -- silencia uma camada
hush         -- para tudo instantaneamente
```

---

## 🥁 Samples utilizados

As trilhas usam apenas samples confirmados no SuperDirt default:

| Sample | Uso |
|---|---|
| `bd` | Bumbo lo-fi |
| `linnhats` | Hi-hat ethereal e lo-fi com swing |
| `gretsch` | Snare fantasma |
| `pebbles` | Vinyl crackle |
| `cp` | Click de glitch |
| `glitch` | Textura digital |
| `superpiano` | Pad principal (synth nativo SuperDirt) |
| `supersaw` | Bass sustentado (synth nativo SuperDirt) |


---

## 🎨 Filosofia

**Código como composição** — o arquivo `.tidal` *é* a música. Modificar o código é compor.

**Textura como função** — as trilhas existem para sustentar foco, não para chamar atenção. O silêncio e o espaço são tão importantes quanto as notas.

**Abertura radical** — tudo aqui é para ser forkado, modificado e redistribuído. Se você criar uma variação, abra um PR.

---

## 🤝 Contribuindo

1. Fork o repositório
2. Crie um arquivo `.tidal` com sua trilha
3. Documente nos comentários: BPM, referências estéticas, ordem de entrada, samples usados
4. Abra um Pull Request

---

## 📜 Licença

[CC BY-SA 4.0](LICENSE) — use, modifique e distribua, inclusive comercialmente, mantendo atribuição e redistribuindo derivações sob a mesma licença.

---

*Feito no RN com TidalCycles, SuperDirt e muito café.*