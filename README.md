
 SysSoft activity - decode encrypted message
 ==============================

A descrição do problema se encontra no README dentro da pasta hack01. Os autores, no arquivo AUTHORS.

Para decriptar o programa, criamos uma biblioteca dinâmica que sobrescreve a função de autorização utilizada no programa docrypt.

Dentro da pasta hack01, execute o comando a seguir para compilar a biblioteca:

```bash
make -f makefile
```

Isso irá gerar o arquivo libhackfile.so.

Por fim, para executar o programa utilizando esta biblioteca execute:

```bash
make -f makefile run
```

O programa pedirá por credenciais de usuário e senha, basta digitar qualquer coisa ou apertar a tecla enter.

Em seguida, o programa irá requisitar por uma decryption key. Esta foi encontrada realizando um objdump no arquivo encrypt o qual continha a declaração da chave explicitamente no código: "easy". Passando ela, é possível decriptar a mensagem.

Os arquivos encrypt_disassembly.txt e encrypt_key_dump.txt contêm o output do objdump realizado para encontrar a chave. A chave fica explícita no arquivo encrypt_key_dump.txt.
