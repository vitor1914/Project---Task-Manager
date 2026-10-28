 <div align="center">

# Controle de Projetos e Tarefas | Project & Task Manager

**Organize projetos, acompanhe tarefas e monitore prazos no Google Sheets.**

**Organize projects, track tasks, and monitor deadlines in Google Sheets.**

![Google Sheets](https://img.shields.io/badge/Google%20Sheets-Planilha-34A853?style=for-the-badge&logo=googlesheets&logoColor=white)
![Google Apps Script](https://img.shields.io/badge/Google%20Apps%20Script-Automa%C3%A7%C3%A3o-4285F4?style=for-the-badge&logo=googleappsscript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Languages](https://img.shields.io/badge/Language-PT--BR%20%7C%20EN-0A66C2?style=for-the-badge)

</div>

---

# 🇧🇷 Português

## 📋 Sobre o projeto

O **Controle de Projetos e Tarefas** é uma solução desenvolvida com Google Sheets, JavaScript e Google Apps Script para organizar projetos, gerenciar atividades, acompanhar prazos e monitorar o progresso do trabalho em uma única planilha.

A automação cria abas estruturadas, configura listas suspensas, aplica formatação visual e utiliza fórmulas para calcular indicadores de acompanhamento.

O projeto pode ser utilizado para organização pessoal, estudos, atividades profissionais, desenvolvimento de software e acompanhamento de projetos de portfólio.

## 🖼️ Demonstração visual

### Painel de controle

![Painel de controle](https://placehold.co/1200x500/174A35/FFFFFF?text=Painel+de+Controle%0AProject+Management+Dashboard)

*Imagem ilustrativa. Substitua por uma captura de tela real do painel após executar o script.*

### Controle de projetos e tarefas

![Controle de projetos e tarefas](https://placehold.co/1200x500/217346/FFFFFF?text=Controle+de+Projetos+e+Tarefas%0AProjects+and+Tasks+Tracker)

*Imagem ilustrativa da organização de projetos, atividades, prioridades e prazos.*

## ✨ Funcionalidades

- **Painel de controle:** indicadores gerais para acompanhar projetos e tarefas.
- **Cadastro de projetos:** nome, categoria, descrição, datas, status, prioridade, link e observações.
- **Gerenciamento de tarefas:** organização de atividades vinculadas a projetos.
- **Progresso automático:** cálculo do total de tarefas, tarefas concluídas e percentual de conclusão dos projetos.
- **Identificação de atrasos:** sinalização de tarefas vencidas que ainda não foram concluídas ou canceladas.
- **Listas suspensas:** padronização dos status, prioridades e categorias.
- **Visão diária:** consulta das tarefas com vencimento na data atual.
- **Lista de prazos:** organização das tarefas pela data de vencimento.
- **Histórico de alterações:** registro de mudanças de status realizadas diretamente na planilha.
- **Controle de horas:** registro de horas previstas e realizadas.
- **Formatação visual:** cabeçalhos destacados, cores, filtros e congelamento da primeira linha.

## 📊 Estrutura da planilha

| Aba | Descrição |
|---|---|
| `Painel` | Indicadores gerais e acompanhamento |
| `Projetos` | Cadastro e progresso dos projetos |
| `Tarefas` | Cadastro e gerenciamento das atividades |
| `Hoje` | Tarefas com prazo para o dia atual |
| `Calendário` | Lista de tarefas organizada por prazo |
| `Listas` | Valores utilizados nas listas suspensas |
| `Histórico` | Registro das alterações de status |

## 🛠️ Tecnologias utilizadas

| Tecnologia | Aplicação |
|---|---|
| Google Sheets | Interface e armazenamento dos dados |
| Google Apps Script | Automação da planilha |
| JavaScript | Implementação da lógica |
| Fórmulas do Sheets | Cálculos e indicadores |
| Validação de dados | Listas suspensas e padronização |

## 🚀 Instalação e configuração

### Requisitos

- Uma conta Google.
- Acesso ao Google Sheets.
- Acesso ao editor do Google Apps Script.

### Passo a passo

1. Acesse o [Google Sheets](https://sheets.google.com).
2. Crie uma nova planilha em branco.
3. Abra o menu **Extensões → Apps Script**.
4. Apague o código inicial do editor.
5. Cole o código JavaScript completo do projeto.
6. Clique em **Salvar**.
7. No seletor de funções, escolha `criarControleProjetos`.
8. Clique em **Executar**.
9. Autorize as permissões solicitadas pelo Google, se necessário.
10. Volte à planilha e verifique as abas criadas.

### ⚠️ Atenção antes de executar novamente

A função `criarControleProjetos()` limpa o conteúdo das abas com os nomes utilizados pelo projeto antes de reconstruir a estrutura.

Execute inicialmente em uma planilha nova. Antes de executar novamente em uma planilha já utilizada, faça uma cópia de segurança para evitar perder dados.

## 📖 Como utilizar

1. Abra a aba `Projetos`.
2. Cadastre o nome, a categoria, as datas, o status e a prioridade de cada projeto.
3. Acesse a aba `Tarefas`.
4. Cadastre as atividades e associe cada uma ao projeto correspondente.
5. Informe os prazos, as prioridades e as horas previstas, quando aplicável.
6. Atualize o status das tarefas conforme o trabalho evoluir.
7. Consulte o `Painel` para acompanhar os indicadores.
8. Utilize `Hoje` e `Calendário` para consultar os prazos.

## 📈 Regras de cálculo

### Progresso das tarefas

O percentual é estimado com base no status:

- Concluída: 100%.
- Em andamento: 50%.
- Outros status: 0%.

### Progresso dos projetos

O progresso é calculado pela proporção entre tarefas concluídas e tarefas cadastradas para o projeto.

### Identificação de atrasos

Uma tarefa é sinalizada como atrasada quando seu prazo é anterior à data atual e seu status não é `Concluída` nem `Cancelada`.

## ⚠️ Limitações conhecidas

- A aba `Hoje` apresenta tarefas com vencimento na data atual.
- A aba `Calendário` é uma lista ordenada por prazo, e não uma grade de calendário mensal.
- O histórico registra alterações de status feitas diretamente na planilha. Alterações produzidas por fórmulas ou outros scripts não acionam automaticamente o gatilho simples `onEdit`.
- O script não envia notificações por e-mail nem cria eventos no Google Calendar.
- O funcionamento das fórmulas pode depender da configuração regional da planilha. Caso ocorram erros, verifique a localidade e os separadores aceitos pelo Google Sheets.

## 🔧 Personalização

O projeto pode ser adaptado para diferentes rotinas e necessidades.

É possível modificar as categorias e os status na aba `Listas`, personalizar cores, adicionar campos e ajustar as fórmulas no Apps Script.

Recomenda-se manter uma cópia de segurança antes de realizar modificações.

## 🎯 Aplicações práticas

- Organização de projetos pessoais.
- Gerenciamento de tarefas diárias.
- Planejamento de estudos.
- Acompanhamento de projetos de programação.
- Controle de atividades de portfólio.
- Organização de entregas e prazos.
- Registro de horas de trabalho.

## 📄 Licença

Nenhuma licença específica foi definida para este projeto. Para permitir a distribuição sob termos formais, adicione um arquivo `LICENSE` ao repositório.

---

# 🇺🇸 English

## 📋 About the project

**Project & Task Manager** is a solution built with Google Sheets, JavaScript, and Google Apps Script to organize projects, manage tasks, track deadlines, and monitor progress in a single spreadsheet.

The automation creates structured tabs, configures dropdown lists, applies visual formatting, and uses formulas to calculate tracking indicators.

The project can be used for personal organization, studying, professional activities, software development, and portfolio project tracking.

## 🖼️ Visual preview

### Dashboard

![Project management dashboard](https://placehold.co/1200x500/174A35/FFFFFF?text=Project+Management+Dashboard)

*Illustrative image. Replace it with a real screenshot of the dashboard after running the script.*

### Projects and tasks

![Project and task tracker](https://placehold.co/1200x500/217346/FFFFFF?text=Projects+and+Tasks+Tracker)

*Illustrative image of project organization, tasks, priorities, and deadlines.*

## ✨ Features

- **Dashboard:** overview of projects and tasks.
- **Project register:** name, category, description, dates, status, priority, link, and notes.
- **Task management:** activities linked to their respective projects.
- **Automatic progress calculations:** total tasks, completed tasks, and project completion percentage.
- **Overdue detection:** flags past-due tasks that have not been completed or canceled.
- **Dropdown lists:** standardized statuses, priorities, and categories.
- **Daily view:** displays tasks due on the current date.
- **Deadline list:** tasks organized by due date.
- **Change history:** logs status changes made directly in the spreadsheet.
- **Time tracking:** records estimated and actual hours.
- **Visual formatting:** styled headers, colors, filters, and a frozen first row.

## 📊 Spreadsheet structure

| Tab | Description |
|---|---|
| `Painel` | General indicators and tracking |
| `Projetos` | Project register and progress |
| `Tarefas` | Task registration and management |
| `Hoje` | Tasks due today |
| `Calendário` | Tasks sorted by deadline |
| `Listas` | Values used by dropdown lists |
| `Histórico` | Status-change log |

## 🛠️ Technologies

| Technology | Purpose |
|---|---|
| Google Sheets | User interface and data storage |
| Google Apps Script | Spreadsheet automation |
| JavaScript | Application logic |
| Google Sheets formulas | Calculations and indicators |
| Data validation | Dropdown lists and standardized values |

## 🚀 Installation and setup

### Requirements

- A Google account.
- Access to Google Sheets.
- Access to the Google Apps Script editor.

### Step-by-step instructions

1. Open [Google Sheets](https://sheets.google.com).
2. Create a new blank spreadsheet.
3. Open **Extensions → Apps Script**.
4. Remove the starter code from the editor.
5. Paste the complete JavaScript project code.
6. Click **Save**.
7. Select the `criarControleProjetos` function.
8. Click **Run**.
9. Grant the requested Google permissions if prompted.
10. Return to the spreadsheet and check the generated tabs.

### ⚠️ Before running the script again

The `criarControleProjetos()` function clears the contents of tabs with the names used by this project before rebuilding the structure.

Run it in a new spreadsheet first. Before running it again in a spreadsheet containing data, create a backup to avoid losing information.

## 📖 How to use

1. Open the `Projetos` tab.
2. Enter each project's name, category, dates, status, and priority.
3. Open the `Tarefas` tab.
4. Add tasks and link each one to the appropriate project.
5. Enter deadlines, priorities, and estimated hours where applicable.
6. Update task statuses as work progresses.
7. Review the `Painel` dashboard for tracking indicators.
8. Use `Hoje` and `Calendário` to review deadlines.

## 📈 Calculation rules

### Task progress

The percentage is estimated from the task status:

- Completed: 100%.
- In progress: 50%.
- Other statuses: 0%.

### Project progress

Project progress is calculated as the number of completed tasks divided by the total number of registered tasks for that project.

### Overdue detection

A task is flagged as overdue when its deadline is earlier than the current date and its status is neither `Concluída` nor `Cancelada`.

## ⚠️ Known limitations

- The `Hoje` tab displays tasks due on the current date.
- The `Calendário` tab is a deadline-sorted list, not a monthly calendar grid.
- The history log records status changes made directly in the spreadsheet. Changes made by formulas or other scripts do not automatically trigger the simple `onEdit` trigger.
- The script does not send email notifications or create Google Calendar events.
- Formula behavior may depend on spreadsheet locale settings. If errors occur, check the locale and separators supported by Google Sheets.

## 🔧 Customization

The project can be adapted to different workflows and needs.

You can change categories and statuses in the `Listas` tab, customize colors, add fields, and adjust formulas in Apps Script.

Keeping a backup before making changes is recommended.

## 🎯 Use cases

- Personal project organization.
- Daily task management.
- Study planning.
- Software development project tracking.
- Portfolio management.
- Deliverable and deadline tracking.
- Work-hour tracking.

## 📄 License

No specific license has been defined for this project. To distribute it under formal terms, add a `LICENSE` file to the repository.

---

<div align="center">

**Desenvolvido com Google Sheets e Google Apps Script**  
**Built with Google Sheets and Google Apps Script**

</div>