<h1>TypeScript</h1>
<h3>É uma linguagem de tipagem, ou seja, não deixa tu escrever códigos errados, avisa dos erros logo no desenvolvimento.</h3>

<h1>Exemplos</h1>

``` typescript
const userName = "John Doe"

userName()
```
**Vai apontar erro, porque ``` userName ``` não é uma função!**


``` typescript
const user = {
  name: "John Doe",
  email: "jhondoe@email.com"
}

console.log(user.age)
```

**Vai dar ruim, porque ``` age ``` não existe dentro do objeto ``` user ```**
