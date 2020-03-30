# EIE4413_lab


Dear student, 

If you still cannot do the remote login, you may try the following approach:

To connect to the remote PC, student using Windows 10/8.1 may also go to the VDI Gateway link using Internet Explorer 11. Just click the following link:

https://vscc.polyu.edu.hk/RDWeb/Pages/en-US/desktops.aspx

Just have a try.

Daniel Lun
## Q1.1
~~~
x = rand(1,65536);	% Define a random vector x with 65536 elements
y = rand(1,65213);	% Define a random vector y with 65213 elements
tic				% Start to count
fft(x);
t1 = toc			% Record the finish time

tic		 		% Start to count
fft(y);
t2 = toc			% Record the finish time
~~~
## Output
~~~
t1 =

    0.0012


t2 =

    0.0073
~~~
## Q1.2
~~~
x1 = [1,1,1,1,0,0,0,0]
X1 = fft(x1)

x2 = [1,1,-1,0,1,0,-1,1]
X2 = fft(x2)

x3 = [1,1,1,1,-1,-1,-1,-1]
X3 = fft(x3)

x4 = [0,1,1,0,0,-1,-1,-1]
X4 = fft(x4)
~~~
## Output
~~~
>> run('C:\Users\17083046d\Documents\MATLAB\Lab1_17083046d_Q1_2.m')

x1 =

     1     1     1     1     0     0     0     0


X1 =

  Columns 1 through 4

   4.0000 + 0.0000i   1.0000 - 2.4142i   0.0000 + 0.0000i   1.0000 - 0.4142i

  Columns 5 through 8

   0.0000 + 0.0000i   1.0000 + 0.4142i   0.0000 + 0.0000i   1.0000 + 2.4142i


x2 =

     1     1    -1     0     1     0    -1     1


X2 =

    2.0000    1.4142    4.0000   -1.4142   -2.0000   -1.4142    4.0000    1.4142


x3 =

     1     1     1     1    -1    -1    -1    -1


X3 =

  Columns 1 through 4

   0.0000 + 0.0000i   2.0000 - 4.8284i   0.0000 + 0.0000i   2.0000 - 0.8284i

  Columns 5 through 8

   0.0000 + 0.0000i   2.0000 + 0.8284i   0.0000 + 0.0000i   2.0000 + 4.8284i


x4 =

     0     1     1     1     0    -1    -1    -1


X4 =

  Columns 1 through 4

   0.0000 + 0.0000i   0.0000 - 4.8284i   0.0000 + 0.0000i   0.0000 - 0.8284i

  Columns 5 through 8

   0.0000 + 0.0000i   0.0000 + 0.8284i   0.0000 + 0.0000i   0.0000 + 4.8284i

~~~
## Q1.3
~~~
x1 = [1,1,1,1]
X1 = fft(x1,4)
X1 = abs(X1)
subplot(511)
stem(X1)
x2 = [1,1,1,1]
X2 = fft(x1,8)
X2 = abs(X2)
subplot(512)
stem(X2)
x3 = [1,1,1,1]
X3 = fft(x3,32)
X3 = abs(X3)
subplot(513)
stem(X3)
x4 = [1,1,1,1]
X4 = fft(x4,128)
X4 = abs(X4)
subplot(514)
stem(X4)
x5 = [1,1,1,1]
X5 = fft(x5,1024)
X5 = abs(X5)
subplot(515)
stem(X5)
~~~
## Output