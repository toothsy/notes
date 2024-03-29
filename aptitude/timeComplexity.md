# recursive ones
- #### for these kinda problems you need to see how many function calls are happening
	- #### mergesort
		- here, merging takes takes $O(N)$ time and 
		- dividing takes $O(logN)$, since you half it every time
		- Naturally your tc is  $O(NlogN)$ 
	- #### generate parenthesis
		- here on each function call you're calling twice and it only increases
		- so it increases the tc  exponentially .
		- making the tc at the order $O(2^N)$
# Masters theorem
- ### $T(n) = aT(\frac{n}{b})\ + \theta (n^k \log^pn)) $
- ### where $a \ge 1, b > 1, k\ge 0,\ \  p\  \epsilon $ R
	- #### if $b<1$ then the problem will keep on increasing
	- #### if $k<0$ means the answer is $\propto \frac{1}{input array}$, which kinda dont make sense
- ## Always compare $a$ and $b^k$.
- ## if($a>b^k$)
	- #### $T(n) = \theta(n^k log^pn)$
- ## if($a == b^k$)
	- #### there are 3 cases wrt to p
		- #### $if ( p>-1 )$ then $T(n) = \theta(n^{ \log _{a}b} \log^{p+1}n)$
		- #### $if ( p=-1 )$ then $T(n) = \theta(n^{ \log _{a}b} log\log n)$
		- #### $if ( p<-1 )$ then $T(n) = \theta(n^{ \log _{a}b} )$
- ## if($a<b^k$)
	- #### there are 2 cases wrt to p
		- ### $if ( p\ge 0 )$, then $T(n) = \theta(n^{ k}log^pn )$
		- ### $if ( p\lt 0 )$ , then $T(n) = \theta(n^{ k} )$
