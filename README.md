# Markdown-Learn-Record

这是我学习 **Markdown** 的时候的学习记录，我用 **Markdown** 记录了 在markdown中所学到的知识点

## 仓库内容说明
1. **basic\.md** 是我练习的痕迹
2. **markdown\.md** 是我学习到的知识点
3. **image** 文件夹下是一些我学习markdown时用到的图片，图片是从网上随便搜的，没有版权问题
3. **README\.md** 是git仓库的说明文件

## 学习资源
[B站UP主青空の霞光的教学视频]( https://www.bilibili.com/video/BV1eJ4m157kC/?spm_id_from=333.337.search-card.all.click&vd_source=dbfefd0cc37b2895be48a923d6db2d8d "UP主是：青空の霞光")

## 嵌入点代码试试看

```c
    void MCU_Init(void)
    {
        //初始化代码
        LED_Init();
        KEY_Init();
        Music_Init();
        Touch_Init();
        Motor_Init();
        Servo_Init();
        Camera_Init();
        WiFi_Init();
        Bluetooth_Init();
        GPS_Init();
        RFID_Init();
        NFC_Init();
        Infrared_Init();
        Ultrasonic_Init();
        Accelerometer_Init();
        Gyroscope_Init();
        Compass_Init();

        //创建任务
        xTaskCreate(vTask_PlayMusic, "Task_PlayMusic", 100, NULL, 1, NULL);
        xTaskCreate(vTask_ReceiveData, "Task_ReceiveData", 100, NULL, 1, NULL);
        xTaskCreate(vTask_SendData, "Task_SendData", 100, NULL, 1, NULL);
        xTaskCreate(vTask_ControlLED, "Task_ControlLED", 100, NULL, 1, NULL);

        //启动调度器
        vTaskStartScheduler();

        //如果任务创建失败，则进入死循环
        while( 1 );
    }
```

