---
layout: post
title: Different notes
---

Some tips for linux, vim and others

##Linux:

  Add swap file:
  
    $sudo fallocate -l 2g /mnt/2GB.swap
    sudo chmod 600 /mnt/2GB.swap  
    sudo mkswap /mnt/2GB.swap
    sudo swapon /mnt/2GB.swap

*Build and run:*

    $ clang++ -std=c++14 main.cpp
    $ ./a.out
    i=1, c=a, d=2.3
    tuple<0>=2

#### C++17
##Vim:

Close current buffer in split

    :bd | bp #

This could be added to vimrc:

    command Bd bp\|bd \#

```cpp
#include <iostream>
#include <tuple>

int main()
{
    auto tuple = std::make_tuple(1, 'a', 2.3);

    // unpack the tuple into its individual components
    auto& i = std::get<0>(tuple);
    auto& c = std::get<1>(tuple);
    auto& d = std::get<2>(tuple);

    std::cout << "i=" << i << ", c=" << c << ", d=" << d << '\n';

    // change the value of i inside the tuple
    i = 2;

    // show that the value inside the tuple has changed
    std::cout << "tuple<0>=" << std::get<0>(tuple) << '\n';

    return 0;
}
```

####To read:
https://github.com/draperlaboratory/fracture/wiki/How-An-IR-Statement-Becomes-An-Instruction
http://eli.thegreenplace.net/2013/02/25/a-deeper-look-into-the-llvm-code-generator-part-1#id1
http://www.agner.org/optimize/optimizing_cpp.pdf
http://arktur04.github.io/books/ -> books list
