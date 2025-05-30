# S.O. 2025.1 - Atividade 03 - Compilação de código dentro de docker fedora

## Informações gerais

- **Objetivo do repositório**: Repositório para atividade avaliativa dos alunos
- **Assunto**: Implementação de tarefas (processos)
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- disciplina: **SO** [Sistemas Operacionais](https://github.com/sistemas-operacionais/)
- professor: [Leonardo A. Minora](https://github.com/leonardo-minora)
- aluno: Gustavo Henrique da Cruz Macieç
- Matrícula: 20232014040003;

### **1. Objetivo**  
Criar um ambiente isolado com Docker Fedora para compilar e executar programas em C, utilizando:  
- Um Dockerfile personalizado com GCC  
- Mapeamento de volume entre host (Windows) e container  
- Compilação e execução direta no terminal do container  

### **2. Passos Executados**  

#### **Comandos Principais**  
```bash
# Construção da imagem
docker build -t fedora-gcc .

# Execução do container com volume mapeado
docker run -it --rm -v ${PWD}:/app fedora-gcc

# Dentro do container:
gcc main.c -o programa  # Compilação
./programa              # Execução
```

### OBS:
#### main.c:
![image](https://github.com/user-attachments/assets/42e662cf-992e-467e-a29c-c2ef00deca4a)
#### dockerfile:
![image](https://github.com/user-attachments/assets/229d35b6-ace1-405b-baa9-9159a06ae21a)

### **3. Resultados Obtidos** 
#### saída do programa:
```Hello Docker + Fedora + GCC!```

![image](https://github.com/user-attachments/assets/1ff4cd1f-1917-4d1e-bab9-2da9c39faa68)

### **4. Conclusão**
#### A experiência mostrou como o Docker simplifica o desenvolvimento em C, eliminando problemas de compatibilidade. O meu maior desafio foi configurar o mapeamento de volumes, mas acredito que tenha dado certo, com isso, agora posso desenvolver em qualquer máquina sem preocupações. Além da portabilidade, descobri como containers podem padronizar ambientes de trabalho, algo que vou levar para projetos futuros. Uma solução prática que realmente facilita a vida do programador.
