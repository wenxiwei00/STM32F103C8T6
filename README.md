# STM32F103C8T6
添加库函数
1. 在工程文件夹下面添加library文件夹
2. 找到外设的库函数在哪里。misc是内核库函数，其他都是外设库函数
   ![image](https://github.com/user-attachments/assets/aa10bfc6-3e4b-4719-8965-90ee91fe57fc)
3. 找到2步骤对应的头文件，粘贴到library里面
   ![image](https://github.com/user-attachments/assets/0c87e82d-1992-4a04-8435-7bb6e7241112)
   把文件夹里面添加好的文件添加到工程里面
   ![image](https://github.com/user-attachments/assets/ff88eccb-f6f6-4382-ae47-d9febe58a21c)
4. 有了上面这些外设库，我们还是不能使用，要添加如下三个库和函数到user目录下。这三个是什么作用看如下图片。it.c和it.h是用来配置中断的
   ![image](https://github.com/user-attachments/assets/5f67ed8b-49ce-4bf7-aa38-4be6b7239410)
   ![image](https://github.com/user-attachments/assets/ae3536bc-a428-43c7-a112-0405d1835a0d)

5. 现在我们的User和Libray里面有很多头文件，我们需要让软件知道这个头文件在哪里，所以我们需要在设置里面把他们包含进来。
   ![image](https://github.com/user-attachments/assets/c45f6c6e-c15d-40c4-b42a-7a7a89160be3)
6. 下面我们还要做一步：打开如下.h代码，这个代码表示：只有你定义了USE_STDPERIPH_DRIVER这个字符串后，你使用stm32f10x_conf.h语句时才有效。所以我们要定义它一下，具体操作如下
   ![image](https://github.com/user-attachments/assets/d941aa01-a245-4dea-955d-8d64cda9dc26)
   ![image](https://github.com/user-attachments/assets/112c3dde-53b2-43da-9256-520b422e61b9)
   只有做到了如上，我们的外设库函数才能使用
   ![image](https://github.com/user-attachments/assets/654a9201-6c9a-42f1-8239-4f715adece33)

现在我们就添加完成了库函数，有了库函数，我们就不需要配置寄存器的方式来写代码了。下面第一个图是配置寄存器的当时点亮一个灯，下面第二个图是配置库函数的方式点亮一个灯。
![image](https://github.com/user-attachments/assets/95e716e9-2ab0-4937-acb6-34d8a9048d91)




   
