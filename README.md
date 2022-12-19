# RSA Factoring Challenge

## What is RSA ?

[RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem))  is public key encryption system where two different keys are used in decryption and encryption process. In a public-key cryptosystem, the encryption key is public and distinct from the decryption key, which is kept secret (private). An RSA user creates and publishes a public key based on two large prime numbers, along with an auxiliary value. The prime numbers are kept secret. Messages can be encrypted by anyone, via the public key, but can only be decoded by someone who knows the prime numbers.

The security of RSA relies on the practical difficulty of factoring the product of two large prime numbers, the "factoring problem". Breaking RSA encryption is known as the RSA problem. Whether it is as difficult as the factoring problem is an open question.[3] There are no published methods to defeat the system if a large enough key is used.

RSA is a relatively slow algorithm. Because of this, it is not commonly used to directly encrypt user data. More often, RSA is used to transmit shared keys for symmetric-key cryptography, which are then used for bulk encryption–decryption. 

> source: Wikipedia

## The Given Task

This was a task from our school [ALX Holberton](https://www.alxafrica.com) to write two programes<br>
> First:
Factorize as many numbers as possible into a product of two smaller numbers.

   - Usage: factors <file>
       - where <file> is a file containing natural numbers to factor.
       - One number per line
       - You can assume that all lines will be valid natural numbers greater than 1
       - You can assume that there will be no empy line, and no space before and after the valid number
       - The file will always end with a new line
   - Output format: n=p*q
       - one factorization per line
       - p and q don’t have to be prime numbers
       - See example
   - You can work on the numbers of the file in the order of your choice
   - Your program should run without any dependency: You will not be able to install anything on the machine we will run your program on
   - Time limit: Your program will be killed after 5 seconds if it hasn’t finish
   - Push all your scripts, source code, etc… to your repository
        - we will only run your executable factors
```
$ cat tests/test00
4
12
34
128
1024
4958
1718944270642558716715
9
99
999
9999
9797973
49
239809320265259
$ time ./factors tests/test00
4=2*2
12=6*2
34=17*2
128=64*2
1024=512*2
4958=2479*2
1718944270642558716715=343788854128511743343*5
9=3*3
99=33*3
999=333*3
9999=3333*3
9797973=3265991*3
49=7*7
239809320265259=15485783*15485773

real    0m0.009s
user    0m0.008s
sys 0m0.001s
```

> Second:
	- RSA Laboratories states that: for each RSA number n, there exist prime numbers p and q such that n = p × q. The problem is to find these two primes, given only n.
	- This task is the same as task 0, except:

    - p and q are always prime numbers
    - There is only one number in the files

How far can you go in less than 5 seconds?
Read: [RSA Factoring Challenge](https://alx-intranet.hbtn.io/rltoken/Cn9Lq_kKNpNx4dmvFMuwgQ)
```
$ cat tests/rsa-1
6
$ ./rsa tests/rsa-1
6=3*2
$ cat tests/rsa-2
77
$ ./rsa tests/rsa-2
77=11*7
$ [...]  
$ cat tests/rsa-15
239821585064027
$ ./rsa tests/rsa-15 
239821585064027=15486481*15485867
$ cat tests/rsa-16
2497885147362973
$ ./rsa tests/rsa-16
2497885147362973=49979141*49978553
$ [...]
```

Thankyou for visiting !!
