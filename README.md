# 🧪 BrunoTest
![API Tests](https://github.com/LucioAmorim/BrunoTest/actions/workflows/api-tests.yml/badge.svg)

Projeto de testes de API utilizando **Bruno** como alternativa ao Postman.

---

## 📌 Sobre o Projeto

Este projeto demonstra a execução de testes automatizados de API com:
- Organização por tipo de teste (**smoke**)
- Separação por domínio (`user`, `login`)
- Configuração de ambiente (atualmente apenas `dev`)
- Execução via CLI (`bru run`)
- Integração com CI (GitHub Actions)

---

## 🚀 Execução dos Testes

Os testes são executados via pipeline no GitHub Actions.

👉 [Resultados da action](https://github.com/LucioAmorim/BrunoTest/actions/workflows/api-tests.yml)

---

## 🔐 Segurança

> ⚠️ **Importante**

Os dados como `baseUrl` e payloads estão expostos neste projeto **apenas para fins didáticos**.

Em um cenário real, o ideal é:

- Utilizar **GitHub Secrets** para dados sensíveis
- Evitar exposição de:
  - URLs de produção
  - Credenciais (login/senha)
  - Tokens de autenticação

---

## 🧪 Test Cases

### User - CreateUser

| Test Case   | Validation     | Expected Result |
|-------------|----------------|----------------|
| Create User | Status Code    | `200`          |
| Create User | Body Code      | `200`          |
| Create User | Message        | `'1001'`       |
| Create User | Response Time  | < 1000 ms      |

---

### Authentication - LoginSuccessfull

| Test Case           | Validation     | Expected Result                          |
|--------------------|----------------|------------------------------------------|
| Login Successfully | Status Code    | `200`                                    |
| Login Successfully | Body Code      | `200`                                    |
| Login Successfully | Message        | Contains `'logged in user session'`      |
| Login Successfully | Response Time  | < 1000 ms                                |

---

## 🧠 Tecnologias Utilizadas

- [Bruno CLI](https://www.usebruno.com/)
- GitHub Actions
- YAML (configuração de testes)

---


