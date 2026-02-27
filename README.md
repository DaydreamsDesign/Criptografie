# Criptografie

########################################################- Tema 1 -#############################################################
\documentclass[12pt]{article}
\usepackage[utf8]{inputenc}
\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage{amssymb}
\usepackage{verbatim}

\begin{document}

\section*{Exercițiul 1}

\begin{quote}
\emph{„În cazul de față — într-adevăr în toate cazurile de scriere secretă — prima 
întrebare privește limba cifrului; pentru că principiile rezolvării, în special în 
ceea ce privește cifrurile mai simple, depind de geniul idiomului particular și 
variază odată cu acesta. [...] Asumând, așadar, criptograma a fi în engleză, 
primul meu pas a fost să determin literele predominante, precum și pe cele mai puțin 
frecvente. Numărându-le pe toate, am construit următorul tabel:}

Din caracterul 8 apar de 33 de ori \\
; " 26 \\
4 " 19 \\
‡) " 16 \\
*** " 13 \\
5 " 12 \\
6 " 11 \\
†1 " 8 \\
0 " 6 \\
92 " 5 \\
:3 " 4 \\
? " 3 \\
¶ " 2 \\
—. " 1

Acum, în limba engleză, litera care apare cel mai frecvent este e.\textquotedblright

\flushright{— Edgar Allan Poe, \emph{„Cărăbușul de aur”}}
\end{quote}

\section*{Exercițiul 2}

\begin{verbatim}
def itg(n):
    r = 0
    k = 0
    cn = n
    while cn != 0:
        r = r + (cn % 10) * (2 ** k)
        k = k + 1
        cn = cn // 10
    return r

def suma(a, b):
    ai = itg(a)
    bi = itg(b)
    
    s = ai + bi
    r = 0
    p = 1 
    
    while s != 0:
        r = r + (s % 2) * p
        p = p * 10
        s = s // 2
    
    return r

a = 1010
b = 1101
rez = suma(a, b)
\end{verbatim}

\section*{Exercițiul 3}

Fie $n = \log_2 b$ (numărul de biți ai lui $b$) și $k = \log_2 c$ (numărul de biți ai lui $c$).

Complexitatea funcției $a\_la\_b\_mod\_c$: $O(n \cdot k^2) = O(\log b \cdot (\log c)^2)$

\section*{Exercițiul 4}

\begin{align*}
\text{a. } &111100_{(2)} = 0 \cdot 2^0 + 0 \cdot 2^1 + 1 \cdot 2^2 + 1 \cdot 2^3 + 1 \cdot 2^4 + 1 \cdot 2^5 = 0+0+4+8+16+32 = 60 \\
\text{b. } &3B_{(16)} = 11 \cdot 16^0 + 3 \cdot 16^1 = 11 + 48 = 59 \\
\text{c. } &FG_{(26)} = 6 \cdot 26^0 + 5 \cdot 26^1 = 6 + 130 = 136 \\
\text{d. } &400_{(10)} = (15)(10) = PK_{(26)} \\
\text{e. } &ZZ \cdot E = (25)(25) \cdot (4) = (3)(25)(22) = DZW_{(26)}
\end{align*}

\section*{Exercițiul 5}

\[
\begin{aligned}
20^{22} \mod 23 &= (20^2)^{11} \mod 23 \\
&= 400^{11} \mod 23 \\
&= 9^{11} \mod 23 \\
&= (9^{10}) \cdot 9 \mod 23 \\
&= (81^5) \cdot 9 \mod 23 \\
&= 11^5 \cdot 9 \mod 23 \\
&= 11^4 \cdot 11 \cdot 9 \mod 23 \\
&= 121^2 \cdot 99 \mod 23 \\
&= 6^2 \cdot 7 \mod 23 \\
&= 36 \cdot 7 \mod 23 \\
&= 13 \cdot 7 \mod 23 \\
&= 91 \mod 23 \\
&= 22
\end{aligned}
\]

\end{document}
