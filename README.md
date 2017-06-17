<a href="https://github.com/apirobot/django-vue-simplenote">
    <p align="center">
      <img src="https://raw.githubusercontent.com/apirobot/django-vue-simplenote/master/other/preview.gif" alt="django-vue-simplenote">
    </p>
</a>

---

## Description

`django-vue-simplenote` is an example of note application that uses **django & django rest framework** as a backend and **vue.js** as a frontend.


## How to run

Clone the repository:

```zsh
➜ git clone https://github.com/apirobot/django-vue-simplenote
```

Create and activate virtualenv:

```zsh
➜  virtualenv -p python3 env
➜  source env/bin/activate
```

Run scripts from Makefile that install all dependencies, run migrations and start dev server.

```zsh
(env) ➜  make dev
(env) ➜  make migrate
(env) ➜  make run
```

We are done.

- Frontend: http://localhost:8080/
- Backend: http://localhost:8000/
