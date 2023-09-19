# learning-pygame-basic-code
num=input('number please')
print(int(num[0])+int(num[1]))


# F STRING STR() INT() FLOAT() BOOLEAN TRUE FALSE \N CHANGE THE LINE /MAKE SENTENCES BE SEGREGATED/
a1="lovE"
a2="you"
a3=999
print(f"{a1}+{a2}+{a3}")

#PYTHON CALCUALTION INTEGER DIVDED/ ** POWERED % REMAINS

print(4//3)
print(5**2)
print(8%3)
print(round(1.456788, 3)) # after , to which digits
print(round(4/3,2))
num =22
num *=2
num1= float(input("your height plz\n"))
num2= float(input('your weight plz\n'))
print (f"your BMI is {(round(num2/((num1*0.01)**2),0))}")
num1 *=0.01

bmii = round(num2 / ((num1) ** 2), 0)
print(f"your bmi is {bmii} ")

#part2
#if it rains today
#eelse boolean
is_rainy= True
if is_rainy:
    print( "I am going to drive my car")
else:
    print("I am going to my work on foot")

score=6.5
if score>7:
    pritnt("your are going beloved")
else:
    print("everyone says that you are a loser")

#判斷兩值是否相等的話是要用＝＝, = 只代表左值變成右值的邊量 != 不相等的意思 名字有空格不行

name= "lina"
print(name=="lina")
if name=="lina":
    print(" LOVE HER SO MUCH")
else:
    print("get out of here" )

number= int(input("please insert your number"))

if  number%2 ==0:
    print("even")
else:
    print("odd")

# elif ( 否則如果）, nested if （巢狀 if)

score=20
cheat=True
if score>90:
    if cheat:
        print("please do better next time, don't be caught up")
    else:
        print("offer you 100 dollars")
elif score>80:
    print("offer you 50 dollars")
    if cheat:
        print("please do better next time, don't be caught up")
elif score>70:
    print("offer you 30 dollars")
    if cheat:
        print("please do better next time, don't be caught up")
else:
    print("you such a useless crap, give me your soul")
    if cheat:
        print("please do better next time, don't be caught up")

yourheight=float(input("your height\n"))
yourweight=float(input("your weight\n"))
yourheight *=0.01
yourheight **=2
yourbmi= round( yourweight/yourheight, 1)

print(f"Your BMI is {yourbmi}\n")
if yourbmi>35:
    print("fat ass")
elif 30<=yourbmi<35:
    print("half of your body is in a coffin")
elif 27<=yourbmi<30:
    print("obessity is waiting you in the future")
elif 24<=yourbmi<27:
    print("discussting overweighted guy, shame on you")
elif 18.5<=yourbmi<24:
    print("be awared of your weight, you are so close to be a fat ass")
else:
    print("good enough good enough, the walking beauty")

# and or not not = !=

print( 'welcome to use ramen ordering machine')
print("(1)salty type  $220")
print("(2)soy sauce  $240")
print("(3)pork bone  $280")
soup=(input(" please insert 1 or 2 or 3\n"))
big=input("larger potion?, prok bone +$50, others + 30$ ( please insert Y or N")
egg=input("want eggs? + $30 (please insert Y or N")
pork=input(" pork belly? +$60 ( please insert Y or N")
bill=0
if soup=="1":
    bill +=220
elif soup=="2":
    bill +=240
elif soup=="3":
    bill +=280
if big=="Y":
    bill +=50
elif soup=="1"or"2":
    bill +=30
elif big=="N":
    bill +=0
if egg=="Y":
    bill +=30
if pork=="Y":
    bill +=30
if big=="Y"and egg=="Y" and pork =="Y":
    bill -=20
    print(f" add everything minus 20 dollars, the amount is {bill}, thanks for your coming")
else:
    print(f"the amount is {bill}, thanks for your coming")
