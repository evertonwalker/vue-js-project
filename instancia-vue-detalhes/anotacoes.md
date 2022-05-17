# Multiplas instancias

Sim podemos ter, mas não é uma boa prática, só em cenários que realmente precisam por algum motivo aleatório.

# Podemos criar variáveis pela instancia do vue e usa-las na renderização?

A resposta é NÃO, porque nenhuma propriedade ou method que é criado fora do vue não é reativo, logo ele não pode ser utilizado
porque ele não vai ter todos os seus "SUPER-PODERES" com get and setters and watchers para fazer as lógicas
dentro do seu component