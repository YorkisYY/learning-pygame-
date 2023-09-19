# learning basic python code to create a calculator. the calculator is applied to BMI, BMR & TEDD

def print_info(name, age, who):
    print(f" {name} is {age} years old")
    print(f" {name} loves {who} so much")

print_info("YY", "26y", who="LL")

#STARTING FROM HERE
def find_max (figure1, figure2, figure3):

    if figure1>=figure2 and figure1>=figure3:
        print(figure1)
    elif figure2>figure3 and figure2>figure1:
        print(figure2)
    else:
        print(figure3)
find_max(0,100,20)


def find_min(figure1,figure2,figure3):
    if figure1<=figure2 and figure1<=figure3:
        print(figure1)
    elif figure2<=fuigure1 and figure2<=figure3:
        print(figure2)
    else:
        print(figure3)
find_min(0,100,20)




def find_max (figure1,figure2,figure3):

    if figure1>=figure2 and figure1>=figure3:
        return figure1
    elif figure2>figure3 and figure2>figure1:
        return figure2
    else:
        return figure3


def find_min(figure1,figure2,figure3):
    if figure1<=figure2 and figure1<=figure3:
        return figure1
    elif figure2<=figure1 and figure2<=figure3:
        return figure2
    else:
        return figure3

def max_min(figure1,figure2,figure3):
    if type(figure1) !=int or type(figure2) !=int or type(figure3) !=int:
        return "plz do what we want"
    else:
        return find_max(figure1,figure2,figure3)-find_min(figure1,figure2,figure3)

find_value = max_min(100,20,98)

print(find_value)


def get_bmi (height,weight):
    height *=0.01
    height **=2
    bmi=round(weight/height,1)
    return bmi
def get_bmr(sex,height,weight,age):
    if sex=="m":
        bmr= height*6.25+weight*10-age*5+5
        bmr = round(bmr, 2)
        return bmr
    elif sex=="f":
        bmr= height*6.25+weight*10-age*5-161
        bmr= round(bmr,2)
        return bmr
def get_tdee(sex,height,weight,age,times):
    bmr=get_bmr(sex,height,weight,age)
    tdee=bmr*times
    tdee=round(tdee,2)
    return tdee
print("welcome to use BMI & BMR & TDEE CALCULATOR")
print("calculate BMI (1)\n calculate BMR (2)\n calculate TDEE (3)")
num=input("the number you like to calculate")
if num=="1":
    height=float(input("your height"))
    weight=float(input("your weight"))
    bmi= get_bmi(height,weight)
    print(f"your BMI is {bmi}")
elif num=="2":
    sex=input("your sex please(m or f)")
    height = float(input("your height"))
    weight = float(input("your weight"))
    age= int(input("your age please"))
    bmr=get_bmr(sex,height,weight,age)
    print(f"your basic metabolic rate is {bmr}")
elif num=="3":
    sex = input("your sex please(m or f)")
    height = float(input("your height"))
    weight = float(input("your weight"))
    age = int(input("your age please"))
    print("(1) no exercise a week\n(2) exercise 1~2 times\n(3) exercise 3~5 times\n(4) exercises 6~7 times\n (5) low cost labor" )
    exer= input("your weekly exercising times")
    times=0
    if exer=="1":
        times=1.2
    elif exer=="2":
        times=1.375
    elif exer=="3":
        times=1.55
    elif exer=="4":
        times=1.725
    elif exer=="5":
        times=1.9
    tdee=get_tdee(sex, height, weight, age, times)
    print(f"your tdee is {tdee}")

