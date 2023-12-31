# Rustcode
## Introdução ao Rust 


### Rust é uma linguagem de programação de sistemas desenvolvida pela Mozilla, conhecida por sua segurança e desempenho. Nesta primeira aula, vamos abordar os conceitos básicos do Rust:

##### 1  - Instalação do Rust: Como instalar o compilador Rust em seu sistema.

##### 2 - Hello, World!: Escrever e executar seu primeiro programa Rust.

##### 3 - Variáveis e Tipos de Dados: Explorar os tipos de dados básicos em Rust, como inteiros, floats, booleanos e caracteres.

##### 4  - Mutabilidade: Aprender sobre a diferença entre variáveis mutáveis e imutáveis em Rust.


### Aula 2: Estruturas de Controle e Funções em Rust

###### 1 - Condicionais (if, else, match): Aprenda a usar condicionais para controlar o fluxo do programa.

###### 2 - Loops (for, while): Explore como criar loops em Rust para repetir tarefas.

###### 3 - Funções: Saiba como definir e chamar funções em Rust, incluindo a passagem de argumentos e valores de retorno.

###### 4 - Ownership e Borrowing: Introdução aos conceitos fundamentais de propriedade (ownership) e referência (borrowing) em Rust, que tornam a linguagem segura e eficiente.

### Aula 3: Coleções em Rust

#### 1 - Arrays e Slices: Entenda como criar, acessar e manipular arrays e slices em Rust.

##### 2 - Vec: Aprenda sobre o tipo de coleção dinâmica Vec e como usá-lo para armazenar uma lista de elementos.

##### 3 - Strings: Explore como lidar com strings em Rust, incluindo as diferenças entre strings literais e strings dinâmicas.

##### 4 - HashMaps: Introdução aos HashMaps, que permitem armazenar pares chave-valor.

### Aula 4: Estruturas de Dados Personalizadas em Rust

###### 1 - Structs: Aprenda a criar e usar structs para definir estruturas de dados personalizadas.

###### 2 - Enums: Explore os enums em Rust, que permitem representar tipos de dados com várias variantes.

###### 3 - Métodos: Saiba como adicionar métodos a structs para encapsular o comportamento relacionado a essas estruturas.

###### 4 - Traits: Introdução às traits, que permitem definir comportamentos compartilhados entre tipos diferentes.

### Aula 5: Gerenciamento de Erros e Concorrência em Rust

##### 1 - Manejo de Erros: Explore as maneiras de lidar com erros em Rust, incluindo o uso de Result e Option.

##### 2 - Concorrência: Introdução ao modelo de concorrência em Rust com threads e async/await.

##### 3 - Ownership Avançado: Aprofunde-se em propriedade (ownership) e referências em cenários mais complexos.

##### 4 - Gerenciamento de Dependências: Saiba como gerenciar dependências externas em seu projeto Rust com Cargo, o gerenciador de pacotes oficial.

### Aula 6: Programação Avançada em Rust

###### 1 - Traits Avançadas: Aprofunde-se nas traits em Rust, incluindo a criação de traits genéricas e associação de tipos.

###### 2 - Macros: Aprenda sobre macros em Rust e como criar macros personalizadas.

###### 3 - Unsafe Rust: Introdução ao uso do unsafe para contornar as restrições de segurança da linguagem.

###### 4 ####### 4 - Padrões de Design: Explore padrões de design comuns em Rust, como o padrão de empréstimo (borrowing pattern).

######  5 - Web Development com Rust: Veja como usar Rust para desenvolvimento web com frameworks como Rocket ou Warp.

### Aula 7: Rust na Prática - Desenvolvimento de Projetos

###### 1 - Desenvolvimento de Aplicativos de Linha de Comando (CLI): Aprenda como criar aplicativos de linha de comando eficientes em Rust.

###### 2 - Desenvolvimento de Bibliotecas: Saiba como criar bibliotecas reutilizáveis em Rust que podem ser compartilhadas com outros desenvolvedores.

###### 3 - Desenvolvimento de Aplicativos Web: Explore como criar aplicativos web em Rust usando frameworks como Rocket, Actix, ou Warp.

