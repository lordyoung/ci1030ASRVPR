1. For detailed information about the SDK's components, features, and development, please refer to the SDK documentation for the corresponding chip series in the Software Development section of the Docume
   Taking CI13060 as an example, the reference link is as follows: https://document.chipintelli.com/%E8%BD%AF%E4%BB%B6%E5%BC%80%E5%8F%91/SDK/CI130X%E8%8A%AF%E7%89%87SDK/CI-SDK-Offline/

2. If you need to modify and adjust the relevant algorithm parameters in the SDK, please refer to the SDK documentation for the corresponding chip series in the Software Development section of the Documentation Center.
   Taking AEC as an example, the reference link is as follows:：https://document.chipintelli.com/%E8%BD%AF%E4%BB%B6%E5%BC%80%E5%8F%91/SDK/CI130X%E8%8A%AF%E7%89%87SDK/components/%E5%9B%9E%E5%A3%B0%E6%B6%88%E9%99%A4%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E/

3. If the firmware size exceeds the flash capacity of the selected chip, please try again after switching to a smaller acoustic model, reducing the number of command words or voice prompts, or using a chip with larger flash capacity.

4. If algorithms are enabled, the system provides relatively less memory space for language model. To ensure normal recognition operation, please reduce the number of command words.


The firmware communication protocol is as follows:
小屁开门:A5 FA 00 81 01 00 21 FB:A5 FA 00 82 01 00 22 FB
小屁开盟:A5 FA 00 81 02 00 22 FB:A5 FA 00 82 02 00 23 FB
小批开门:A5 FA 00 81 03 00 23 FB:A5 FA 00 82 03 00 24 FB
小批开盟:A5 FA 00 81 04 00 24 FB:A5 FA 00 82 04 00 25 FB
小屁锁车:A5 FA 00 81 05 00 25 FB:A5 FA 00 82 05 00 26 FB
小批锁车:A5 FA 00 81 06 00 26 FB:A5 FA 00 82 06 00 27 FB
注册声纹:A5 FA 00 81 07 00 27 FB:A5 FA 00 82 07 00 28 FB
删除声纹:A5 FA 00 81 08 00 28 FB:A5 FA 00 82 08 00 29 FB
确定删除:A5 FA 00 81 09 00 29 FB:A5 FA 00 82 09 00 2A FB
删除全部声纹:A5 FA 00 81 0A 00 2A FB:A5 FA 00 82 0A 00 2B FB
<删除成功>:A5 FA 00 81 0B 00 2B FB:A5 FA 00 82 0B 00 2C FB
<注册成功>:A5 FA 00 81 0C 00 2C FB:A5 FA 00 82 0C 00 2D FB
<请再说一次>:A5 FA 00 81 0D 00 2D FB:A5 FA 00 82 0D 00 2E FB
<重复录入失败>:A5 FA 00 81 0E 00 2E FB:A5 FA 00 82 0E 00 2F FB
<请先注册声纹>:A5 FA 00 81 0F 00 2F FB:A5 FA 00 82 0F 00 30 FB
<删除失败>:A5 FA 00 81 10 00 30 FB:A5 FA 00 82 10 00 31 FB
<注册失败>:A5 FA 00 81 11 00 31 FB:A5 FA 00 82 11 00 32 FB
<电量低>:A5 FA 00 81 12 00 32 FB:A5 FA 00 82 12 00 33 FB
<识别失败>:A5 FA 00 81 13 00 33 FB:A5 FA 00 82 13 00 34 FB
<欢迎语>:A5 FA 00 81 14 00 34 FB:A5 FA 00 82 14 00 35 FB
<休息语>:A5 FA 00 81 15 00 35 FB:A5 FA 00 82 15 00 36 FB
