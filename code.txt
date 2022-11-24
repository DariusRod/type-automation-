bracket1=18200
bracket2=37000
bracket3=87000
bracket4=180000

rate1=0.19
rate2=0.325
rate3=0.37
rate4=0.45

def inc_tax (x):
    if x<=bracket1:
        return 0
    elif x<=bracket2:
        return "{:.2f}".format((x-bracket1)*rate1)
    elif x<=bracket3:
        return "{:.2f}".format((x-bracket2)*rate2+(bracket2-bracket1)*rate1)
    elif x<=bracket4:
        return "{:.2f}".format((x-bracket3)*rate3+(bracket3-bracket2)*rate2+(bracket2-bracket1)*rate1)
    elif x>bracket4:
        return "{:.2f}".format((x-bracket4)*rate4+(bracket4-bracket3)*rate3+(bracket3-bracket2)*rate2+(bracket2-bracket1)*rate1)
print(inc_tax(50000))
