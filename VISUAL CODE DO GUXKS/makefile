# Makefile para clonar repositório Lua e configurar o Git

# Variáveis
REPO_URL=https://github.com/maidell/lua
USER_NAME=maidell
USER_EMAIL=mateusmaidel@gmail.com
REPO_DIR=lua

# Alvos
all: clone_repo config_git open_code

clone_repo:
	git clone $(REPO_URL)

config_git:
	git config --global user.name $(USER_NAME)
	git config --global user.email $(USER_EMAIL)

open_code: clone_repo
	cd $(REPO_DIR) && code .

# Limpar configurações de usuário global do Git (opcional)
clean:
	git config --global --unset user.name
	git config --global --unset user.email

.PHONY: all clone_repo config_git open_code clean

