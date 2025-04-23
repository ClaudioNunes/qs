# Laboratório de Gerenciamento de Defeitos

![banner](https://img.shields.io/badge/Qualidade%20de%20Software-Defect%20Management-blue)

Mini‑site **HTML + CSS + JavaScript puro** criado para que estudantes de graduação em Computação pratiquem **Gerenciamento de Defeitos** em um ambiente controlado e divertido. Todas as funcionalidades contêm _bugs_ intencionais que precisam ser identificados, registrados e (opcionalmente) corrigidos.

---

## 🎯 Objetivos Didáticos

1. **Identificar** defeitos através de técnicas de teste (caixa‑preta, partição de equivalência, valores‑limite, teste exploratório etc.).
2. **Registrar** cada defeito de forma padronizada (descrição, passos para reprodução, severidade, prioridade, evidências).
3. **Classificar & Priorizar** para selecionar o que deve ser corrigido primeiro.
4. **Reproduzir / Confirmar** o defeito em diferentes ambientes ou navegadores.
5. **Corrigir** o código‑fonte e **validar** a correção com novos testes.
6. **Fechar** o ciclo registrando versão de correção, autor da correção e verificador.

> Dica para instrutores: integre este fluxo a ferramentas como **GitHub Issues**, **Jira**, ou planilhas compartilhadas.

---

## 🗂️ Estrutura do Repositório

| Caminho                               | Descrição                                                  |
|---------------------------------------|------------------------------------------------------------|
| `buggy_defect_management_site.html`   | Página única com todas as funcionalidades bugadas.         |
| `README.md`                           | Este arquivo — instruções e objetivos.                     |

> Caso deseje separar o CSS/JS em arquivos externos, sinta‑se livre para fazê‑lo; os bugs continuarão funcionando 😉.

---

## 🚀 Como Executar

### 1. Abrir Diretamente no Navegador
```bash
# Clone o repositório
$ git clone https://github.com/<SEU_USUARIO>/defect‑management‑lab.git
$ cd defect‑management‑lab

# Basta abrir o arquivo HTML
$ start buggy_defect_management_site.html   # Windows
$ open buggy_defect_management_site.html    # macOS
```

### 2. Servidor Local (recomendado para evitar restrições de CORS)
```bash
# Python ≥3.7
$ python -m http.server 8000
# Navegue até http://localhost:8000/buggy_defect_management_site.html
```

### 3. GitHub Pages
1. Vá em **Settings ▸ Pages** e aponte para o branch principal.
2. O site ficará disponível em `https://<SEU_USUARIO>.github.io/defect‑management‑lab/buggy_defect_management_site.html`.

---

## 🧩 Funcionalidades e Pistas de Bugs

| Seção | Habilidade de Teste em Foco | Exemplo de Cenário de Teste |
|-------|-----------------------------|-----------------------------|
| **Calculadora Bugada** | Entradas inválidas / precisão | Somar `1.5 + 1.5` ou `"a" + 2` |
| **Lista de Tarefas Bugada** | Manipulação de coleção / contadores | Adicionar 3 itens, remover o 2º e verificar contagem |
| **Formulário Bugado** | Validação de campos | Enviar e‑mails sem `@`, idade negativa ou vazia |
| **Busca Bugada** | Busca, case‑sensitive, estado da UI | Pesquisar `computador` (minúsculo) ou limpar busca |

<details>
<summary>⚠️ Spoiler – Lista de Bugs Internos</summary>

* **Calculadora**: uso de `parseInt` causa truncamento; falta `isNaN` check.
* **Todo**: `splice(index, index)` remove múltiplos itens; contagem incorreta.
* **Formulário**: regex permissivo, não valida idade ≥0.
* **Busca**: filtro case‑sensitive; resultados "fantasma" ao buscar vazio.

</details>

---

## 📝 Roteiro Sugerido de Atividade (para Alunos)

1. **Exploração** – Navegue por todas as seções tentando entradas diversas.
2. **Registro** – Para cada defeito encontrado, crie um artefato (Issue, card ou linha de planilha) com:
   - Passos para reproduzir
   - Resultado esperado × obtido
   - Evidência (print, gif, vídeo)
   - Severidade & prioridade
3. **Classificação** – Agrupe defeitos similares, priorize correções críticas.
4. **Correção** – Faça _fork_ do repositório, corrija ao menos **um** defeito e envie _pull request_.
5. **Validação Cruzada** – Avalie a correção de outro grupo/colega.
6. **Relatório Final** – Entregue lista de defeitos, evidências, PRs e lições aprendidas.

---

## 🤝 Contribuindo

Pull requests são bem‑vindos! Para alterações de grande porte, abra primeiro uma *issue* para discutir o que você gostaria de mudar.

---

## 📜 Licença

Distribuído sob a licença **MIT**. Consulte `LICENSE` para mais detalhes.

