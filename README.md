# assignment2-siddagoni
# Saikumar Siddagoni
###### Raghavendra
It's my me time place, where I had **sambar rice** and **black coffe** many times <br>

*** 

# Directions to the place
Nearest airport is Rajiv Gandhi international airport
1. After coming out of Airport.
    1. Book a cab to destination raghavendra kothapet
    2. After reaching the destination
    3. You can directly walk in without reservation and dine

# list of specific foods items from your location that you would recommend for others
* Chicken Steaks
* Chicken Pulao
* veg Biryani
* Chilly Chicken
* Chicken 65

[link to AboutMe](AboutMe.md) 

***

# SPORTS

Sports are much needed for one who want to be fit and be healthy mentally and physically.<br>

|Activity|Location|Fee|
|--------|--------|---|
|Baseball|Hugesfield|$20|
|Volleyball|Recreation_center|$30|
|Cricket   |Parkway|$5|

***

# Pithy Codes

> "Work is worship. Duty is religion!"- *Puri jaganath* <br>
> "The only one who can stop is you"- *Ayn Rand*

***

# Code Fencing

> Sparse Table is a data structure, that allows answering range queries. <br>

 Precomputation:

```
int st[MAXN][K + 1];
for (int i = 0; i < N; i++)
    st[i][0] = f(array[i]);

for (int j = 1; j <= K; j++)
    for (int i = 0; i + (1 << j) <= N; i++)
        st[i][j] = f(st[i][j-1], st[i + (1 << (j - 1))][j - 1]);
```

Range Sum Queries:

```
long long st[MAXN][K + 1];

for (int i = 0; i < N; i++)
    st[i][0] = array[i];

for (int j = 1; j <= K; j++)
    for (int i = 0; i + (1 << j) <= N; i++)
        st[i][j] = st[i][j-1] + st[i + (1 << (j - 1))][j - 1];

        long long sum = 0;
for (int j = K; j >= 0; j--) {
    if ((1 << j) <= R - L + 1) {
        sum += st[L][j];
        L += 1 << j;
    }
}

```

Range Minimum Queries (RMQ):

```
int log[MAXN+1];
log[1] = 0;
for (int i = 2; i <= MAXN; i++)
    log[i] = log[i/2] + 1;

int st[MAXN][K + 1];

for (int i = 0; i < N; i++)
    st[i][0] = array[i];

for (int j = 1; j <= K; j++)
    for (int i = 0; i + (1 << j) <= N; i++)
        st[i][j] = min(st[i][j-1], st[i + (1 << (j - 1))][j - 1]);

int j = log[R - L + 1];
int minimum = min(st[L][j], st[R - (1 << j) + 1][j]);
```

Let's go to Sparse table datastructure<https://cp-algorithms.com/data_structures/sparse-table.html>





