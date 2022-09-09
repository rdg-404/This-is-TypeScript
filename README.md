<div align="center">
  <img  align="center" src="https://blog.theodo.com/static/ba2166b279b234c4824d1c2fb299ced2/a79d3/ts_logo.png">
</div>


<h3>É uma linguagem de tipagem, ou seja, não deixa tu escrever códigos errados, avisa dos erros logo no desenvolvimento.</h3>

<h1>Exemplos</h1>

### Utilizar o [TypeScript Playgorund](https://www.typescriptlang.org/play?#code/Q) para testar os códigos.

``` typescript
const userName = "John Doe"

userName()
```
* Vai apontar erro, porque ``` userName ``` não é uma função!


``` typescript
const user = {
  name: "John Doe",
  email: "jhondoe@email.com"
}

console.log(user.age)
```

* Vai dar ruim, porque ``` age ``` não existe dentro do objeto ``` user ```

``` typescript
function sum(a: number, b: number){
  return a + b;
}

sum.toLowerCase();
```

* Erro porque não da para utilizar ``` toLoweCase() ``` em numeros

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
* Especificar tipagem na variável


<h2>JavaScript</h2>

``` javascript
function showUser(user, age){
  console.log(`Olá ${user}. Você tem ${age} anos.)
}

showUser('John Doe', 22)
```
* A tipagem não é importante para o JS


<h1 align="center">Tipos primitivos</h1>

``` typescript
  let loading: boolean;
  loading = false;
  
  
  let email: string;
  email = "johndoe@email.com";
  
  
  let price: number;
  price = 10.50;
  price = 20;
```

<h3>Também segue o mesmo padrão para Arrays</h3>

``` typescript
   let numbers: number[];
   numbers = [1,2,3,4,5]
```

<h3>E como é usado em funções?</h3>

``` typescript
    function showMessage(message: string): void{
      return message;
    }
```

* Erro! Porque espera um ``` return ``` vazio

``` typescript
    function showMessage(message: string): string{
      return message;
    }
```

* Ok! Porque espera o que o ``` return ``` seja uma string


<br><br><br><br>
<h1 align="center">Atribuir vários tipos para a mesma variável (UNION)</h1>

``` typescript
  function printUserId(id: number | string){
    console.log(`O ID do usuário é: ${id}`);
  }
  
  printUserId('101')
  printUserId(101)
```

* O typescript aceitaria tanto ``` number ``` como ``` string ```


<br><br><br><br>
<h1 align="center">Generics</h1>


``` typescript
  function useState<T extends string | number = number>(){
    let state: T;
    
    function get(){
      return state;
    }
    
    function set(newValue: T){
      state = newValue;
    }
    
    return {get, set}
  }
  
let newState = useState<string>();
newState.get();
newState.set("John Doe");
newState.set(123);
```
* Utilizando uma letra entre <> ao declarar a função ``` <T> ```, fala que terá o tipo que for definido ao chamar a mesma.
* Usando extends ``` <T extends string | number> ``` o tipo fica indefinido, mas lembrar de não declarar o tipo ao chamar a função.
* Atribuindo o sinal de = na declaração da função ``` <T extends string | number = number> ```, torna um tipo padrão para a variável.

<br><br><br><br>
<h1 align="center">Type</h1>

``` typescript
  type IdType = string | number;
  
  let userId: IdType;
  let adminId: IdType;
  
  
  adminId = 10;
```

* Serve para quando duas ou mais variáveis têm os mesmos tipos declarados

<br><br><br><br>
<h1 align="center">Asserção de tipos</h1>

``` typescript
  type DefaultUser{
      id: number;
      name: string;
      avatar: string;
  }
  
  
  let newUser = {} as DefaultUser;
```

* O novo usuário receberá as propriedades baseadas no usuário padrão, é como se fosse um modelo a ser seguido.



<br><br><br><br>
<h1 align="center">Tipagem para objetos</h1>

``` typescript
  type User = {
    name: string;
    email: string;
    age: number;
    isAdmin: boolean;
  }
  const newUser: User
 
```
* A variável newUser vai possuir todas as propriedades de User
* Colocar uma ? na frente da propriedade ``` idAdmin? ``` a torna opcional



<br><br><br><br>
<h1 align="center">Juntando tipos</h1>

``` typescript
  type User = {
    name: string;
    id: number;
  }
  
  type Char = {
    nickname: string;
    level: number;
  }
  
  type PlayerInfo = User & Char;
  
  let info: PlayerInfo = {
    id: 09;
    name: "John Doe";
    nickname: "Morgan";
    level: 999
  }
```

* Cria um novo tipo ``` PlayerInfo ``` que conterá tanto ``` User ``` quanto ``` Char ``` usando o &.


