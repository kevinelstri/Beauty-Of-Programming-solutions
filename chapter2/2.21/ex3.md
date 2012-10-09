假设N = a*b中b是奇数。当a也是奇数时，不妨设b>=a
当a <= b/2+1，N可以写成2a项的和，中间两项分别是b/2, b/2+1
当a >= b/2时，N可以写成b项的和，中间一项是a


这个结论可以很容易得到
那么当a == b/2+1成立的时候，确定的数N就直接可以获得它的最大序列程度k+2了
结合a*b == N，可以得到b^2+2b == 2N b == sqrt(2N+1)-1
那么也就是说，2N+1是一个完全平方数，在65位整数+1范围内 找出最大的完全平方奇数

实际上，可以逆过来，完全平方奇数开方后也是一个奇数，那么找出这样的奇数就是O(1)的事情了
由(K^2 - 1)/2<= 2^64 有K <= sqrt(2^65+1) K <= sqrt(2)*2^32
找出在此条件下最大的奇数，而结果N=(K^2-1)/2，这个数可以被sqrt(2N+1)+1个整数的连续序列和表示