###### 4 - Desenvolvimento de Jogos: Descubra como desenvolver jogos em Rust usando a biblioteca Amethyst ou outras opções.

###### 5 -  Integração com Outras Linguagens: Aprenda como integrar código Rust em projetos escritos em outras linguagens, como C/C++ ou Python.

### Aula 8: Tópicos Avançados em Rust e Desafios
##### 1 - Rust no Ecossistema de Desenvolvimento: Aprofunde-se em tópicos avançados, como lifetimes, async/await, e gerenciamento de memória.

###### 2 - Desafios de Codificação: Apresentarei desafios de codificação para você aplicar o que aprendeu até agora em Rust.

##### 3 - Projetos Pessoais: Incentivo para iniciar um projeto pessoal em Rust para consolidar suas habilidades.

##### 4 - Comunidade e Recursos: Saiba onde encontrar recursos adicionais, fóruns e comunidades para continuar seu aprendizado em Rust.


### Desafio 1: Fatorial em Rust

##

Seu primeiro desafio é escrever um programa em Rust que calcula o fatorial de um número inteiro não negativo. O fatorial de um número n é o produto de todos os inteiros de 1 a n.

Por exemplo, o fatorial de 5 é 5! = 5 x 4 x 3 x 2 x 1 = 120.

Tente implementar esta função em Rust.

#### Aqui está uma implementação simples em Rust para calcular o fatorial de um número:

~~~
fn calcular_fatorial(numero: u64) -> u64 {
    if numero == 0 {
        return 1;
    }
    
    let mut resultado = 1;
    for i in 1..=numero {
        resultado *= i;
    }
    
    resultado
}

fn main() {
    let numero = 5; // Substitua pelo número desejado.
    let resultado = calcular_fatorial(numero);
    println!("O fatorial de {} é igual a {}.", numero, resultado);
}

~~~
*  Neste código, a função calcular_fatorial recebe um número inteiro não negativo e calcula seu fatorial. No main(). 
##

### Tópico 1: "Hello, World!"
##
*Aqui está um exemplo do programa "Hello, World!" em Ferrugem:*
~~~
fn main() {
    println!("Hello, World!");
}

~~~
* fn main() { ... }defina a função principal do programa.
* println! é uma macro para imprimir texto no console.
##### Compile e execute este programa usando o comando cargo runno terminal. Ele imprimirá "Olá, mundo!" sem console.
##
### Tópico 2: Variáveis ​​e tipos de dados em Rust
##
#### Em Rust, você precisa declarar o tipo de uma variável explicitamente ou deixar o Rust inferir o tipo automaticamente. Aqui estão alguns exemplos:
~~~
fn main() {
    // Variáveis inteiras
    let idade: i32 = 30; // Declara uma variável inteira de 32 bits
    let numero = 42; // O Rust infere que é um i32
    
    // Variáveis de ponto flutuante
    let salario: f64 = 1000.50; // Declara um ponto flutuante de 64 bits
    let altura = 1.75; // O Rust infere que é um f64
    
    // Variáveis booleanas
    let esta_chovendo = true;
    
    // Caracteres
    let letra_a = 'a';
    
    // Texto (String)
    let nome = "Alice"; // O Rust infere que é uma String
    
    println!("Idade: {}", idade);
    println!("Salário: {:.2}", salario); // {:.2} formata para duas casas decimais
    println!("Está chovendo? {}", esta_chovendo);
    println!("Primeira letra do nome: {}", letra_a);
    println!("Nome: {}", nome);
}

~~~
* let é usado para declarar variáveis ​​em Rust.
* i32 e f64são exemplos de tipos de dados.
* {:.2}é usado para formatar números de ponto flutuante.
##
### Tópico 3: Mutabilidade em Ferrugem
## 
#### Em Rust, por padrão, as variáveis ​​são imutáveis, o que significa que você não pode alterar o valor delas após a atribuição. Para tornar uma variável mutável, você deve usar a palavra-chave mut. Aqui está um exemplo:
~~~
fn main() {
    let x = 5; // Variável imutável
    println!("x: {}", x);
    
    let mut y = 10; // Variável mutável
    println!("y (antes): {}", y);
    
    y = 15; // Agora podemos alterar o valor de y
    println!("y (depois): {}", y);
}

