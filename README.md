# C-p30-3-
C 语言学习笔记 p30 数据的存储(3)
#include<stdio.h>
int main()
{
    char a[1000];
    int i;
    for(i=0;i<1000;i++)
    {
        a[i]=-1-i;
    }
    printf("%d",strlen(a));
    return 0;
}//输出为255，遇到0停止打印
unsigned char i=0;
int main()
{
    for(i=0;i<=255;i++)
    {
        printf("hello world\n");
    }
    return 0;
}//死循环，因为unsugned char最大值为255于条件恒成立

//符点型在类型中的存储
int main()
{
    double d=1E10;
    printf("%lf\n",d);
    return 0;
}

int main()
{
    int n=0;
    float* pFloat=(float*)&n;
    printf("n的值为：%d\n",n);
    printf("pFloat的值为：%f\n",pFloat);

    *pFloat=9.0;
    printf("num的值为：%d\n",n);
    printf("pFloat的值为：%f\n",*pFloat);
    return 0;
}//由于浮点型和整形在内存中存储差异不同，所以输出的值差别也很大具体内容参看下节
