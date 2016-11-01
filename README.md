# example-scala
Repositório com o primeiro projeto de scala. Exemplo implementado do curso do Coursera.

Os principios da linguagem funcional é abodada nessa implementação. Como é a sintaxe e conceitos básico da linguagem Scala. As estruturas dos programados construidos em Scala se assemelha com a linguagem OO Java.

Nesse projeto foram implementadas duas funções para testar os conceitos. As implementações surgeridas segue. Vale ressaltar que ambas as implementações foram acompanhadas por testes unitários.

* SUM

```
def sum(xs: List[Int]): Int = {
  if (xs.isEmpty) throw new java.lang.UnsupportedOperationException("list `xs` is empty")
  if (xs.length == 1) 
      return xs.head 
   else 
      return xs.head + sum(xs.tail)
}
```

* MAX 

```
 def max(xs: List[Int]): Int = {
   if (xs.isEmpty) throw new java.util.NoSuchElementException("`xs` is an empty list")
      return xs.max
 }
```

Foi adicionando ainda o arquivo **plugins.sbt**, dentro de **\example\project**, para configurar os plugins necessários para executar o projeto.

Plugin adicionado em **plugins.sbt** para executar sbt diretamente, sem executar o sbt console.

```
addSbtPlugin("com.typesafe.sbt" % "sbt-start-script" % "0.10.0")

```

Tal plugin foi importado e utilizando em **\example\build.sbt**

```

import com.typesafe.sbt.SbtStartScript
seq(SbtStartScript.startScriptForClassesSettings: _*)

```
