# Porque um componente renderiza?

- Hooks changed (mudou estado, contexto, reducer)
- Props changed (mudou propriedades)
- Parent rerendered (componente pai renderizou)

# Qual o fluxo de renderização?

1. O React recria o HTML da interface daquele componente
2. Compara a versão do HTML recriada com a versão anterior
3. Se mudou alguma coisa, ele reescreve o HTML na tela

# Memo

- Com o memo ele adiciona um passo a mais no fluxo de renderização e o memo irá olhar se mudou algo nos hooks do componente, nas props (deep comparison) e comparar com a versão anterior dos hooks e props.
- Se algo mudou ele vai permitir a nova renderização e entrará no fluxo de renderização, caso não tenha mudado nada, ele não permitirá entrar no fluxo de renderização.
