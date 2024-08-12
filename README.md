# micrograd

> [!NOTE]
> one more good ref to understand backprob is by [artem](https://youtu.be/SmZmBKc7Lrs?si=qO0w2biWfroAiRsf)

now lets dive in to andrej implementing micrograd

neural net training under the hood

micrograd implements backpropagation

whats backprop? its an algorithm that evaluates gradient of a loss function with respect to the weights of the nn and that allows us to tune the weights of the nn in such a way that the loss is minimized and in turn improve the accuracy of the nn

`.backward()` initializes backpropagation which recursively apply the chain rule

what does it tell you? it tells you how `a` and `b` are effecting `g` thtough this mathematical expression

for example, if `a.grad() = 138` it tells you that if `a` is slightly tweaked a tiny amount and made larger, `g` will grow and its slope of growth would be 138 

whats derivative? if you slightly bump up the the value `x` by `h`, how does the function responds/what is the slope at the point, does the function go up/down and by how much.

to get the slope, we need to have rise (`f(x + h) - f(x)`) over run(`h`)

when the slopes zero, if we nudge `x` by some anount, the function doesn't respond much
