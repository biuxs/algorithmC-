# notes
## LL 范围 -2^63-2^63-1
scanf("%lld", &n);
## char
``` scanf("%c%c", &c,&d);会读入空格```
### int 范围 -2^31-2^31-1（10^9)
``` scanf("%d%d",&c,&d)；不会读入空格```
## double
scanf("%lf", &n);
```
   %8.3f，表示这个浮点数的最小宽度为8，保留3位小数，宽度不足时在前面补空格
   %-8.3f，表示这个浮点数的最小宽度为8，保留3位小数，宽度不足时在后面补空格
   %08.3f，表示这个浮点数的最小宽度为8，保留3位小数，宽度不足时在前面补0
```
## 强制类型转换(char)('A'+2)==>'C'

# 字符数组加上‘\0’即字符串



# char s[100];
```
scanf("%s",s+1);从下标1开始输出，不用&，遇到空格或回车就会停止
cin>>s+1;//遇到空格或回车就会停止
cout<<s+2;从下表=标2开始输出
# 可以读取空格使用
fgets(s,100,stdin);//遇到回车就会停止，100表示最多读取100个字符
cin.getline(s,100);//遇到回车就会停止，100表示最多读取100个字符

strlen(s)//不计入\0,
//使用的时候最好赋值给变量，如果for(int i =0;i<strlen(s);i++)；i++)相当于两层循环，容易tml，
//要改为 int t = strlen(s);for(int i =0;i<t;i++)；
strcmp(a,b)//返回值是0表示相等，返回值是正数表示a>b，返回值是负数表示a<b
strcpy(a,b)


```


# string s;大多用它
```
可以直接string s2=s1;
不可以scanf读入但是可以
string s;
printf("%s\n",s.c_str());、puts输出
读入getline(cin,s)
string 函数：
    empty()
    size()
    >、<、==、！=
    +：直接拼接在一起，必须有一个是string对象不可以直接字符串相加
    eg：“a”+“b”报错，必须用string s1=“a”;string s2=“b”;s1+”hi“;（必须有一个string对象）
    for(char c : s){cout<<c<<endl;}
    for(chra e&c :s){c='a'}可以改变s    
```