~~~
* Neste exemplo, xé uma variável imutável e yé uma variável mutável. Você pode receber um novo valor a y, mas não a x.
##

### Tópico 4: Condicionais em Rust (if, else, match)
##
#### Rust oferece várias formas de declaração condicional. Vamos começar com if, else, e match.
~~~
fn main() {
    let numero = 5;

    if numero < 0 {
        println!("Número é negativo.");
    } else if numero == 0 {
        println!("Número é igual a zero.");
    } else {
        println!("Número é positivo.");
    }
}

~~~
* Neste exemplo, o programa verifica se numeroé negativo, igual a zero ou positivo e imprime uma mensagem correspondente 
##### Exemplo 2:match
~~~
fn main() {
    let dia_da_semana = "quarta-feira";

    match dia_da_semana {
        "segunda-feira" | "terça-feira" | "quarta-feira" | "quinta-feira" | "sexta-feira" => {
            println!("Dia de trabalho!");
        }
        "sábado" | "domingo" => {
            println!("Fim de semana!");
        }
        _ => {
            println!("Dia inválido.");
        }
    }
}

~~~
* Neste exemplo, o matché usado para atribuir o valor de dia_da_semanavárias opções e imprimir uma mensagem correspondente.


##
### Tópico 5: Loops em Rust (for e while)
##
#### Rust oferece duas principais estruturas de repetição: for e while. Vamos explorar os exemplos:
~~~
fn main() {
    // Loop de 1 a 5 (incluindo 5)
    for numero in 1..=5 {
        println!("Número: {}", numero);
    }
}

~~~

* Neste exemplo, o for é usado para criar um loop de 1 a 5 e imprimir cada número.

### Exemplo 2: while Loop

~~~

fn main() {
    let mut contador = 0;

    while contador < 5 {
        println!("Contador: {}", contador);
        contador += 1;
    }
}

~~~
* Neste exemplo, usamos um while loop para imprimir o valor de contador enquanto ele for menor que 5.
##

### Tópico 6: Funções em Rust
##
##### Funções são blocos de código reutilizáveis em Rust. Aqui está um exemplo de como criar e chamar funções:
~~~
// Definindo uma função chamada "soma"
fn soma(a: i32, b: i32) -> i32 {
    let resultado = a + b;
    resultado // O último valor da função é retornado implicitamente
}

fn main() {
    let numero1 = 5;
    let numero2 = 3;
    
    // Chamando a função "soma"
    let resultado = soma(numero1, numero2);
    
    println!("A soma de {} e {} é igual a {}.", numero1, numero2, resultado);
}

~~~
* Neste exemplo, criamos uma função chamada soma que recebe dois números inteiros (a e b) como argumentos e retorna a soma deles. Na função main, chamamos a função soma e imprimimos o resultado.
* 
##

### Tópico 7: Ownership e Borrowing em Rust
##
#### O sistema de propriedade (ownership) e referências (borrowing) é uma característica fundamental de Rust para garantir a segurança e prevenir problemas de gerenciamento de memória. Vamos explorar isso com exemplos:

###### Exemplo 1: Ownership (Propriedade)
~~~
fn main() {
    let s1 = String::from("Olá"); // s1 é a proprietária deste valor
    let s2 = s1; // s1 "empresta" o valor para s2
    // println!("s1: {}", s1); // Isso resultaria em um erro, s1 não é mais válido aqui
    println!("s2: {}", s2);
}

~~~
* Neste exemplo, s1 é a proprietária da String inicial. Quando atribuímos s1 a s2, s1 perde a propriedade e não pode mais ser usado.
###### Exemplo 2: Borrowing (Empréstimo)
~~~
fn main() {
    let s1 = String::from("Olá");
    let tamanho = calcular_tamanho(&s1); // Passamos uma referência para a função
    println!("Tamanho de s1: {}", tamanho);
}

