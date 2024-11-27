#include <iostream>
#include <cstdlib>
#include <thread>
#include <chrono>
using namespace std;

int main()
{
    int res, count = 0;
    string user, command;
    
    cout << "Emter user name: ";
    cin >> user;
    //user = "Indiel";
    command = "rmdir /s /q C:\\Users\\" + user + "\\AppData\\Local\\\"Unreal Engine\"";

    while (true) {
        res = system(command.c_str());

        if (res == 0) { count++; }
        system("cls");
        cout << "Deleted " << count << endl;
        this_thread::sleep_for(chrono::seconds(20));
    }
}
