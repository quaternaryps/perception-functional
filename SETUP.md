# SETUP: perception-functional (Kit + Datomic Local + Reagent + microk8s, NodePort)

You are an autonomous coding agent running on an Ubuntu 24.04 app server.

Your goal is to:

1. Install prerequisites (Java, Clojure, git, microk8s, Docker).
2. Scaffold a **Kit**-based Clojure app as a **monorepo**.
3. Add **Datomic Local** integration.
4. Add a **Reagent** frontend for the 5 swimlanes of life.
5. Containerize the app with Docker.
6. Deploy it to **microk8s** using a **NodePort** service.

Work in the repository:

`https://github.com/quaternaryps/perception-functional`

Clone it locally before starting.

---

## Phase 0 – Clone repo

```bash
cd ~
git clone https://github.com/quaternaryps/perception-functional.git
cd perception-functional