fn calcular_tamanho(s: &String) -> usize { // Recebemos uma referência
    s.len() // Podemos acessar o valor referenciado, mas não modificá-lo
}

~~~

* Neste exemplo, passamos uma referência &s1 para a função calcular_tamanho. Isso permite que a função acesse o valor sem possuir a propriedade.

* Esses são conceitos importantes para evitar vazamentos de memória e erros de acesso em Rust.
##

### Tópico 8: Estruturas de Dados Personalizadas em Rust
##
##### Em Rust, você pode criar suas próprias estruturas de dados usando structs(estruturas) e enums(enumerações). Vamos explorar ambos com exemplos:
###### Exemplo 1: Structs (Estruturas)
~~~
// Definindo uma struct chamada "Pessoa"
struct Pessoa {
    nome: String,
    idade: u32,
}

fn main() {
    // Criando uma instância da struct "Pessoa"
    let alice = Pessoa {
        nome: String::from("Alice"),
        idade: 30,
    };
    
    // Acessando os campos da struct
    println!("Nome: {}", alice.nome);
    println!("Idade: {}", alice.idade);
}

~~~
* Neste exemplo, criamos uma struct chamada Pessoacom campos nomee idade, e depois criamos uma instância da struct.
###### Exemplo 2: Enums (Enumerações)

~~~
// Definindo um enum chamado "DiaDaSemana"
enum DiaDaSemana {
    Segunda,
    Terca,
    Quarta,
    Quinta,
    Sexta,
    Sabado,
    Domingo,
}

fn main() {
    // Usando um valor do enum
    let dia = DiaDaSemana::Quarta;
    
    match dia {
        DiaDaSemana::Sabado | DiaDaSemana::Domingo => {
            println!("É fim de semana!");
        }
        _ => {
            println!("É dia útil.");
        }
    }
}

~~~
* Neste exemplo, criamos um enum chamado DiaDaSemana que representa os dias da semana e usamos um valor do enum em um match para determinar se é um dia útil ou de fim de semana.

* Essas estruturas de dados personalizadas são úteis para organizar e representar dados em seu código.
##
### Tópico 9: Traits em Rust
##
##### As traits em Rust são semelhantes às interfaces em outras linguagens de programação e permitem definir comportamentos compartilhados entre diferentes tipos de dados. Vamos explorar como criar e usar traits em Rust com exemplos:

##### Exemplo 1: Definindo uma Trait
~~~
 // Definindo uma trait chamada "Apresentavel"
trait Apresentavel {
    fn apresentar(&self);
}

// Implementando a trait para o tipo String
impl Apresentavel for String {
    fn apresentar(&self) {
        println!("Olá, sou uma String: {}", self);
    }
}

fn main() {
    let texto = String::from("Rust é incrível!");
    texto.apresentar();
}

~~~
* Neste exemplo, definimos uma trait chamada Apresentavel e a implementamos para o tipo String, permitindo que objetos do tipo String usem a função apresentar.

##### Exemplo 2: Uso Polimórfico de Traits
~~~
fn apresentar_coisa(apresentavel: &dyn Apresentavel) {
    apresentavel.apresentar();
}

fn main() {
    let texto = String::from("Rust é poderoso!");
    let numero = 42;

    apresentar_coisa(&texto);
    apresentar_coisa(&numero.to_string());
}

~~~

* Neste exemplo, usamos polimorfismo para chamar a função apresentar em diferentes tipos de dados que implementam a trait Apresentavel.
##

### Tópico 10: Macros em Rust
##
##### As macros em Rust são uma poderosa ferramenta para gerar código de forma programática. Vamos explorar como criar macros simples em Rust com exemplos:

##### Exemplo 1: Criando uma Macro Básica
~~~
// Definindo uma macro chamada "saudacao"
macro_rules! saudacao {
    () => {
        println!("Olá, mundo!");
    };
}

fn main() {
    saudacao!(); // Chamando a macro
}

~~~
* Neste exemplo, definimos uma macro saudacao que gera código para imprimir "Olá, mundo!" quando chamada.

##### Exemplo 2: Macros que Aceitam Parâmetros

