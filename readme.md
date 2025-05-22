## 1. Qual o papel de cada camada da arquitetura MVC?

No projeto, usamos MVC para organizar o código:

- **Model:** cuida do banco de dados. Ele salva, busca, edita e apaga alunos e cursos.
- **Controller:** recebe os pedidos do usuário (como salvar ou editar um aluno), chama o Model e envia os dados para a View.
- **View:** mostra as informações no navegador com HTML e EJS.

Eles trabalham juntos: o usuário faz uma ação → o Controller recebe → o Model acessa o banco → a View mostra o resultado.

---

## 2. Como o projeto usa JSON?

Tem uma rota que responde em JSON:  
**GET /alunos/curso/:curso_id**  
Ela retorna os alunos de um curso específico em formato JSON. O Controller chama o Model, pega os dados e responde com `res.json(alunos)`. Isso pode ser usado por outro sistema ou por JavaScript no front-end.

---

## 3. Por que usar HTML com formulários e tabelas?

Porque é simples, direto e fácil de usar. Com formulários, dá pra cadastrar e editar. Com tabelas, dá pra organizar os dados. Mesmo com tecnologias novas, HTML básico ainda funciona bem em projetos com Node.js, principalmente para sistemas simples e educativos.
