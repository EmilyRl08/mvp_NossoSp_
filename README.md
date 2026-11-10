# Nosso SP 📰

O **Nosso SP** é um portal de notícias locais de São Paulo. Seu objetivo é permitir que moradores acompanhem acontecimentos de suas regiões, consultem notícias no mapa e interajam com as publicações.

## Tecnologias utilizadas

- Python e Django – Back-end.
- HTML, CSS e JavaScript – Interface.
- SQLite – Banco de dados.
- Geoapify – API de localização e geocodificação.
- Leaflet e OpenStreetMap – Exibição do mapa.

## Funcionalidades

- **Leitor:** visualizar notícias, pesquisar publicações, comentar, favoritar e solicitar cadastro como jornalista.
- **Jornalista:** criar notícias, adicionar título, conteúdo, imagem, tags, região, bairro e rua; salvar rascunhos e enviar matérias para aprovação.
- **Administrador:** analisar, aprovar, negar e excluir notícias, além de avaliar solicitações de novos jornalistas.
- **Mapa:** visualizar a localização das notícias utilizando a API Geoapify.

## Como executar o projeto

### 1. Abrir a pasta do projeto

Abra o terminal na pasta que contém o arquivo `manage.py`.

### 2. Criar o ambiente virtual

```bash
python -m venv .venv
```

### 3. Ativar o ambiente virtual

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

Se houver erro de permissão:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Depois, ative novamente.

### 4. Instalar as dependências

```bash
python -m pip install Django djangorestframework
```

### 5. Configurar o banco de dados

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Verificar o projeto

```bash
python manage.py check
```

### 7. Iniciar o servidor

```bash
python manage.py runserver
```

Acesse pelo navegador:

http://127.0.0.1:8000/

Para encerrar o servidor, pressione `Ctrl + C` no terminal.

## Logins para teste

| Perfil | E-mail | Senha |
|---|---|---|
| Jornalista | jornalista@nossoSP.com | NossoSP123! |
| Administrador | admin@teste.com | admin123 |
| Leitor | leitor@nossoSP.com | Leitor123! |

**Importante:** utilize esses dados na página de login do próprio site. São contas de demonstração configuradas no código.

## Passo a passo para testar

**Jornalista**
1. Entre com o login de jornalista.
2. Acesse a área de criação de notícias.
3. Preencha título, conteúdo, categoria, tags, região, bairro e rua.
4. Salve como rascunho ou envie para aprovação.

**Administrador**
1. Entre com o login de administrador.
2. Acesse o painel administrativo.
3. Analise as notícias pendentes.
4. Aprove ou negue uma publicação.

**Leitor**
1. Entre com o login de leitor.
2. Acesse as notícias publicadas.
3. Teste os comentários e favoritos.
4. Consulte o portal do leitor.

## Teste da API Geoapify

1. Entre como jornalista.
2. Cadastre uma notícia com rua, bairro e região.
3. Envie para aprovação.
4. Entre como administrador e aprove a notícia.
5. Abra a publicação e confira o mapa.

A Geoapify transforma o endereço em coordenadas geográficas e permite posicionar o mapa.

## Possíveis erros

| Erro | Solução |
|---|---|
| Python não reconhecido | Instale o Python e adicione ao PATH. |
| No module named django | Execute `python -m pip install Django`. |
| No module named rest_framework | Execute `python -m pip install djangorestframework`. |
| manage.py não encontrado | Entre na pasta correta do projeto. |
| no such table | Execute `python manage.py migrate`. |
| Porta 8000 ocupada | Execute `python manage.py runserver 8001`. |
| Mapa não aparece | Verifique a chave Geoapify, o endereço e a conexão com a internet. |
| Página não abre | Confira se o servidor está em execução. |

## Estrutura principal

- `manage.py`: comandos do Django.
- `config/`: configurações do projeto.
- `noticias/`: modelos, views e funcionalidades.
- `templates/`: páginas HTML.
- `static/`: arquivos CSS e JavaScript.
- `media/`: imagens enviadas.
- `db.sqlite3`: banco de dados local.

---

**Nosso SP — Informação local, participação e comunidade.**
