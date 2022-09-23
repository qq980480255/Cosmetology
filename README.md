
/////////////c++模拟键盘输入//////////
#include <Windows.h>

int main()
{
    Sleep(3000);

    // 模拟点击右键
    mouse_event(MOUSEEVENTF_RIGHTDOWN, 0, 0, 0, 0);
    mouse_event(MOUSEEVENTF_RIGHTUP, 0, 0, 0, 0);

    // 模拟按下'A'键
    keybd_event('A', 0, 0, 0);
    keybd_event('A', 0, KEYEVENTF_KEYUP, 0);

    // 模拟按下 CTRL + F
    keybd_event(VK_CONTROL, (BYTE) 0, 0, 0);
    keybd_event('F', (BYTE)0, 0, 0);

    keybd_event('F', (BYTE)0, KEYEVENTF_KEYUP, 0);
    keybd_event(VK_CONTROL, (BYTE)0, KEYEVENTF_KEYUP, 0);

    getchar();
    return 0;
} 
 
//////////////////////////////
