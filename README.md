
# MSM_ICBC2023

Credit: This is developed on top of a modified blst library. Check the original library at [blst library](https://github.com/supranational/blst).



## Compilation
The code is tested on intel Mac OS, on M1 Mac OS, and on intel ubuntu. They can be compiled and run using the same commands as explained below. Note MSM_ICBC2023 is not compatible with the original blst library since some of the source code in blst has been modified. 

After downloading the compressed file and uncomrepssing it, in the terminal under 
<code>
MSM_ICBC2023
</code>
folder,
one first runs 
<code>
./build.sh
</code>
to build the modified blst library, then runs

<pre><code>
g++ -std=c++17 -o main_test -g -O2 main_p1.cpp libblst.a
</code></pre> 
or 
<pre><code>
g++ -std=c++17 -o main_test -g -O2 main_p2.cpp libblst.a
</code></pre> 

to complie the corresponding benchmark over
<code>
G_1 
</code>
or
<code>
G_2
</code>
respectively.

Type in
<pre><code>
./main_test
</code></pre> 
to run the experiment.

## Configuration
In 
<code>
main_p1.cpp
</code>
or 
<code>
main_p2.cpp
</code>
there is a 
<pre><code>
/***----***
Configuration
***----***/
</code></pre> 
snippet. One can adjust the integer 
<code>
xx (10 <= xx <= 22)
</code>
in the line 
<pre><code> 
#include "config_files/config_file_n_exp_xx.h" 
</code></pre> 
to run the code for different number of points
<code> 
n = 2^{xx}.
</code>