~~~
// Definindo uma macro chamada "soma"
macro_rules! soma {
    ($a:expr, $b:expr) => {
        $a + $b
    };
}

fn main() {
    let x = 5;
    let y = 3;
    let resultado = soma!(x, y); // Chamando a macro com parâmetros
    println!("Resultado da soma: {}", resultado);
}

~~~

* Neste exemplo, definimos uma macro soma que aceita dois valores como parâmetros e retorna a soma deles quando chamada.

* As macros são uma ferramenta poderosa para gerar código repetitivo ou realizar tarefas complexas de metaprogramação.
##
### Tópico 11: Rust na Web - Desenvolvimento Web com Rust
##
##### Rust também pode ser usado para desenvolvimento web, com frameworks como Rocket, Actix, Warp e outros. Vamos explorar um exemplo simples com o framework Rocket:

##### Exemplo com Rocket: Criando um Servidor Web Básico
###### Para criar um servidor web simples com Rust e Rocket, primeiro, você precisa adicionar Rocket como dependência em seu arquivo Cargo.toml:
~~~
[dependencies]
rocket = "0.5"

~~~
##### Aqui está um exemplo de servidor web Rocket básico:
~~~
use rocket::{Rocket, get, routes};

#[get("/")]
fn index() -> &'static str {
    "Olá, mundo!"
}

fn main() {
    let rocket = Rocket::ignite().mount("/", routes![index]);
    rocket.launch();
}

~~~
* Neste exemplo, definimos uma rota para a raiz ("/") que retorna a mensagem "Olá, mundo!" quando acessado.

* -se de incluir as dependências corretas no seu Cargo.tomle, em seguida, você pode usar cargo runpara iniciar o servidor web.

* Lembre-se de que isto é apenas um exemplo simples. Frameworks como Rocket oferecem recursos avançados para criar aplicativos web mais complexos em Rust.
##
### Tópico 12: Integração com Outras Linguagens
##
###### Rust é conhecido por sua capacidade de se integrar facilmente com outras linguagens, como C/C++ e Python. Vamos explorar como fazer essa integração com exemplos simples.

##### Exemplo com C/C++: Chamando Funções C a partir de Rust

###### Para chamar funções C a partir de Rust, você precisa criar uma interface usando o arquivo de cabeçalho C e vincular a biblioteca C correspondente. Vamos ver um exemplo de chamada de uma função C a partir de Rust:

###### Suponha que temos um arquivo funcoes.c com a seguinte função:
~~~
#include <stdio.h>

void funcao_c() {
    printf("Função C foi chamada!\n");
}

~~~
##### Agora, podemos criar um arquivo Rust que chama essa função:
~~~
extern "C" {
    fn funcao_c();
}

fn main() {
    unsafe {
        funcao_c();
    }
}

~~~
* Este exemplo demonstra como usar extern "C" para declarar uma função C em Rust e, em seguida, chamar essa função de dentro de um programa Rust.

#### Exemplo com Python: Chamando Rust a partir de Python

##### Você pode criar uma biblioteca compartilhada em Rust e, em seguida, chamar essa biblioteca a partir de um programa Python usando a biblioteca ctypes. Aqui está um exemplo:

###### Suponha que temos uma função simples em Rust que queremos chamar:
~~~
// lib.rs
#[no_mangle]
pub extern "C" fn somar(a: i32, b: i32) -> i32 {
    a + b
}

~~~
##### Compilamos isso em uma biblioteca compartilhada:

~~~
$ rustc --crate-type cdylib lib.rs

~~~
##### Agora, podemos chamá-la a partir de Python:
~~~
# main.py
from ctypes import CDLL

# Carregando a biblioteca compartilhada Rust
rust_lib = CDLL("./lib.so")

# Chamando a função somar
resultado = rust_lib.somar(5, 3)
print("Resultado da soma:", resultado)

~~~
* Executando main.py, você verá que a função Rust é chamada a partir do Python.

* Esses são exemplos simples de integração, e a extensibilidade de Rust é uma de suas características poderosas.
##

Fim da jornada Rust intermediário
