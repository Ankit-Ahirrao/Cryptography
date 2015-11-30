# Cryptography

[Hard Core Predicate](#hard-core-predicate)

[Euclidean Algorithm](#euclidean-algorithm)

[One time Pad](#one-time-pad)

[Public Key Crptography](#public-key-crytography)

[Diffie-Hellman](#Diffie-Hellman)

[Elliptic Curve](#elliptic-curve)
 
- - - 

## Elliptic Curve 

Elliptic curve cryptography (ECC) is an approach to public-key cryptography based on the algebraic structure of elliptic curves over finite fields. ECC requires smaller keys compared to non-ECC cryptography (based on plain Galois fields) to provide equivalent security.

Elliptic curves are applicable for encryption, digital signatures, pseudo-random generators and other tasks. They are also used in several integer factorization algorithms that have applications in cryptography.

>> Public-key cryptography is based on the intractability of certain mathematical problems. Early public-key systems are secure assuming that it is difficult to factor a large integer composed of two or more large prime factors. For elliptic-curve-based protocols, it is assumed that finding the discrete logarithm of a random elliptic curve element with respect to a publicly known base point is infeasible: this is the **"elliptic curve discrete logarithm problem"**

Elliptic curves are generally in the form:

![Elliptic Curves](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Elliptic%20Curve/Selection_001.png)

Addition in Elliptic Curves:

The way addition and multiplication are performed for Elliptic Curves is shown here:

![addition](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Elliptic%20Curve/Selection_002.png)

The reason for Elliptic Curves will work for finite field is because we need to make sure that if there are two points on the curve, and there is a infinite line drawn to connect two points should also cut a third point. 

Result for addition we get by drawing a vertical line as shown below:

Multiplication is `n * addition` addition is calculated in a really different way in `Elliptic Curves` which means multiplication so powerful!! **"elliptic curve discrete logarithm problem"**

![Addition Result](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Elliptic%20Curve/Selection_003.png)

Now the ECC is applied for Diffie Hellman Crytography. They agree on certain parameters, and share a public key just like normal Diffie Hellman!

![Diffie Hellman Parameters](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Elliptic%20Curve/Selection_004.png)

What each parameters mean here 

![ECC](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Elliptic%20Curve/Selection_005.png)

Alice and Bob calculate their private key by multiplying with `G` which is also known as `Generator Sequence` 

![ECC](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Elliptic%20Curve/Selection_006.png)

Result of Diffie Hellman! Algorithm 

![DF](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Elliptic%20Curve/Selection_007.png)


## Diffie Hellman

There is a problem with symmetric key cryptography 

There are lots of computer on internet which wants to send messages but don't have the shared key, then how will they send the messages?

![Problems](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Diffie%20Hellman/Selection_001.png)

1- First they choose the `blue` color
2- The alice will choose `orange` color, and Bob will choose `green` colors. Not send this over the network
3- Mix the color
4- See the other images for more clarity 

Using colors to understand how diffie hellman algorithm works 

![Colors](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Diffie%20Hellman/Selection_002.png)

Now they will exchange their colors 

![Mix](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Diffie%20Hellman/Selection_003.png)

The final result after mixing should be also be same, as you can see in the above image.

Mathematics Behind `D-H`

Step 1:

![Step1](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Diffie%20Hellman/Selection_004.png)

Step 2:

![Step2](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Diffie%20Hellman/Selection_005.png)


Step 3:

Alice and Bob both will compute the final value of `s` which should be equal

![Step3](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Diffie%20Hellman/Selection_006.png)

Step 4:

This is a `Discrete Logarithm Problem` 

![Step4](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Diffie%20Hellman/Selection_007.png)

## Public Key Crptography

It is also known as `Asymmetric Scheme` since you are using two keys Public and Private

A cryptographic system that uses two keys -- a public key known to everyone and a private or secret key known only to the recipient of the message. When John wants to send a secure message to Jane, he uses Jane's public key to encrypt the message. Jane then uses her private key to decrypt it.

An important element to the public key system is that the public and private keys are related in such a way that only the public key can be used to encrypt messages and only the corresponding private key can be used to decrypt them. Moreover, it is virtually impossible to deduce the private key if you know the public key.

Public-key systems, such as Pretty Good Privacy (PGP), are becoming popular for transmitting information via the Internet. They are extremely secure and relatively simple to use. The only difficulty with public-key systems is that you need to know the recipient's public key to encrypt a message for him or her. What's needed, therefore, is a global registry of public keys, which is one of the promises of the new LDAP technology.
Public key cryptography was invented in 1976 by Whitfield Diffie and Martin Hellman. For this reason, it is sometime called Diffie-Hellman encryption. It is also called asymmetric encryption because it uses two keys instead of one key (symmetric encryption).

![Public Key Cryptography](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Public%20Key%20Cryptography/Selection_001.png)

Both ways we can achieve this. Either using private keys to first encrypt, and then decrypt or vice versa.

![Public Key Cryptography](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Public%20Key%20Cryptography/Selection_001.png) 



## One Time Pad

In cryptography, the one-time pad (OTP) is an encryption technique that cannot be cracked if used correctly. In this technique, a plaintext is paired with a random secret key (also referred to as a one-time pad). Then, each bit or character of the plaintext is encrypted by combining it with the corresponding bit or character from the pad using **modular addition**. If the key is truly random, is at least as long as the plaintext, is never reused in whole or in part, and is kept completely secret, then the resulting ciphertext will be impossible to decrypt or break.It has also been proven that any cipher with the perfect secrecy property must use keys with effectively the same requirements as OTP keys.

Gilbert S. Vernam for the XOR operation used for the encryption of a one-time pad.

`Some of the properties of one time pad`

![One time pad](https://github.com/rakeshsukla53/Cryptography/blob/master/images/One-time-pad/Selection_001.png)

`How one time pad works`

![One time pad](https://github.com/rakeshsukla53/Cryptography/blob/master/images/One-time-pad/Selection_002.png)

Since the letters cannot be added we first need to convert into decimal or binary. Here we converting into decimal and then adding them. If the keys are of same size as of plaintext, and it is truly random then it is almost impossible to decrypt it.

![Modular Addition](https://github.com/rakeshsukla53/Cryptography/blob/master/images/One-time-pad/Selection_002.png)


## Euclidean Algorithm

In mathematics, the Euclidean algorithm[a], or Euclid's algorithm, is an efficient method for computing the greatest common divisor (GCD) of two numbers, the largest number that divides both of them without leaving a remainder

[Euclid Algorithm](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Euclidean%20Algorithm/Selection_002.png)

Application of Euclid Algorithm 

The Euclidean algorithm has many theoretical and practical applications. It is used for reducing fractions to their simplest form and for performing division in modular arithmetic. Computations using this algorithm form part of the cryptographic protocols that are used to secure internet communications, and in methods for breaking these cryptosystems by factoring large composite numbers. The Euclidean algorithm may be used to solve Diophantine equations, such as finding numbers that satisfy multiple congruences according to the Chinese remainder theorem, to construct continued fractions, and to find accurate rational approximations to real numbers. Finally, it is a basic tool for proving theorems in number theory such as Lagrange's four-square theorem and the uniqueness of prime factorizations. The original algorithm was described only for natural numbers and geometric lengths (real numbers), but the algorithm was generalized in the 19th century to other types of numbers, such as Gaussian integers and polynomials of one variable. This led to modern abstract algebraic notions such as Euclidean domains.

  
## Hard Core Predicate 

In cryptography, a hard-core predicate of a one-way function f is a predicate b (i.e., a function whose output is a single bit) which is easy to compute given x but is hard to compute given f(x). In formal terms, there is no probabilistic polynomial-time algorithm that computes b(x) from f(x) with probability significantly greater than one half over random choice of x.

`RSA` is implemented on the same principal

![RSA](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Hard_Core_Predicate/14.png)

`RSA` is also known as one way TRAP door function which means that there is no way to undue the encryption unless there you have the `private key`. 

![Easy to Predict](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Hard_Core_Predicate/9.png)

![Hard to Predict](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Hard_Core_Predicate/8.png)

`private key` is represented by `d` in the below images

`n` is the trap door here. Because of prime factorization it is extremely difficult to find n 

`number` which is greater than 1 can be represented exactly one way as the product of two prime numbers

`15 = 3*5`
 
`255 = 3*5*17`

`n` knowing the factors of n is the trapdoor function 

![Real Life Public Key](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Hard_Core_Predicate/13.png)

[![RSA Video](https://github.com/rakeshsukla53/Cryptography/blob/master/images/Hard_Core_Predicate/1.png)](https://www.youtube.com/watch?v=Z8M2BTscoD4)

So hard core predicate is basically a boolean value which can tell whether the inverse of any function can be done or not in `True` or `False`

There is a difference between `One way function` and `Trap Door Function`. RSA is basically a `Trap Door Function` 

`Hard Core Bit` Predict `easy to compute` given x but `hard to guess` given f(x)








