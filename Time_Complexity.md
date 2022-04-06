~~~c
int recursiveFun5(int n)
{
    for (i = 0; i < n; i += 2) {
        // do something
    }

    if (n <= 0)
        return 1;
    else
        return 1 + recursiveFun5(n-5);
}
~~~

Iterative = O(n/2) -> O(n)
Recursive = O(n/5) -> O(n)

O(n*n/2*5)	= O(n^2/10) -> O(n^2)


~~~c
void g(int n) {
	if (n == 1)
		return;
	g(n-1);
	g(n-1);
}
~~~

for n-1 >	 O(2^n-1)	->  O(2^(n/1)) -> O(2^n)
for n-1 = O(2^n-1) 	-> O(2^n)
k -> No of recursive Calls

|
