# Instalação do Bloqueador de Anúncios do Spotify no Linux

Este guia explica como instalar o bloqueador de anúncios para o Spotify no Linux.

## Pré-requisitos

Certifique-se de que o Spotify não esteja instalado via Snap, pois o bloqueador não é compatível com essa versão.

## Instalação

1. **Clone o Repositório**:
   ```bash
   git clone https://github.com/abba23/spotify-adblock.git
   ```

2. **Navegue até o diretório clonado**:
   ```bash
   cd spotify-adblock
   ```

3. **Compile o projeto**:
   ```bash
   make
   ```

4. **Instale o bloqueador**:
   ```bash
   sudo make install
   ```

## Execução

Para executar o Spotify com o bloqueador de anúncios:

```bash
LD_PRELOAD=/usr/local/lib/spotify-adblock.so spotify &
```

## Criando um Atalho

Edite o arquivo `.desktop` do Spotify para incluir o `LD_PRELOAD` na execução:

```plaintext
Exec=env LD_PRELOAD=/usr/local/lib/spotify-adblock.so spotify %U
```

Salve as mudanças e utilize o ícone para abrir o Spotify com o bloqueador ativo.
