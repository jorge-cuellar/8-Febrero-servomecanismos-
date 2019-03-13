# 8-Febrero-servomecanismos
tarea 2


%% problema 1
syms n
limit((1+1/n)^n, n, inf)

%% problema 2
n=[1 10 100 500 1000 2000 4000 8000];
y=(1+1./n).^n

%% problema 3
a=[2 6; 3 9]; b=[1 2; 3 4]; c=[-5 5; 5 3];
z=zeros(2, 2);
g=[a z z; z b z; z z c]

%% problema 4
f=zeros(1, 50);
f(1)=1;f(2)=1;
for k=3:50
    f(k)=f(k-2)+f(k+1)
end

%% proble 4 seccion b
f=zeros(1,50);q=zeros(1,50);
f(1)=1;f(2)=1;q(1)=1;q(2)=1;
for k=3:50
f(k)=f(k-2)+f(k-1);
q(k)=f(k)/f(k-1)
end

%% problema 5
x=-10:.1:-5;
y=2+sin(x);
z=-5:.1:2;
t=exp(z);
u=2:.1:10;
v=log(u.^2+1);
plot(x,y,z,t,u,v)

%% problema 6
r=10;
A=[5, 2, r; 3, 6, 2*r-1; 2, r-1, 3*r];
b=[2; 3 ; 5];
s=A\b


%% problema 1
syms x a 
solve('2*x+a==5', x)

%% problema 2
syms x a b
solve('x^2+a*b+b==0', x)

%% problema 3
syms x
solve('2*exp(x)+3*cos(x)==0', x)

%% problema 4
syms c y x
y1=2*x-3*c*y;
y2=c*x+2*y;
eqns = [y==5, y1==7];
[sol4_1, sol4_2] = solve(eqns)

%% problema 5
syms x y
y1=3*x^2-2*x+y;
y2=x*y+x;
eqns = [y==7, y1==5];
[sol4_1, sol4_2] = solve(eqns)
