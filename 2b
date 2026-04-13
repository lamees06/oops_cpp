#include <iostream>
#include <string>
using namespace std;

class String
{
    char* str;
public:
    String(const char* s)
    {
        int len = 0;
        while (s[len] != '\0')
        {
            ++len;
        }
        str = new char[len + 1];
        for (int i = 0; i < len; ++i) {
            str[i] = s[i];
        }
        str[len] = '\0';
    }
    String(const String& other)
    {
        int len = 0;
        while (other.str[len] != '\0')
        {
            ++len;
        }
        str = new char[len + 1];
        for (int i = 0; i < len; ++i)
        {
            str[i] = other.str[i];
        }
        str[len] = '\0';
    }
    ~String()
    {
        delete[] str;
    }
    const char* getStr() const
    {
        return str;
    }
    void printSpacedString() const
    {
        for (int i = 0; str[i] != '\0'; ++i) {
            cout << str[i] << " ";
        }
        cout << endl;
    }
};
string findVowels(const String& s)
{
    string vowels = "";
    const char* str = s.getStr();
    for (int i = 0; str[i] != '\0'; ++i)
    {
        char ch = str[i];
        if (ch == 'a' || ch == 'A' ||ch == 'e' || ch == 'E' ||ch == 'i' || ch == 'I' ||ch == 'o' || ch == 'O' ||ch == 'u' || ch == 'U')
        {
            vowels += str[i];
        }
    }
    return vowels;
}

int main() {
    string input;
    cout << "Enter a string: ";
    getline(cin, input);
    String s(input.c_str());
    s.printSpacedString();
    string vowels = findVowels(s);
    cout << "Vowels: " << vowels << endl;
    cout << "Number of vowels: " << vowels.length() << endl;
    return 0;
}
