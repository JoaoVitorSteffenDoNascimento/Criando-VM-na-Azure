# Desafio DIO: Criando uma Máquina Virtual na Azure

Este projeto faz parte do laboratório da DIO sobre os benefícios da nuvem, com foco na criação de máquinas virtuais no Microsoft Azure.

## 🧠 Objetivo

Aplicar na prática os conhecimentos adquiridos sobre máquinas virtuais, utilizando o portal da Azure para criar uma VM Windows Server 2022 e documentar todo o processo.


## 🛠️ Etapas Realizadas

### 1. Acesso ao Portal
- Acesse o [portal da Azure](https://portal.azure.com) com sua conta.

### 2. Criação da Máquina Virtual
- No campo de busca, digite **"Máquinas Virtuais"**.
- Clique em **"Criar" > "Máquina virtual do Azure"**.

### 3. Configuração da Instância
- **Nome da VM**: `myVM`
- **Imagem**: `Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2`
- **Região**: `Brazil South`
- **Tamanho**: padrão sugerido pelo portal

### 4. Conta de Administrador
- **Usuário**: `azureuser`
- **Senha**: senha segura com no mínimo 12 caracteres

### 5. Regras de Porta de Entrada
- **Permitir portas selecionadas**:
  - RDP (3389)
  - HTTP (80)

### 6. Validação e Criação
- Clique em **"Examinar + Criar"**
- Após validação, clique em **"Criar"**

---

## 🔗 Conexão com a VM

- Vá até a VM criada e clique em **"Conectar > RDP"**
- Baixe o arquivo `.rdp` e abra no seu computador
- Use o usuário e senha configurados para acessar

---

## 🌐 Instalação do IIS (Servidor Web)

Dentro da VM, abra o PowerShell e execute:

```powershell
Install-WindowsFeature -name Web-Server -IncludeManagementTools
