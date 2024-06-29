# heath_equation
# Resolução da equação do calor utilizando o método das diferenças finitas.

Quando cursei a disciplina de Transferência de Calor, havia uma proposta para resolvermos as equações de calor analiticamente para problemas simples. No entanto, também aprendemos métodos numéricos para resolver algumas equações diferenciais parciais neste contexto. É interessante ver como poderíamos resolvê-las numericamente e visualizar as soluções como se fossem um "mapa", e para isto o Python pode ser utilizado para resolver este tipo de problema.
Antes disso, é necessário termos uma base sobre a equação de calor e o método das diferenças finitas que será utilizado para este artigo. A equação de calor é uma EDP, logo
![image](https://github.com/maiarasalmaso/heath_equation/assets/91421583/46f03fb1-44f2-44ea-861d-b161cf435683)

Em termos do plano cartersiano, esta equação pode ser escrita da seguinte maneira.
![image](https://github.com/maiarasalmaso/heath_equation/assets/91421583/640df791-8f06-4cd7-9b2c-7d90f73db143)

onde u é a o que queremos saber, t é variável temporal, x e y são variáveis espaciais, e α é a constante de difusividade. Então, basicamente, queremos encontrar a solução u em x e y , e ao longo do tempo t .
O método das diferenças finitas é um método numérico para resolver equações diferenciais aproximando a derivada com diferenças finitas dada por
![image](https://github.com/maiarasalmaso/heath_equation/assets/91421583/f45e7ff3-9166-4132-bbbb-a1e41716c181)

No método de diferença finita, nós o aproximamos e removemos o limite. Então, em vez de usar o símbolo diferencial e limite, usamos o símbolo delta que é a diferença finita.
![image](https://github.com/maiarasalmaso/heath_equation/assets/91421583/86bb1f11-36bc-49c3-89cd-c51c15647a61)

Iremos "discretizar" o dominio espacial e o intervalo de tempo, portanto
![image](https://github.com/maiarasalmaso/heath_equation/assets/91421583/8d4d80f5-a9e6-4e26-8048-6f5c1ea9aa9d)

A solução para u que precisamos encontrar é 
![image](https://github.com/maiarasalmaso/heath_equation/assets/91421583/7e3caf9a-2657-496b-bbc2-31a0b849b002)

A equação a cima com o método da diferenças finitas é descrita da seguinte maneira
![image](https://github.com/maiarasalmaso/heath_equation/assets/91421583/5c25ad0c-0f23-405b-ac7f-e7ad5d5cb94b)

que ajustando ostermos, a equação será dada por 
![image](https://github.com/maiarasalmaso/heath_equation/assets/91421583/c9861a47-f451-47d9-b008-d9f995f69b83)

onde
![image](https://github.com/maiarasalmaso/heath_equation/assets/91421583/86481cce-1bc8-484a-a0a2-b758804b7648)

 Exemplo para ser resolvido utilizando o Python
Para um problema numperico, podemos supor uma placa quadrada fina com um lado de 30 unidades de comprimento com a temperatura variando dentro da placa, dada inicialmente por 0°C em t = 0. Vamos considerar considerar Δ x = 1 e α = 2,0

![solucao_equacao_calor](https://github.com/maiarasalmaso/heath_equation/assets/91421583/07dad76f-381d-4d9e-923c-6e6f7fb9e9f6)
