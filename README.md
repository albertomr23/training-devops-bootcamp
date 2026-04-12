# Training DevOps Bootcamp

Repositorio de trabajo para el **Bootcamp DevOps 2026** (T-Systems + Universidad de Granada).

---

## Material del bootcamp

Slides, laboratorios, teoria y cheat-sheets estan en la plataforma del curso:

**[carlospalanca.es/cursos](https://carlospalanca.es/cursos)**

El instructor os dara la contrasenya de acceso el primer dia.

| Dia | Temas | App |
|-----|-------|-----|
| Dia 1 | Cultura DevOps, Git, Docker, Docker Compose | MyFitness |
| Dia 2 | CI/CD, GitHub Actions, Pipelines | MyFitness + CampusEats |
| Dia 3 | Kubernetes, Helm, GitOps con ArgoCD | CampusEats |
| Dia 4 | Terraform, Prometheus, Grafana, Proyecto Final | QuizBattle + Monitoring |

---

## Preparar el entorno

Antes del primer dia, necesitais:

- Windows 10/11 con **WSL2 + Ubuntu**
- **Docker Desktop** con integracion WSL2
- **Git** + cuenta GitHub
- **VS Code** con extension WSL
- **Node.js 20**, **kubectl**, **kind**, **helm**, **terraform** (dentro de WSL2)

La guia paso a paso esta en la plataforma del curso (Dia 0 — Setup del entorno).

---

## Empezar a trabajar

1. **Forkead** este repositorio a vuestra cuenta de GitHub (boton "Fork" arriba a la derecha).

2. **Clonad** vuestro fork dentro de WSL2:

```bash
cd ~/bootcamp
git clone https://github.com/TU-USUARIO/training-devops-bootcamp.git
cd training-devops-bootcamp
```

3. Abrid VS Code:

```bash
code .
```

Ya estais listos para el Dia 1.

---

## Aplicaciones

Las aplicaciones se van liberando dia a dia. Al principio solo teneis acceso a **MyFitness**. El instructor ira anadiendo las demas conforme avance el bootcamp.

### MyFitness (Dia 1)

App de seguimiento de ejercicios. La usareis para crear vuestro primer Dockerfile y Docker Compose.

```
apps/myfitness/
├── backend/     Express API + SQLite (puerto 3001)
└── frontend/    HTML estatico + Nginx
```

**Stack:** Node.js + Express + SQLite

### CampusEats (Dias 2-3) — *bloqueada*

Plataforma de comida del campus. Backend API + frontend + MongoDB. Se libera en el Dia 2.

### QuizBattle (Dia 4) — *bloqueada*

App de votacion en tiempo real con 5 microservicios. Se libera en el Dia 4 para Terraform.

### Monitoring (Dia 4) — *bloqueada*

Stack Prometheus + Grafana. Se libera en el Dia 4 para observabilidad.

---

## Que vais a construir

| Dia | Que anadis | Archivos nuevos |
|-----|-----------|----------------|
| Dia 1 | Dockerfiles + Docker Compose + push a DockerHub | `apps/myfitness/*/Dockerfile`, `docker-compose.yml` |
| Dia 2 | Pipeline CI/CD | `.github/workflows/ci.yml` |
| Dia 3 | Manifiestos Kubernetes | `k8s/*.yaml` |
| Dia 4 | Infraestructura Terraform + Monitoring | `terraform-*/`, dashboards Grafana |

---

## Reglas del repositorio

- Trabajad siempre en vuestra copia (fork). No modifiqueis el repo original.
- Haced commits frecuentes con mensajes descriptivos.
- Si algo se rompe, `git log` para ver que cambio y `git diff` para ver que es diferente.
