# ♿ Guia de Acessibilidade Digital e IHC - Grupo 4

[![MkDocs](https://img.shields.io/badge/MkDocs-Material-526CFE?style=for-the-badge&logo=markdown)](https://squidfunk.github.io/mkdocs-material/)
[![Acessibilidade](https://img.shields.io/badge/WCAG-2.2-005A9C?style=for-the-badge&logo=w3c)](https://www.w3.org/WAI/standards-guidelines/wcag/)

Bem-vindo ao repositório oficial da documentação viva do **Grupo 4** para a disciplina de **Interação Humano-Computador (IHC)** da Universidade de Brasília (UnB - FGA), ministrada pela Profa. Rejane Figueiredo.

Este projeto tem como objetivo central a construção de um **Guia Prático de Acessibilidade Digital**. Nele, unimos os princípios teóricos de Fatores Humanos (Modelos Mentais e Carga Cognitiva), o rigor técnico internacional da WCAG 2.2 e a base legal brasileira fundamentada pela **ABNT NBR 17225:2025**.


# ♿ Guia de Acessibilidade Digital e IHC - Grupo 4

[![Acesse a Documentação Viva](https://img.shields.io/badge/Documenta%C3%A7%C3%A3o_Viva-Acesse_Aqui-10b981?style=for-the-badge&logo=githubpages&logoColor=white)](https://unb-ihc.github.io/IHC_2026.1_Grupo04/)

## 🌐 Link de Acesso Direto
👉 **[Clique aqui para acessar o Guia de Acessibilidade Digital e o Checklist Interativo](https://unb-ihc.github.io/IHC_2026.1_Grupo04/)**

---

## 📋 A Ferramenta: Checklist Interativo de Auditoria

O principal artefato técnico desenvolvido neste repositório é o **Checklist Interativo de Verificação de IHC**. 

Sabemos que ferramentas de varredura automática (como Lighthouse, WAVE e ASES) capturam, em média, apenas **30% a 40%** das barreiras reais de acessibilidade em um código front-end. O restante exige uma inspeção humana rigorosa. Para solucionar isso, desenvolvemos uma ferramenta de auditoria interativa (via HTML/JS encapsulada no MkDocs) que permite a um avaliador realizar o pente-fino de qualquer interface.

O nosso Checklist está dividido em 3 blocos estratégicos:

1. **Estrutura Global e Semântica da Aplicação:** Focado no "Backstage" do código. Avalia tags estruturais do HTML5 puro, configuração de idioma (`lang`), links de salto ocultos e a sanidade da árvore de elementos (DOM) para leitores de tela.
2. **Conteúdo, Compreensão e Formulários:** Focado na clareza cognitiva. Avalia o uso de linguagem simples, rótulos de formulários (`<label>`), previsão e gestão de erros amigáveis, e o uso de tags robustas de acessibilidade (`WAI-ARIA`).
3. **Gerenciamento Perceptivo, Mídias e Teclado:** Focado em "Frontstage" (UI/UX). Avalia o contraste visual, o redimensionamento nativo da tela (zoom), pausas em animações e, fundamentalmente, se 100% da interface é operável de forma autônoma apenas através do teclado (sem armadilhas de foco).

**Como funciona:** À medida que o avaliador marca os critérios aprovados, a ferramenta calcula e atualiza dinamicamente uma barra de progresso. Ao final, ela emite o diagnóstico do sistema: **Risco Crítico de Exclusão**, **Conformidade Parcial** ou a almejada **Conformidade Regular Alcançada**.

---

## 👥 Nossa Squad (Grupo 4)

A equipe foi estruturada de forma cross-funcional, onde cada integrante aplica a sua especialidade na construção deste ecossistema analítico.

<table align="center">
  <tr>
    <td align="center">
      <img src="docs/img/rodrigo.jpg" width="120px;" style="border-radius: 50%;" alt="Foto do Rodrigo"/><br>
      <b>Rodrigo Henrique</b><br>
      <i>Líder / UX Architect</i>
    </td>
    <td align="center">
      <img src="https://via.placeholder.com/120" width="120px;" alt="Foto do Davi"/><br>
      <b>Davi Severiano</b><br>
      <i>Engenharia Normativa</i>
    </td>
    <td align="center">
      <img src="https://via.placeholder.com/120" width="120px;" alt="Foto do Daniel"/><br>
      <b>Daniel Lira</b><br>
      <i>Infra. e Ferramentas</i>
    </td>
    <td align="center">
      <img src="https://via.placeholder.com/120" width="120px;" alt="Foto do Antônio"/><br>
      <b>Antônio Lucas</b><br>
      <i>Auditoria UI / Acessibilidade</i>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://via.placeholder.com/120" width="120px;" alt="Foto do Enzo"/><br>
      <b>Enzo Menalli</b><br>
      <i>Design Empático e Personas</i>
    </td>
    <td align="center">
      <img src="docs/img/149fba7c-400d-47da-9dcc-22ab1416add5.jpg" width="120px;" alt="Foto do Paulo Ferreira"/><br>
      <b>Paulo Ferreira Filho</b><br>
      <i>Analista de Semântica Web</i>
    </td>
    <td align="center">
      <img src="https://via.placeholder.com/120" width="120px;" alt="Foto do Paulo Vitor"/><br>
      <b>Paulo Vitor Gomes</b><br>
      <i>UX Researcher / Dados</i>
    </td>
    <td align="center">
      </td>
  </tr>
</table>


---

## 🚀 Como rodar o projeto localmente

Se você deseja contribuir ou rodar a documentação deste repositório na sua máquina, siga os passos:

1. Clone o repositório:
   ```bash
   git clone [https://github.com/SEU_USUARIO/ihc_2026.1_grupo04.git](https://github.com/SEU_USUARIO/ihc_2026.1_grupo04.git)
