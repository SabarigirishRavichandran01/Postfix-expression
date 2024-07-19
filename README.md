exp=input()
stack=[]
for i in range(0,len(exp)):
    if (exp[i]>='0' and exp[i]<='9'):
        stack.append(int(exp[i]))
    else:
        v1=stack.pop()
        v2=stack.pop()
        if(exp[i]=='+'):
            stack.append(v2+v1)
        elif(exp[i]=='-'):
            stack.append(v2-v1)
        elif(exp[i]=='*'):
            stack.append(v2*v1)
        elif(exp[i]=='/'):
            stack.append(v2//v1)
print(stack.pop())
