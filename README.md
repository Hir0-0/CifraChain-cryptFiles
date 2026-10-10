# CifraChain

Aplicação estática para encriptar e decriptar textos e arquivos com uma cadeia de cifras diretamente no navegador. Os dados são processados no próprio dispositivo; não há dependências de React, Node.js, servidor de aplicação ou etapa de build.

## Publicar no GitHub Pages

1. Coloque `index.html`, `favicon.svg`, `.nojekyll` e `README.md` na **raiz da branch `main`**.
2. No GitHub, abra **Settings → Pages**.
3. Em **Build and deployment**, escolha **Deploy from a branch**.
4. Selecione a branch `main` e a pasta `/(root)`, e salve.
5. Abra o endereço exibido nessa mesma tela após a publicação.

O arquivo `index.html` na raiz é a página de entrada do site. O `README.md` serve apenas como documentação do repositório; ele não é o app.

## Executar localmente

Basta abrir `index.html` em um navegador moderno. Para melhor compatibilidade com as APIs criptográficas do navegador, recomenda-se testar via HTTPS ou por um servidor local, por exemplo:

```bash
python -m http.server 8000
```

Depois abra `http://localhost:8000`.

## Recursos

- Cadeias de cifras reordenáveis e configuráveis.
- Encriptação e decriptação de textos e arquivos.
- AES-GCM e AES-CBC, Base64, hexadecimal, URL encode, XOR, RC4, César, Vigenère, Atbash, Morse, Bacon e GZIP.
- Exportação/importação de perfis e pacotes de descriptografia.
- Histórico armazenado localmente no navegador.

**Nota de segurança:** AES-GCM é a opção recomendada para confidencialidade e verificação de integridade. XOR, RC4, César, Vigenère, Atbash, Morse e Bacon são para fins didáticos e não devem ser usados para proteger dados sensíveis. Proteja os perfis que incluem chaves com uma senha mestre forte.
