# Automação de Processamento de Notas Fiscais (Power Automate)

**O Problema:** Armazenamento manual de notas fiscais de serviço na pasta da tesouraria, exigindo renomeação individual de arquivos (formato "NF [número]-[data]") e processamento de até 200 documentos por período, gerando alto risco de erro humano e perda de tempo operacional.

## A Solução
Desenvolvimento de um fluxo de automação (RPA) utilizando **Power Automate Desktop** para capturar, renomear e organizar automaticamente as Notas Fiscais de Serviço (NFS-e), garantindo padronização para futura integração com SAP e eliminando tarefas repetitivas.

---

## Funcionalidades da Automação

O robô executa as seguintes etapas no fluxo de trabalho:

### 1. Interação Web e Captura
* Inicia o navegador (Microsoft Edge) e acessa o portal da Prefeitura.
* Realiza a navegação automática para localizar as notas fiscais pendentes.

### 2. Padronização de Arquivos
* Identifica os arquivos baixados.
* Renomeia automaticamente cada arquivo seguindo a regra de negócio estrita: **"NF [número]-[data]"**.

### 3. Organização de Diretórios
* Salva os arquivos renomeados na pasta correta da Tesouraria.
* Move os arquivos originais para a pasta de "Processados" (`...\ENVIO DOCS-PREFEITURA\Processados`), mantendo o diretório de entrada limpo e organizado.

---

## Stack Tecnológico

* **Ferramenta:** Microsoft Power Automate Desktop.
* **Ambiente:** Integração Web (Portal Prefeitura) e Sistema de Arquivos (File System).
* **Navegador:** Microsoft Edge.

---

## Benefícios e Impacto

* **Eficiência:** Eliminação do processo manual de baixar e renomear 200+ notas fiscais.
* **Compliance:** Garantia de que 100% dos arquivos estão no padrão de nomenclatura correto, evitando erros operacionais e perda de documentos.
* **Foco Estratégico:** Liberação da equipe de tesouraria para focar em análises financeiras ao invés de trabalho repetitivo.

---

## Estrutura do Fluxo (Low-Code)

O fluxo foi desenhado utilizando ações visuais do Power Automate:

1.  **Launch New Microsoft Edge:** Abertura do portal da prefeitura.
2.  **Get Files in Folder:** Leitura dos arquivos brutos no diretório local.
3.  **Loop (For Each):** Iteração sobre cada nota fiscal.
4.  **Rename/Move Files:** Aplicação da lógica de nomenclatura e arquivamento.
5.  **UI Automation:** Preenchimento de campos e cliques em botões de upload/download no portal.

---

**Status do Projeto:** Concluído ✅
