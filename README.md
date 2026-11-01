[readme_desconto_composto.md](https://github.com/user-attachments/files/34229907/readme_desconto_composto.md)
# 📉 Calculadora de Desconto Composto Comercial

Calculadora educacional, em um único arquivo HTML, para resolver problemas de **desconto composto comercial** (desconto "por fora") com **resolução passo a passo**.

Desenvolvida pelo **Prof. Laerte Bemm** — Departamento de Matemática, Universidade Estadual de Maringá (UEM).

---

## 📌 Sobre o projeto

Descontar um título (duplicata, nota promissória etc.) significa antecipar o seu recebimento antes do vencimento, pagando uma taxa pela antecipação. Nesta calculadora:

| Símbolo | Significado |
|---------|-------------|
| **FV** | Valor nominal (valor de face / resgate no vencimento) |
| **VC** | Valor comercial (valor efetivamente recebido) |
| **VD** | Valor do desconto, $VD = FV - VC$ |
| **i** | Taxa de desconto por período |
| **n** | Prazo de antecipação, em **meses** |
| **iᶠ** | Taxa efetiva da operação |

No **desconto composto comercial**, a taxa $i$ incide sucessivamente, período a período, sobre o próprio valor do título. Por isso a taxa efetiva cobrada é **sempre maior** que a taxa de desconto anunciada.

---

## 🧮 Fórmulas utilizadas

$$VC = FV \cdot (1 - i)^n$$

$$VD = FV - VC$$

$$FV = \frac{VD}{1 - (1 - i)^n}$$

$$i = 1 - \left(\frac{VC}{FV}\right)^{1/n}$$

$$i_f = \frac{i}{1 - i}$$

---

## 🗂️ Tipos de problema

A calculadora possui cinco modos, selecionáveis por botões:

| Tipo | Dados de entrada | Resultados |
|------|------------------|------------|
| **1** | FV, i, n (meses inteiros) | VC, VD, iᶠ — com opção de comparar com o desconto racional composto (por dentro) |
| **2** | FV, i, n (meses) | VC, VD, iᶠ |
| **3** | FV, VC, n (meses) | i, iᶠ |
| **4** | i | iᶠ |
| **5** | VD, i, n (meses) | FV, VC, iᶠ |

Em todos os casos, o resultado é apresentado em etapas: dados, fator de desconto, valores calculados e verificação da taxa efetiva.

---

## ✏️ Exemplos

**Tipo 1** — Título de R$ 2.000,00, antecipado 3 meses, taxa de 2,5% a.m.

- Fator de desconto: $(1 - 0{,}025)^3 \approx 0{,}926859$
- VC ≈ **R$ 1.853,72**
- VD ≈ **R$ 146,28**
- iᶠ ≈ **2,5641% a.m.**

**Tipo 3** — FV = R$ 1.000,00, VC = R$ 880,00, n = 4 meses

- i ≈ **3,15% a.m.**
- iᶠ ≈ **3,25% a.m.**

**Tipo 4** — Taxa de desconto de 24,75% a.a.

- iᶠ ≈ **32,89% a.a.**

**Tipo 5** — VD = R$ 4.780,98, i = 4,5% a.m., n = 7 meses

- Calcula FV e VC isolando FV na fórmula de VD.

---

## 🚀 Como usar

### Localmente

1. Baixe o arquivo `desconto-composto-comercial.html` (ou clone o repositório):
   ```bash
   git clone https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git
   ```
2. Abra o arquivo no navegador (duplo clique ou `Arquivo → Abrir`).
3. Escolha o tipo de problema, preencha os campos e clique em **▶ Calcular**.

Não há instalação, build nem dependências: basta um navegador moderno.

### Online com GitHub Pages

1. No repositório, vá em **Settings → Pages**.
2. Em **Build and deployment**, selecione **Deploy from a branch**.
3. Escolha a branch `main` e a pasta `/ (root)` e clique em **Save**.
4. Se quiser que o site abra direto na calculadora, renomeie o arquivo para `index.html`.
5. Após alguns instantes, a calculadora estará disponível em:
   ```
   https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/
   ```

---

## ⚠️ Validações e observações

- A taxa de desconto deve estar **entre 0% e 100%** (exclusive).
- No **Tipo 1**, o prazo deve ser um número **inteiro** de meses.
- Nos **Tipos 3 e 5**, o prazo deve ser positivo e, no Tipo 3, **VC deve ser menor que FV**.
- Os campos aceitam **vírgula ou ponto** como separador decimal (ex.: `2,5` ou `2.5`).
- Todos os prazos e taxas devem estar na **mesma unidade de tempo** (meses e % a.m., por exemplo).
- A ferramenta tem finalidade **didática**; não substitui o cálculo oficial de uma instituição financeira.

---

## 🛠️ Tecnologias

- HTML5
- CSS3 (layout responsivo com Grid e Flexbox)
- JavaScript puro (*vanilla*), sem bibliotecas externas

---

## 📁 Estrutura sugerida do repositório

```
├── index.html     # a calculadora (ou desconto-composto-comercial.html)
├── README.md      # este arquivo
└── LICENSE        # licença (opcional)
```

---

## 🔗 Projeto relacionado

Esta calculadora segue a mesma estrutura visual da **Calculadora de Desconto Comercial Simples**, que trata o desconto por fora com taxa aplicada linearmente sobre o valor nominal.

---

## 👤 Autoria

**Prof. Laerte Bemm**
Departamento de Matemática — Universidade Estadual de Maringá (UEM)

---

## 📄 Licença

Defina a licença de sua preferência (por exemplo, [MIT](https://opensource.org/licenses/MIT)) e adicione o arquivo `LICENSE` ao repositório. Para uso estritamente acadêmico, você também pode indicar aqui: *"Material educacional de uso livre, com citação da autoria."*
