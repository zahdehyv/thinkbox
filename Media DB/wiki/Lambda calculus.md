---
type: wiki
subType: ""
title: Lambda calculus
englishTitle: Lambda calculus
year: ""
dataSource: Wikipedia API
url: https://en.wikipedia.org/wiki/Lambda_calculus
id: 18203
wikiUrl: https://en.wikipedia.org/wiki/Lambda_calculus
lastUpdated: 2025/April/01
length: 89493
tags: mediaDB/wiki
---
In [mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic "Mathematical logic"), **lambda calculus** (also written as **_λ_-calculus**) is a [formal system](https://en.wikipedia.org/wiki/Formal_system "Formal system") for expressing [computation](https://en.wikipedia.org/wiki/Computability "Computability") based on function [abstraction](https://en.wikipedia.org/wiki/Abstraction_\(computer_science\) "Abstraction (computer science)") and [application](https://en.wikipedia.org/wiki/Function_application "Function application") using variable [binding](https://en.wikipedia.org/wiki/Name_binding "Name binding") and [substitution](https://en.wikipedia.org/wiki/Substitution_\(algebra\) "Substitution (algebra)"). Untyped lambda calculus, the topic of this article, is a [universal machine](https://en.wikipedia.org/wiki/Universal_machine "Universal machine"), a [model of computation](https://en.wikipedia.org/wiki/Model_of_computation "Model of computation") that can be used to simulate any [Turing machine](https://en.wikipedia.org/wiki/Turing_machine "Turing machine") (and vice versa). It was introduced by the mathematician [Alonzo Church](https://en.wikipedia.org/wiki/Alonzo_Church "Alonzo Church") in the 1930s as part of his research into the [foundations of mathematics](https://en.wikipedia.org/wiki/Foundations_of_mathematics "Foundations of mathematics"). In 1936, Church found a formulation which was [logically consistent](https://en.wikipedia.org/wiki/Lambda_calculus#History), and documented it in 1940.

Lambda calculus consists of constructing [lambda terms](https://en.wikipedia.org/wiki/Lambda_calculus#Lambda_terms) and performing [reduction](https://en.wikipedia.org/wiki/Lambda_calculus#Reduction) operations on them. A term is defined as any valid lambda calculus expression. In the simplest form of lambda calculus, terms are built using only the following rules:[[a]](https://en.wikipedia.org/wiki/Lambda_calculus#cite_note-3rules-1)

1. x![{\textstyle x}](https://wikimedia.org/api/rest_v1/media/math/render/svg/d951e0f3b54b6a3d73bb9a0a005749046cbce781): A [variable](https://en.wikipedia.org/wiki/Lambda_calculus#validLambdaVar) is a character or string representing a parameter.
2. (λx.M)![{\textstyle (\lambda x.M)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/79e4067c3f6090d545a422bdc288b35a3352fe83): A [lambda abstraction](https://en.wikipedia.org/wiki/Lambda_calculus#lambdaAbstr) is a function definition, taking as input the bound variable x![{\displaystyle x}](https://wikimedia.org/api/rest_v1/media/math/render/svg/87f9e315fd7e2ba406057a97300593c4802b53e4) (between the λ and the punctum/dot **.**) and returning the body M![{\textstyle M}](https://wikimedia.org/api/rest_v1/media/math/render/svg/913ace920108f7552777e36ac0b7ee3f5093a088).
3. (M N)![{\textstyle (M\ N)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/d51003b457bd295edc4d9f2400117cad8a2153e0): An [application](https://en.wikipedia.org/wiki/Lambda_calculus#anApplic), applying a function M![{\textstyle M}](https://wikimedia.org/api/rest_v1/media/math/render/svg/913ace920108f7552777e36ac0b7ee3f5093a088) to an argument N![{\textstyle N}](https://wikimedia.org/api/rest_v1/media/math/render/svg/0d21d55fc102ec49600d3d5522a59ae4561acc22). Both M![{\textstyle M}](https://wikimedia.org/api/rest_v1/media/math/render/svg/913ace920108f7552777e36ac0b7ee3f5093a088) and N![{\textstyle N}](https://wikimedia.org/api/rest_v1/media/math/render/svg/0d21d55fc102ec49600d3d5522a59ae4561acc22) are lambda terms.

The reduction operations include:

- (λx.M[x])→(λy.M[y])![{\textstyle (\lambda x.M[x])\rightarrow (\lambda y.M[y])}](https://wikimedia.org/api/rest_v1/media/math/render/svg/2e714f725a86a41858c71de7c5d04ebfa2141c9b) : [α-conversion](https://en.wikipedia.org/wiki/Lambda_calculus#%CE%B1-conversion), renaming the bound variables in the expression. Used to avoid [name collisions](https://en.wikipedia.org/wiki/Name_collision "Name collision").
- ((λx.M) N)→(M[x:=N])![{\textstyle ((\lambda x.M)\ N)\rightarrow (M[x:=N])}](https://wikimedia.org/api/rest_v1/media/math/render/svg/bcda4dac6e18fedb6162af13b20557ad282e130f) : [β-reduction](https://en.wikipedia.org/wiki/Lambda_calculus#%CE%B2-reduction),[[b]](https://en.wikipedia.org/wiki/Lambda_calculus#cite_note-beta-4) replacing the bound variables with the argument expression in the body of the abstraction.

If [De Bruijn indexing](https://en.wikipedia.org/wiki/De_Bruijn_index "De Bruijn index") is used, then α-conversion is no longer required as there will be no name collisions. If [repeated application](https://en.wikipedia.org/wiki/Reduction_strategy_\(lambda_calculus\) "Reduction strategy (lambda calculus)") of the reduction steps eventually terminates, then by the [Church–Rosser theorem](https://en.wikipedia.org/wiki/Church%E2%80%93Rosser_theorem "Church–Rosser theorem") it will produce a [β-normal form](https://en.wikipedia.org/wiki/Beta_normal_form "Beta normal form").

Variable names are not needed if using a universal lambda function, such as [Iota and Jot](https://en.wikipedia.org/wiki/Iota_and_Jot "Iota and Jot"), which can create any function behavior by calling it on itself in various combinations.