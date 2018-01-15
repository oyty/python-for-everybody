为了保证函数定义是在函数被第一次调用之前，你必须知道程序中语句的执行顺序，这就是`执行流程`。

程序一般从第一条语句开始执行，然后从上到下依次顺序执行。

函数定义并不会改变程序的执行顺序，但是要记住，函数只有在被调用的时候才会被执行。

函数调用就像是执行流程中的一个迂回，当遇到要调用的函数时，程序不会接着去执行下一句，而是跳到函数体，等执行完函数体里面的语句，在跳回到刚才的地方继续执行。

当你理解了执行流程，就变得很简单了。在一个函数中，程序可能要执行另一个函数的语句，在定义新函数时，程序可能还要执行另一个函数。

所以呢，这里有一个小技巧，有时候没必要从头到尾去阅读程序，按照执行流程来阅读可能更好。