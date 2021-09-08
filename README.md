# assignment2-veeravelly
# Saikrishna veeravelly
###### Nalgonda

 The place which i like the most in the world is Nalgonda because i had my childhood over there and i had been in that place from my birth and my **parents** live there and i like my **house** which has a big garden in it, I love spending time in doing gardening.
 
 ---
 # Directions to Chicago
 1. Take a cab from the place you stay in maryville
 2. Head towards the nearest airport
 3. Catch the flight to chicago
     1. go through the secuirty check
     2. go ahead and complete your bag checking
     3. findout the terminal wait until they give a call
     4. Board the fligt            
 4. After landing find a taxi and go out to explore the places in chicago.

 * phone
 * sunglasses
 * hat 
 
 [AboutMe](https://github.com/veeravelly96/assignment2-veeravelly/blob/main/AboutMe.md)

---
# My Favourite food and drinks

The following given table shows the list of my favourite foods/drinks and where they are available.

| **Foods/drinks**             |**Location**|**Cost($)**|
|:----------------------------:|:----------:|:---------:|
| hyderabd dum biryani         |Hyderabad   |10         |
| Ram ki dosa                  |Hyderabad   |7          |
| Gokul chat                   |Hyderabad   |5          |
| fried egg maggie             |Hyderabad   |4          |
---
# Quotes
> Powerfull people comes from the powerfull place. - *KGF*

> The unexamined life is not worth living. - *Socrates*
---
# Code Fencing
## Combinatorics
> Combinatorics is an area of mathematics primarily concerned with counting, both as a means and an end in obtaining results, and certain properties of finite structures. It is closely related to many other areas of mathematics and has many applications ranging from logic to statistical physics, from evolutionary biology to computer science, etc. <br>
<https://en.wikipedia.org/wiki/Combinatorics>

* Techniques
    * The Inclusion-Exclusion Principle<br>
```
int solve (int n, int r) {
    vector<int> p;
    for (int i=2; i*i<=n; ++i)
        if (n % i == 0) {
            p.push_back (i);
            while (n % i == 0)
                n /= i;
        }
    if (n > 1)
        p.push_back (n);

    int sum = 0;
    for (int msk=1; msk<(1<<p.size()); ++msk) {
        int mult = 1,
            bits = 0;
        for (int i=0; i<(int)p.size(); ++i)
            if (msk & (1<<i)) {
                ++bits;
                mult *= p[i];
            }

        int cur = r / mult;
        if (bits % 2 == 1)
            sum += cur;
        else
            sum -= cur;
    }

    return r - sum;
}
```
<https://cp-algorithms.com/combinatorics/inclusion-exclusion.html>
    
 
