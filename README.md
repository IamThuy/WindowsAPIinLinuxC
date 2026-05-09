# WindowsAPIinLinuxC

## Como funciona

Usando o MinGW, você pode compilar programas que utilizam a Windows API diretamente no Linux.

Depois, você pode usar o Wine para executar o programa gerado (.exe).

---

## Instalação dos requisitos

### 1. Instalar o MinGW

No Arch Linux, o pacote recomendado é o toolchain completo:

```bash
sudo pacman -S mingw-w64-toolchain
```

---

### 2. Configurar o VSCode

Crie uma pasta oculta no projeto chamada:

```
.vscode
```

Dentro dela, crie um arquivo chamado:

```
c_cpp_properties.json
```

---

### 3. Configuração do JSON

Cole o conteúdo do `c_cpp_properties.json` que está localizado no repositório do projeto.

---

## Executando o programa

Depois de compilar o código com o MinGW, use o Wine para executar o binário:

```bash
wine seu_programa.exe
```

---

## Observações

- O MinGW permite compilar código C/C++ para Windows no Linux
- O Wine executa o binário Windows sem necessidade de recompilar
- Certifique-se de incluir corretamente `Windows.h` ao compilar