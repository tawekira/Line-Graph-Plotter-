## Why use Line Graph Plotter?
Line Graph Plotter allows for extensive customisation of many features in order to suit specific needs, beautify your graphs and make data visualisation pleasant to the eye. 

![image](https://user-images.githubusercontent.com/82096960/122642884-3a86f500-d13f-11eb-8f9a-f7631020defa.png)
##### Sample Graph

### Features
1. 

### Code
```markdown
import matplotlib.pyplot as plt
import seaborn as sns

additional = input("Change Theme Y/N: ")
if additional == "Y":
    theme = input("Choose theme: \n 1.darkgrid - d"
                                "\n 2.whitegrid - w"
                                "\n 3.dark - D"
                                "\n 4.white - W"
                                "\n 5.ticks - T"
                                "\n:")
    if theme =="d":
        sns.set_style("darkgrid")

    if theme =="w":
        sns.set_style("whitegrid")

    if theme =="D":
        sns.set_style("dark")

    if theme =="W":
        sns.set_style("white")

    if theme =="T":
        sns.set_style("ticks")

title = input("Graph title: ")
plt.rcParams.update({'font.family':'sans-serif'})
plt.title(title)

x_axis = input("x-axis label: ")
y_axis = input("y-axis label: ")
plt.xlabel(x_axis)
plt.ylabel(y_axis)

title_font_size = input("Title font size: ")
plt.title(title, size=title_font_size)

x_axis_label_fs = input("X-axis label font size: ")
plt.xlabel(x_axis, size=x_axis_label_fs)

y_axis_label_fs = input("Y-axis label font size: ")
plt.ylabel(y_axis, size=y_axis_label_fs)


number = int(input("How many graphs would you like to plot? "))
Legend =[]

for i in range(number):
    x_coordinates = []
    y_coordinates = []
    userinput = int(input("Number of coordinates: "))
    y=1
    for x in range(userinput):
        userinput1 = int(input("x-coordinate of point "+str(y)+":"))
        x_coordinates.append(userinput1)
        userinput2 = int(input("y-coordinate of point "+str(y)+":"))
        y_coordinates.append(userinput2)
        y +=1


    marker_type = input("Marker type: \n"
                    "0 - 0 \n"
                    "x - x \n"
                    ":")
    if marker_type == "o":
        a= "o"

    if marker_type == "x":
        a= "x"

    b = input("Choose Line colour: \n"
                        "Red - r \n"
                        "Blue - b \n"
                        "Green - g \n"
                        "Cyan - c \n"
                        "Magenta - m \n"
                        "Yellow - y \n"
                        "Black - B \n"
                        "White - w \n"
                        ":")


    line_stye = input("Choose Line style: \n"
                     "1.Solid - S \n"
                     "2.Dotted - D \n"
                     "3.Dashed - d \n"
                     "4.Dashdot - Dd \n"
                     ":")
    if line_stye == "S":
        c="-"
    if line_stye == "D":
        c=":"
    if line_stye == "d":
        c=":"
    if line_stye == "Dd":
        c="-."

    line_width = input("Choose Line width: ")
    plt.plot(x_coordinates, y_coordinates, marker=marker_type, c=b, ls=c, lw=line_width)
    x = input("Input legend: ")
    Legend.append(x)
    number -= 1


plt.legend(Legend)

plt.show()
```
