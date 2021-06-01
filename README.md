# The ineffable, sublime beauty of working with arrays in python 


Let's imagine I have an array called `thing`. Before I start writing the code that will work on the array, I probably want to do the following:

- I want to figure out what type `thing` is
- I want to know the size of `thing`. How big is it?
- I want to know the length of `thing` 
- I want to know the mean value in `thing`
- I want to quickly `diff` `thing`, for reasons
- I also want to know what the type of the data within `thing` is.

The good news is that `python` and `numpy` give you powerful tools to get this info. Let's see how consistent and inutitve the experience of getting this information is in python:

| What I want | `foo(thing)` | `np.foo(thing)` | `thing.foo` | `thing.foo()` |
| ------------ | ---------- | --------  | ----------- | ---- |
| type         | ✅    | ❌     |    ❌     | ❌ |
| shape        | ❌ |  ✅      |  ✅   | ❌ | 
| len         | ✅ | ❌| ❌ |  __ ✅ __ |
| mean        |  ❌        |  ✅ | ❌  | ✅ | 
| diff        |  ❌ | ✅  | ❌ | ❌| 
| dtype |       ❌         |  ❌              |  ✅       |  ❌ |


Wow, that's so intuitive! This is why they say python is an easy to learn language. I'm so grateful to the people who designed this because this presents the best possible user experience. Note that not **every** row is unique. There is no pattern here. It's a thing of beauty. 

Let's make a similar table for for inferior languages like MATLAB. (I'm assuming `thing` is a matrix):  

| What I want | `foo(thing)`  | `thing.foo` | `thing.foo()` |
| ------------ | ---------- | ----------- | ------------ |
| class         | ✅        |   ❌        |    ❌     |
| size        | ✅          |  ❌        | ❌ | 
| length        | ✅ | ❌| ❌ |
| mean        |  ✅        |❌  | ❌  | 
| diff        | ✅ | ❌ | ❌ | 

How boring. Now I won't have to spend half my day on stack overflow. 

And here's a similar table for Julia. I'm assuming `thing` is a `Matrix{Float64}`, and we are `using Statistics`


| What I want | `foo(thing)`  | `thing.foo` | `thing.foo()` |
| ------------ | ---------- | ----------- | ------------ |
| typeof         | ✅        |   ❌        |    ❌     |
| size        | ✅          |  ❌        | ❌ | 
| length        | ✅ | ❌| ❌ |
| mean        |  ✅        |❌  | ❌  | 
| diff        | ✅ | ❌ | ❌ | 

Julia, too dissapoints and is horribly boring and predictable. How are we supposed to get any work done with languages like this?
