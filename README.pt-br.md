# Flight Ops: Analisador de Telemetria MAVLink

*[Read this in English / Leia em Inglês](README.md)*

## 📌 Visão geral
Este repositório contém uma ferramenta proprietária desenvolvida em Python voltada para o **Monitoramento de Operações de Voo e Análise Pós-Voo**. O sistema extrai, processa e gera visualizações de dados brutos de telemetria MAVLink (arquivos `.tlog`) gerados pelo QGroundControl e simulações ArduPilot SITL.

Na aviação agrícola autônoma de grande escala, depender exclusivamente de interfaces gráficas convencionais pode atrasar diagnósticos críticos. Este script automatiza a análise de parâmetros essenciais de voo — como a aderência à altitude da missão e quedas de tensão no banco de baterias —, garantindo troubleshooting rápido, preciso e o cumprimento das normas de segurança durante as operações de pista.

## ⚙️ Funcionalidades
*   **Leitura Nativa MAVLink:** Utiliza a biblioteca `pymavlink` para ler arquivos `.tlog` diretamente das Estações de Controle de Solo (GCS).
*   **Extração Direcionada de Dados:** Isola pacotes críticos para a segurança da missão, incluindo `GLOBAL_POSITION_INT` (Altitude, Posição, Proa) e `BATTERY_STATUS` (Gerenciamento de energia e quedas de tensão).
*   **Geração Automatizada de Gráficos:** Emprega `matplotlib` e `pandas` para renderizar gráficos de performance, auxiliando Despachantes de Voo e Operadores na tomada de decisão em campo.

## 🛠️ Pré-requisitos
*   Python 3.8+
*   QGroundControl (para a geração do arquivo `.tlog`)
*   ArduPilot SITL (Software In The Loop) para a simulação de voo

## 🚀 Como executar
1. Certifique-se de que o arquivo `.tlog` necessário esteja no diretório `/data`.
2. Instale as dependências requeridas do Python:
   ```bash
   pip install -r requirements.txt

## ⚠️ Direitos Autorais e Licença
© 2026 Douglas Mardegan Colodete. Todos os Direitos Reservados.

Este projeto e seu código-fonte são estritamente proprietários. É terminantemente proibida a cópia, distribuição, modificação, exibição pública ou uso não autorizado deste código, por qualquer meio. Este repositório tem como finalidade exclusiva servir como demonstração de portfólio profissional.
