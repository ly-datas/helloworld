## 实验二-Android布局

实验准备：创建一个空项目工程，基本步骤同于实验一，不再赘述。创建项目完成后，在res/layout下创建3个布局文件：线性布局linear_layout.xml、约束布局constraint_layou.xmlt和表格布局table_layout.xml(如下图所示)

<img src="https://i.loli.net/2020/11/01/Vk9oFPbWIYzvQLD.png" alt="`2JY_IV2ZELHMPA__`78`BT.png" style="zoom: 50%;" />

接着，开始对每一个布局文件一一进行设计。

#### 一、线性布局

1、线性布局中，页面上的组件都要写在<LinearLayout></LinearLayout>中，这里只用到了按钮组件Button。

页面的基本思想就是：整体上一行行沿垂直方向布局，其中每一行中的按钮沿水平方向布局。（代码比较长，就不完整粘贴了）

![O_TBKFENT_F5FJ~WAGXFU`4.png](https://i.loli.net/2020/11/02/H4njBEOrh8WJaZk.png)

至于Button边框的实现，通过定义一个button_style.xml文件进行装饰，最后在<Button>属性里加上android:background="@drawable/button_style"即可实现。

button_style.xml文件如下：

<img src="https://i.loli.net/2020/11/02/IFzcmWx32PfBpa9.png" alt="DS7W____3`JLX8ODMRP1FFC.png" style="zoom:50%;" />



2、除了规规矩矩地手写代码外、布局也可以直接通过design手动拖拽组件布局，简单方便。

<img src="https://i.loli.net/2020/11/02/LG1difBSHMlXEO7.png" alt="LRQ08_PC27UK8S_`XC_58PG.png" style="zoom:50%;" />

3、但不管是手写代码，还是通过design拖拽组件，给组件添加text时，都不能直接在 xml 文件里面写（编译器会有提示不建议采用hardcode），规范的写法应该是在 strings.xml 文件中，声明定义好需要的组件的id和text值,然后在布局文件里直接调用（声明如下图）

<img src="https://i.loli.net/2020/11/01/PLXoIR9QBYc6dpi.png" alt="J7P8GH5G3T_0VP142_7VTHO.png" style="zoom: 50%;" />

4、编写完linear_layout和string.xml两个xml文件后。回到MainActivity.java文件中，设置项目编译运行打开的布局文件为Linear_Layout文件，而不是原项目默认的activity_main.xml文件（当然如果你是在activity_main.xml中编写的线性布局代码的话，就不用改了）。

![YYCN@_FI_5V6OZ8NDGP_8VA.png](https://i.loli.net/2020/11/01/91bHnkVOjA3Yg8a.png)

5、做完上述操作后，编译运行整个项目，打开模拟器，就会看到最终页面效果（如下图）

<img src="https://i.loli.net/2020/11/02/mHA7o6FdOqWgjpV.png" alt="T_RUX329AOP8N99_PDDITCR.png" style="zoom:50%;" />



#### 二、约束布局

1、约束布局同样，页面上的组件都要写在<ConstraintLayout></Constraintayout>中，这里的矩形图案用TextView组件实现。

<img src="https://i.loli.net/2020/11/01/El9sqYBLUKhrufA.png" alt="9N_ENWGFB~B0G5W_L`4@1E7.png" style="zoom:80%;" />

注：约束布局要求每个组件，都必须为其设置水平、垂直两个方向上的约束。（代码比较长，就不完整粘贴了）

2、直接通过design手动拖拽组件布局，设计页面如下：

<img src="https://i.loli.net/2020/11/01/8eXilM29kqDBZfW.png" alt="_J2_VFXAKLFVW8`U0_QVMU8.png" style="zoom:80%;" />

3、布局完基本组件位置后也一样，给组件添加text时，都不能直接在 xml 文件里面写，在 strings.xml 文件中，声明定义好需要的组件的id和text值,然后在布局文件里直接使用（声明如下图）

<img src="https://i.loli.net/2020/11/01/XP38yqdiH2z6mtB.png" alt="L_K0D0_H~F@4_X~MUH_3_1Y.png" style="zoom:50%;" />

4、在MainActivity.java文件中，设置项目编译运行打开的布局文件为constraint_layout文件，而不是原项目默认的activity_main.xml文件（当然如果你是在activity_main.xml中编写的线性布局代码的话，就不用改了）。

![_CEWG_FLQL~W__5IJ5JMRVD.png](https://i.loli.net/2020/11/01/PwDUKz8bLO5oHiW.png)

5、做完上述操作后，编译运行整个项目，打开模拟器，就会看到最终页面效果（如下图）

<img src="https://i.loli.net/2020/11/01/LPED7QGriO3zaRy.png" alt="WMPO9XXZ@_2N_Z`SKZ7@__Y.png" style="zoom: 50%;" />

#### 三、表格布局

1、表格布局也是，页面上的组件都要写在<TableLayout></TableLayout>中，这里用到了按钮组件Button和TextView组件。

<img src="https://i.loli.net/2020/11/01/cYaVjdT1mXoh8fw.png" alt="U_@GJM3A@___@WG0J@LVIEK.png" />

表格布局需要设定行<TableRow>,行里面的组件个数就是列个数。

需要说的是，页面上的分割线，用了2dp高，背景颜色为#3c3c3c的TextView组件实现。

<img src="https://i.loli.net/2020/11/01/GI2Skz6HsJ4Vna3.png" alt="_60QJ7Z~X`_Z4XRW5EIYJ_K.png" style="zoom:50%;" />

（代码比较长，就不完整粘贴了）

2、在design中，设计页面如下：

<img src="https://i.loli.net/2020/11/01/r8JZiG3QzT19jCl.png" alt="YK7_IPAQ_SS7F_HCL__874Q.png" style="zoom:50%;" />

3、在 strings.xml 文件中，声明定义好需要的组件的id和text值,然后在布局文件里直接调用（声明如下图）

![CS_`K21ZXL__D_XN_7TV_D8.png](https://i.loli.net/2020/11/01/wHYsbvMEglK4c1X.png)

4、在MainActivity.java文件中，设置项目编译运行打开的布局文件为table_layout文件，而不是原项目默认的activity_main.xml文件。

<img src="https://i.loli.net/2020/11/01/14l6u7JctfsNMnd.png" alt="GQF_@K___BR~C__XGES_V_9.png" style="zoom:50%;" />

5、做完上述操作后，编译运行整个项目，打开模拟器，就会看到最终页面效果（如下图）

<img src="https://i.loli.net/2020/11/01/PETd7SDY6OIfvK4.png" alt="_SVV_K__8_~GGRF4PX6AD_L.png" style="zoom:50%;" />

#### 四、项目打包上传Github

具体的打包上传步骤跟实验一中的“**五、使用Git将本地项目资源打包上传到Github远程仓库**”一样，不再赘述。

#### 五、总结

学会了在Android Studio中，使用线性布局、约束布局、表格布局三种主要设计页面布局方式。了解每一种布局方式的基本原理。
