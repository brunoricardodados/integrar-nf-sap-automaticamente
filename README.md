# Automação de Processamento de Notas Fiscais (Power Automate)

[cite_start]**O Problema:** Armazenamento manual de notas fiscais de serviço na pasta da tesouraria, exigindo renomeação individual de arquivos (formato "NF [número]-[data]") e processamento de até 200 documentos por período, gerando alto risco de erro humano e perda de tempo operacional[cite: 736, 737, 738].

## A Solução
[cite_start]Desenvolvimento de um fluxo de automação (RPA) utilizando **Power Automate Desktop** para capturar, renomear e organizar automaticamente as Notas Fiscais de Serviço (NFS-e), garantindo padronização para futura integração com SAP e eliminando tarefas repetitivas[cite: 745, 746].

---

## Funcionalidades da Automação

O robô executa as seguintes etapas no fluxo de trabalho:

### 1. Interação Web e Captura
* [cite_start]Inicia o navegador (Microsoft Edge) e acessa o portal da Prefeitura (ex: Barueri)[cite: 759].
* Realiza a navegação automática para localizar as notas fiscais pendentes.

### 2. Padronização de Arquivos
* Identifica os arquivos baixados.
* [cite_start]Renomeia automaticamente cada arquivo seguindo a regra de negócio estrita: **"NF [número]-[data]"**[cite: 748].

### 3. Organização de Diretórios
* [cite_start]Salva os arquivos renomeados na pasta correta da Tesouraria[cite: 749].
* [cite_start]Move os arquivos originais para a pasta de "Processados" (`...\ENVIO DOCS-PREFEITURA\Processados`), mantendo o diretório de entrada limpo e organizado[cite: 759].

---

## Stack Tecnológico

* [cite_start]**Ferramenta:** Microsoft Power Automate Desktop[cite: 734].
* **Ambiente:** Integração Web (Portal Prefeitura) e Sistema de Arquivos (File System).
* **Navegador:** Microsoft Edge.

---

## Benefícios e Impacto

* [cite_start]**Eficiência:** Eliminação do processo manual de baixar e renomear 200+ notas fiscais[cite: 738, 751].
* [cite_start]**Compliance:** Garantia de que 100% dos arquivos estão no padrão de nomenclatura correto, evitando erros operacionais e perda de documentos[cite: 742, 752].
* [cite_start]**Foco Estratégico:** Liberação da equipe de tesouraria para focar em análises financeiras ao invés de trabalho repetitivo[cite: 753].

---

## Estrutura do Fluxo (Low-Code)

O fluxo foi desenhado utilizando ações visuais do Power Automate:

1.  **Launch New Microsoft Edge:** Abertura do portal da prefeitura.
2.  **Get Files in Folder:** Leitura dos arquivos brutos no diretório local.
3.  **Loop (For Each):** Iteração sobre cada nota fiscal.
4.  **Rename/Move Files:** Aplicação da lógica de nomenclatura e arquivamento.
5.  [cite_start]**UI Automation:** Preenchimento de campos e cliques em botões de upload/download no portal
---

[cite_start]**Status do Projeto:** Concluído.