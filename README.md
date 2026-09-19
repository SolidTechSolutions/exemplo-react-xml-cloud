# 🇧🇷 SolidSign API - Front-end de Exemplo: Assinatura XML com HSM/Nuvem (React)

## Como funciona

Este front-end chama `POST /api/xml/sign/form` (`http://localhost:8080` por padrão) no back-end de exemplo, enviando as credenciais do HSM/nuvem (`hsmUrl`, `hsmToken`, `uuidCert`). O back-end assina o XML e devolve um `.zip`.

## Requisitos

Rode este back-end de exemplo localmente:

- **Java**: [`exemplo-integracao-xml-cloud`](https://github.com/SolidTechSolutions/exemplo-integracao-xml-cloud)

- Um token JWT válido (`POST /solidsign/auth/token`)

## Como rodar

```bash
npm install
npm run dev
```

Abra `http://localhost:5173`, preencha o formulário e envie.

## Variáveis do formulário

| Campo | Significado | Default |
|---|---|---|
| `baseUrl` | URL base da SolidSign API | `https://www.solidsign.com.br` |
| `authorization` | Token JWT (Bearer) | (vazio) |
| `hsmUrl / hsmToken / uuidCert` | Credenciais do HSM/PSC de nuvem | (vazio) |
| `documents` | XML(s) a assinar | (vazio) |
| `profile` | Perfil de assinatura PBAD/ETSI | `ADRB` |
| `hashAlgorithm` | Algoritmo de hash | `SHA256` |
| `signaturePackaging` | Empacotamento XML-DSig | `ENVELOPED` |
| `canonicalizationMethod` | Método de canonicalização | `EXCLUSIVE` |
| `signatureNodeName` | Nome do nó a assinar | `document` |
| `signatureNodeNamespace` | Namespace do nó (opcional) | (vazio) |
| `signatureNodeId` | ID do nó, tem prioridade sobre nome/namespace (opcional) | (vazio) |
| `isRemoveXPathExclusionFilter` | Remover filtro de exclusão XPath | `false` |
| `isRemoveNamespacePrefixFromNodeNames` | Remover prefixo de namespace dos nomes de nó | `false` |
| `isSignKeyInfo` | Assinar o KeyInfo | `false` |

---

# 🇬🇧 SolidSign API - Example Front-end: XML Signing with HSM/Cloud (React)

## How it works

This front-end calls `POST /api/xml/sign/form` (`http://localhost:8080` by default) on the example backend, sending the HSM/cloud credentials (`hsmUrl`, `hsmToken`, `uuidCert`). The backend signs the XML and returns a `.zip`.

## Requirements

Run this example backend locally:

- **Java**: [`exemplo-integracao-xml-cloud`](https://github.com/SolidTechSolutions/exemplo-integracao-xml-cloud)

- A valid JWT token (`POST /solidsign/auth/token`)

## Running

```bash
npm install
npm run dev
```

Open `http://localhost:5173`, fill in the form and submit.

## Form fields

| Field | Meaning | Default |
|---|---|---|
| `baseUrl` | SolidSign API base URL | `https://www.solidsign.com.br` |
| `authorization` | JWT (Bearer) token | (empty) |
| `hsmUrl / hsmToken / uuidCert` | Cloud HSM/PSC credentials | (empty) |
| `documents` | XML(s) to sign | (empty) |
| `profile` | PBAD/ETSI signature profile | `ADRB` |
| `hashAlgorithm` | Hash algorithm | `SHA256` |
| `signaturePackaging` | XML-DSig packaging | `ENVELOPED` |
| `canonicalizationMethod` | Canonicalization method | `EXCLUSIVE` |
| `signatureNodeName` | Name of the node to sign | `document` |
| `signatureNodeNamespace` | Node namespace (optional) | (empty) |
| `signatureNodeId` | Node ID, takes priority over name/namespace (optional) | (empty) |
| `isRemoveXPathExclusionFilter` | Remove the XPath exclusion filter | `false` |
| `isRemoveNamespacePrefixFromNodeNames` | Remove the namespace prefix from node names | `false` |
| `isSignKeyInfo` | Sign the KeyInfo | `false` |
