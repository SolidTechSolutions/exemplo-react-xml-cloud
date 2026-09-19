# 🇧🇷 SolidSign API - Front-end de Exemplo: Assinatura XML/XAdES em Nuvem/HSM (React)

Este projeto é a contrapartida visual do back-end [`exemplo-integracao-xml-cloud`](https://github.com/SolidTechSolutions/exemplo-integracao-xml-cloud). Reaproveita a lógica de campos e parâmetros da tela **Assinar XML (Nuvem/HSM)** do Portal SolidSign, simplificada: sem login, sem i18n e sem múltiplos node IDs/nomes/namespaces por documento (o back-end de exemplo aceita apenas um de cada, aplicado a todos os arquivos enviados).

## Como funciona

Este front-end fala com o back-end de exemplo local (`POST /api/xml/sign/form`, CORS liberado), que repassa `authorization`/`baseUrl`/`cloudCredentials`, assina, baixa os `.xml` resultantes e devolve um único `.zip` pronto pra download.

## Pré-requisitos

1. Rode o back-end [`exemplo-integracao-xml-cloud`](https://github.com/SolidTechSolutions/exemplo-integracao-xml-cloud) localmente (`mvn spring-boot:run`, porta padrão `8080`).
2. Tenha um token JWT válido e as credenciais do seu provedor de HSM/nuvem (URL, token de acesso e UUID do certificado).
3. Saiba o nome (e, se houver, o namespace) do nó XML que deve ser assinado no(s) seu(s) documento(s).

## Rodando

```bash
npm install
npm run dev
```

Abra `http://localhost:5173`, preencha o formulário e assine.

---

# 🇬🇧 SolidSign API - Example Front-end: Cloud/HSM XML/XAdES Signing (React)

This project is the visual counterpart to the [`exemplo-integracao-xml-cloud`](https://github.com/SolidTechSolutions/exemplo-integracao-xml-cloud) backend. It reuses the field logic from the Portal SolidSign **Sign XML (Cloud/HSM)** screen, simplified: no login, no i18n and no multiple node IDs/names/namespaces per document (the example backend only accepts one of each, applied to every uploaded file).

## How it works

This front-end talks to the local example backend (`POST /api/xml/sign/form`, CORS enabled), which forwards `authorization`/`baseUrl`/`cloudCredentials`, signs, downloads the resulting `.xml` files and returns a single ready-to-download `.zip`.

## Prerequisites

1. Run the [`exemplo-integracao-xml-cloud`](https://github.com/SolidTechSolutions/exemplo-integracao-xml-cloud) backend locally (`mvn spring-boot:run`, default port `8080`).
2. Have a valid JWT token and your cloud/HSM provider credentials (URL, access token and certificate UUID).
3. Know the name (and namespace, if any) of the XML node that must be signed in your document(s).

## Running

```bash
npm install
npm run dev
```

Open `http://localhost:5173`, fill in the form and sign.
