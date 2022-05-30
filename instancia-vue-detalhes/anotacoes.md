# Multiplas instancias

Sim podemos ter, mas não é uma boa prática, só em cenários que realmente precisam por algum motivo aleatório.

# Podemos criar variáveis pela instancia do vue e usa-las na renderização?

A resposta é NÃO, porque nenhuma propriedade ou method que é criado fora do vue não é reativo, logo ele não pode ser utilizado
porque ele não vai ter todos os seus "SUPER-PODERES" com get and setters and watchers para fazer as lógicas
dentro do seu component

# Como o vue Atualiza A DOM ?

O vue cria uma DOM virtual, basicamente uma replica da DOM original e trata toda atualização de dados a partir dela,
então ele está sempre monitorando essa virtual DOM e em caso de mudanças ele faz a atualização ( QUANDO NECESSÁRIO ).

<strong>Instancua VUE </strong> <-- Verificando as diferenças --> <strong> Virtual DOM </strong> <-- Verifica se gerou impacto e tem que atualizar a DOM Física --> <strong> DOM </strong>

Tudo isso é feito para você ter o maior nível de performance possível.

# Ciclo de vida do VUE e os métodos de invocação


beforeCreate -> Método chamado antes de criar a instancia do vue ( você pode usar para obter dados no backend antes do VUe inicializar).

Logo depois ele vai criar sua instancia, fazer injeção de depedências, reatividades dos atributos e uma vez que sua instancia é criada
ele chama o metodo

created -> Onde ele verifica se tem EL? ou se tem TEMPLATE e dependendo chamar o mount. Antes de pegar os dados e jogar na DOM ele chama o método

beforeMount -> agora ele vai pegar os elementos e montar na dom e jogar tudo na referência $el e depois disso vme a função

mounted -> O moutned é resposável ele ciclo de atualização onde vai ficar sempre olhando para virtual DOM
e chamando o beforeUpdate ou update .

beforeDestroy -> para matar todos os watchers e componentes filhos e eventos que estão sendo escutados

destroyed -> E agora depois disso nada que você tentar utilizar com o vue, métodos, dados nenhum mais é executado, pois a instancia
já fui destruída.




