# Guia do Usuário — App Bit Energy

**Instalação e uso · Versão 1.0.0 (beta de campo) · Android**

Este guia é para o **técnico** que vai instalar o app no celular e usá-lo para
configurar os dispositivos Bit Energy em campo.

---

## O que este app faz

O app Bit Energy serve para **configurar o dispositivo** que você instalou no
equipamento de refrigeração ou climatização. Pelo **Bluetooth** do celular, você diz ao
dispositivo:

- em **qual rede Wi-Fi** do local ele deve se conectar, e
- **qual controlador** (Carel) ele está monitorando.

Depois disso, o dispositivo reinicia sozinho, entra na internet e passa a
aparecer no **Painel Bit Energy** ([painel.bitenergy.com.br](https://painel.bitenergy.com.br)), enviando os dados.

> Tudo é feito **por perto**, via Bluetooth. Você não precisa de cabo nem de conta/login para usar o app.

---

## Antes de começar, você vai precisar de

- Um **celular Android** (versão 7.0 ou mais nova).
- **Bluetooth ligado** no celular.
- Estar **perto** (poucos metros) do dispositivo Bit Energy.
- O **dispositivo já instalado e ligado** no equipamento, em **modo de
  configuração** (conforme o procedimento do equipamento).
- O **nome da rede Wi-Fi e a senha** do local.
- No caso do Hive-Link, saber **qual controlador** o dispositivo está ligado (ex.: Carel PJEZ ou
  Carel iJF).

---

## Parte 1 — Baixar e instalar o app *(só na primeira vez)*

### 1. Baixe o aplicativo

No **navegador do celular**, abra o link e baixe o arquivo. Recomendamos o primeiro (menor e serve para a maioria dos celulares):

| Arquivo | Para | Link |
|---|---|---|
| **`BitEnergy-v1.0.0-arm64.apk`** ⭐ | Celulares atuais (recomendado) | [Baixar](https://github.com/AlanMiranda-BR/bitenergy-app-android/releases/download/v1.0.0-beta/BitEnergy-v1.0.0-arm64.apk) |
| `BitEnergy-v1.0.0-universal.apk` | Qualquer celular (use na dúvida) | [Baixar](https://github.com/AlanMiranda-BR/bitenergy-app-android/releases/download/v1.0.0-beta/BitEnergy-v1.0.0-universal.apk) |

O arquivo cai na pasta **Downloads** do celular.

> ⚠️ **Não repasse o app pelo WhatsApp** — ele bloqueia esse tipo de arquivo.
> Use os links acima, ou Google Drive / e-mail.

### 2. Instale o app

1. Toque no arquivo **`.apk`** que você baixou (na pasta Downloads).
2. O Android pode avisar que **não pode instalar apps desta fonte**. Toque em
   **Configurações** e ative **“Permitir desta fonte”**. Volte.
3. Pode aparecer um aviso de que o app **não foi verificado**. Toque em
   **Mais detalhes → Instalar mesmo assim**.
4. Toque em **Instalar** e depois em **Abrir**.

> 💡 Em celulares **Xiaomi / MIUI / HyperOS** aparece uma verificação extra ao
> instalar — é normal, é só seguir as confirmações.

### 3. Na primeira vez que abrir

O app vai pedir permissão de **Bluetooth** e **Localização**. Toque em
**Permitir**. São necessárias para o celular encontrar o dispositivo — o app
**não usa** sua localização para mais nada.

---

## Parte 2 — Configurar um dispositivo *(o dia a dia)*

### Passo 1 — Deixe o dispositivo pronto

Com o dispositivo Bit Energy **ligado** no equipamento e em **modo de
configuração**, fique **perto** dele com o celular.

### Passo 2 — Encontre o dispositivo

Abra o app. A primeira tela é **“Dispositivos Bit Energy”** e ela já começa a
**procurar** automaticamente.

- Quando o dispositivo for encontrado, ele aparece na lista com um nome como
  **“HiveLink-…”**.
- **Toque no dispositivo** para começar.

> **Não apareceu?** Toque no ícone de **atualizar** (↻) no canto superior.
> Confirme que o Bluetooth está ligado, que você está perto e que o dispositivo
> está em modo de configuração.

### Passo 3 — Confira que é o aparelho certo

O app conecta e mostra um cartão **“Dispositivo”** com o **MAC** (um código como
`A0:F2:62:80:48:0C`). Confira que bate com a etiqueta do aparelho que você está
configurando.

### Passo 4 — Preencha os dados

| Campo | O que colocar |
|---|---|
| **Rede Wi-Fi (SSID)** | O nome da rede Wi-Fi do local |
| **Senha Wi-Fi** | A senha dessa rede |
| **Controlador conectado** | Escolha **Carel PJEZ** ou **Carel iJ (Modbus)** |

Há também uma seção **“Avançado (opcional)”** (Tenant, Broker MQTT, etc.).
**Normalmente deixe em branco** — só preencha se a equipe Bit Energy tiver
passado um valor específico para você (por exemplo, o **Tenant** do cliente).

> ℹ️ Qualquer campo deixado **em branco** usa o **valor padrão de fábrica** do dispositivo. Caso o roteador não esteja configurado com o **Wi-Fi** da Bit Energy, informe o **Wi-Fi e senha** do local — sem eles o aparelho pode não conseguir entrar na internet.

### Passo 5 — Envie a configuração

Toque em **“Configurar dispositivo”**. O app mostra:

1. **“Enviando configuração…”**
2. **“Salvando e reiniciando o dispositivo…”**

### Passo 6 — Pronto!

Aparece a tela verde **“Dispositivo configurado!”**.

O aparelho **reinicia** e, em cerca de **30 segundos**, conecta no Wi-Fi e passa a aparecer no **Painel Bit Energy**. Pode fechar o app ou tocar em **“Voltar ao início”** para configurar outro dispositivo.

---

## Parte 3 — Se algo der errado

| O que aparece / acontece | O que fazer |
|---|---|
| **O dispositivo não aparece** na lista | Chegue mais perto; confirme o Bluetooth ligado e o dispositivo em modo de configuração; toque em **atualizar** (↻). |
| **“Bluetooth indisponível…”** | Ligue o **Bluetooth** do celular e volte ao app. |
| **“Permissão de Bluetooth negada…”** | Vá em *Configurações do Android → Apps → Bit Energy → Permissões* e libere **Bluetooth** e **Localização**. |
| **“Não foi possível configurar”** | Toque em **“Tentar novamente”**. Confira Wi-Fi/senha e fique mais perto do aparelho. |
| **Configurou, mas não aparece no Painel** | Aguarde alguns minutos. Confira se o **Wi-Fi do local alcança** o ponto onde o aparelho está e se a **senha** está correta. |

---

## Precisa de ajuda?

Fale com a equipe **Bit Energy**. Ao pedir suporte, tenha em mãos:

- O **MAC** do dispositivo (aparece na tela de configuração).
- O **nome do local / cliente** e a **rede Wi-Fi** usada.
- Uma foto da mensagem de erro, se houver.

- **Painel:** [painel.bitenergy.com.br](https://painel.bitenergy.com.br)

---

*App Bit Energy 1.0.0 (beta de campo) · Guia válido para esta versão · Somente Android (7.0+).*
