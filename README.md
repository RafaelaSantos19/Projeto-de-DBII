# 🧭 AcessiTransporte — Mobilidade com Inclusão

**Desenvolvido por:** *Rafaela Santos da Costa*  
**Trabalho de Conclusão de Curso (TCC)**  
**Tema:** Aplicativo de transporte acessível para pessoas com deficiência ou mobilidade reduzida  
**Linguagens:** HTML, CSS, JavaScript (Front-end) e PHP com SQLite (Back-end)

---

## 💙 Sobre o Projeto

O **AcessiTransporte** nasceu de uma vivência pessoal e de uma grande necessidade:  
as dificuldades que pessoas com deficiência enfrentam ao tentar utilizar aplicativos de transporte convencionais.

> “Muitas vezes, as corridas são canceladas, os veículos não são adaptados ou os motoristas não estão preparados para oferecer o suporte necessário.”

O projeto busca mudar essa realidade através de **tecnologia, empatia e acessibilidade**.  
O AcessiTransporte oferece uma plataforma simples e funcional onde o usuário pode:

- Solicitar corridas adaptadas;
- Informar necessidades especiais (cadeira de rodas, auxílio de embarque, etc.);
- Ver simulações de preço e rota em tempo real;
- Salvar e visualizar histórico de corridas;
- Contatar o SAC para dúvidas ou suporte.

---

## 🎯 Objetivo

Proporcionar **autonomia e dignidade** na mobilidade de pessoas com deficiência física, garantindo uma experiência:
- **Inclusiva**, com interface acessível e recursos assistivos;
- **Responsiva**, funcionando bem em qualquer dispositivo;
- **Funcional**, com front-end e back-end integrados;
- **Educacional**, servindo como base de estudos e conscientização sobre acessibilidade digital.

---

## 🧩 Estrutura do Sistema

tcc-completo/
│
├── index.html             # Página inicial (introdução e navegação)
├── motorista.html          # Página do motorista (dados e corridas)
├── passageiro.html         # Página do passageiro (perfil e preferências)
├── corrida.html            # Página de solicitação de corrida com mapa e simulação
├── sac.html                # Central de Atendimento com envio e histórico
├── contatos.html           # Informações de contato e suporte
├── sobre.html              # História da autora e propósito do projeto
│
├── public/
│   ├── css/styles.css      # Estilos gerais (acessível e responsivo)
│   └── assets/             # Ícones, logotipo e imagens do sistema
│
├── src/
│   └── pages/              # Scripts JavaScript de cada página
│       ├── corrida-page.js
│       ├── motorista-page.js
│       ├── passageiro-page.js
│       ├── sac-page.js
│
└── api/                    # Back-end em PHP com SQLite
├── api.php             # Rotas REST
├── controllers/        # Controladores das requisições
├── repositories/       # Repositórios de dados (SQLite)
├── setup.db            # Banco de dados SQLite
└── services/           # Lógica de negócio

---

## ⚙️ Tecnologias Utilizadas

**Front-end:**
- HTML5, CSS3 e JavaScript (ES6+)
- Leaflet.js — mapa interativo e simulação de rota
- Armazenamento local (`localStorage`) para histórico offline
- Design responsivo e acessível

**Back-end:**
- PHP 8+
- SQLite (banco de dados leve)
- Estrutura MVC simples (Controller / Repository / Service)
- API RESTful com endpoints como `/api/rides` e `/api/sac`

---

## 🧠 Recursos de Acessibilidade

- **Modo alto contraste**
- **Leitura por voz** (compatível com narradores do navegador)
- **Foco visível e navegação por teclado**
- **Integração planejada com VLibras**
- **Textos claros, botões grandes e linguagem simples**

Esses recursos tornam o sistema mais inclusivo para pessoas com deficiência visual, auditiva ou motora.

---

## 🚗 Simulação de Corrida

Na página **Corrida**, o usuário pode:
1. Clicar no mapa para definir origem e destino;
2. Calcular o preço com base na distância;
3. Marcar necessidades específicas (cadeira de rodas, auxílio, etc.);
4. Simular a rota com um veículo em movimento no mapa;
5. Salvar ou enviar a corrida para o backend.

> 💡 O preço é calculado com base na distância (R$ 2,50 por km)  
> + Taxas adicionais de acessibilidade (R$ 8,00 para cadeira de rodas, R$ 5,00 para auxílio de embarque).  
> O sistema também adiciona uma variação dinâmica para simular o comportamento real de demanda.

---

## 💬 SAC — Central de Atendimento

A página **SAC** foi desenvolvida com foco na experiência do usuário:
- Validação em tempo real;
- Contagem de caracteres e limite máximo de texto;
- Envio para o backend (`/api/sac`);
- Salvamento local caso o servidor esteja offline;
- Histórico de mensagens com opção de download (JSON).

---

## 💁‍♀️ Sobre a Autora

Sou **Rafaela Santos da Costa**, cadeirante, e desenvolvi este projeto como parte do meu TCC.  
Minha vivência com a falta de acessibilidade em transportes foi o ponto de partida para criar uma solução que une tecnologia e empatia.

> “Já tive corridas canceladas ao informarem que eu usava cadeira de rodas.  
>  Foi quando percebi que o problema não era a falta de carro, e sim a falta de inclusão.”  

O **AcessiTransporte** é minha forma de transformar essa realidade, provando que a tecnologia pode — e deve — incluir todos.

---

## 🧭 Como Executar o Projeto

### 🔹 Executar localmente (com backend PHP)
1. Instale o **XAMPP** ou outro servidor PHP.
2. Copie a pasta do projeto para o diretório `htdocs`.
3. Inicie o servidor Apache.
4. Acesse [http://localhost/tcc-completo/index.html](http://localhost/tcc-completo/index.html)

### 🔹 Executar apenas o front-end
1. Abra o arquivo `index.html` diretamente no navegador.  
2. O sistema funcionará em modo offline, salvando os dados no `localStorage`.

---

## 🧩 Endpoints principais da API

| Método | Rota          | Descrição                         |
|:-------|:---------------|:----------------------------------|
| `GET`  | `/api/rides`   | Lista as corridas registradas     |
| `POST` | `/api/rides`   | Registra uma nova corrida         |
| `POST` | `/api/sac`     | Envia mensagem ao suporte         |

---

## 🪄 Funcionalidades extras

- Histórico de corridas locais e no servidor  
- Reenvio automático de SAC pendentes  
- Tema responsivo e ajustável  
- Interface modular (páginas separadas e scripts próprios)

---

## 🧱 Licença

Projeto acadêmico desenvolvido para fins educacionais.  
Pode ser usado como referência em estudos, trabalhos de inclusão digital e desenvolvimento acessível.  
Créditos obrigatórios: **Rafaela Santos da Costa — AcessiTransporte (2025)**

---

> 💬 *“Transformar barreiras em caminhos — esse é o propósito do AcessiTransporte.”*
