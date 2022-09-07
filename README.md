<h1 align="center">TypeScript</h1>
<h3>É uma linguagem de tipagem, ou seja, não deixa tu escrever códigos errados, avisa dos erros logo no desenvolvimento.</h3>

<h1>Exemplos</h1>

### Utilizar o [TypeScript Playgorund](https://www.typescriptlang.org/play?#code/Q) para testar os códigos.

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

``` typescript
function sum(a: number, b: number){
  return a + b;
}

sum.toLowerCase();
```

**Erro porque não da para utilizar ``` toLoweCase() ``` em numeros**

<br><br><br><br>
<h1 align="center">TypeScript x JavaScript</h1>

<h3>TypeScript escreve o JS de uma maneira mais compreensivel</h3>


<h2>TypeScript</h2>

``` typescript
function showUser(user: string, age: number){
  console.log(`Olá ${user}. Você tem ${age} anos.)
}

showUser('John Doe', 22)

```
**Especificar tipagem na variável**


<h2>JavaScript</h2>

``` javascript
function showUser(user, age){
  console.log(`Olá ${user}. Você tem ${age} anos.)
}

showUser('John Doe', 22)
```
**A tipagem não é importante para o JS**






