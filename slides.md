% Du markdown au beamer
% Romain Vimont (®om)
% 15 février 2014

# Pourquoi ?

## Parce que

- Le code source est lisible
- Il est *git*able
- Le résultat est le même que *Beamer*

## Du code

La coloration de code est très simple.

### Un Hello World!

~~~java
public static void main(String... args) {
    System.out.println("Hello world!");
}
~~~

## Du code numéroté

~~~{.c .numberLines startFrom="5"}
int main(int argc, char *argv[]) {
  printf("Hello world!\n");
  return 0;
}
~~~

## Des énumérations

- Apache
- BSD
- GPL
    - GPLv2
    - GPLv3
- MIT

## Des listes numérotées

1. Récupérer le projet
2. Installer `pandoc`
3. Installer les dépendances
    a. `texlive-latex-base`
    b. `latex-beamer`
4. Installer un lecteur (`impressive`)
5. `make run`

## Des citations

Celle-ci est de [*Mitch Resnick*](https://en.wikipedia.org/wiki/Mitchel_Resnick).

> If you learn to read, you can then read to learn.\
> If you learn to code, you can then code to learn.[^ted]

[^ted]: \tiny<http://www.ted.com/talks/mitch_resnick_let_s_teach_kids_to_code.html>

## Des apparitions

Par étapes :

> - d'abord…
> - ensuite…
> - enfin…

## D'autres apparitions

D'abord un paragraphe…

. . .

Puis un autre

*(ça ne marche pas avec pandoc 1.9.4.2, mais ça marche avec 1.12.2.1, vérifiez
votre version)*

## Mise en forme

| Il y a 2 types de personnes :
|   ceux qui comprennent la récursivité et
|   ceux qui ne comprennent pas qu'il y a 2 types de personnes :
|     ceux qui comprennent la récursivité et
|     ceux qui ne comprennent pas qu'il y a 2 types de personnes :
|       ceux qui comprennent la récursivité et
|       ceux qui…


# Spécial \LaTeX /Beamer

## Du spécifique

Certaines choses n'existent pas nativement en *Pandoc Markdown*, il suffit donc
d'utiliser du \LaTeX.



## Images

Les images sont supportées par *Markdown*, mais on ne peut pas spécifier la
taille. Il est donc pratique d'utiliser directement \LaTeX.

----

\center\includegraphics[scale=0.5]{fonction_0.png}
![une image](images/fonction_0.png)

## Des maths

Avec des formules :

\center$\displaystyle\frac{\pi}{4}=\int_0^1 \sqrt{1-x^2}\mathrm dx$

$$f(x)=\dfrac{1}{x+1}$$

