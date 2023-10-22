<h1 style="color:white;">Hi, im STOJANOVICLJUBINKO</h1>

![alt text](https://raw.githubusercontent.com/stojanovicljubinko/stojanovicljubinko/main/Snimak%20ekrana%202023-10-22%20134753.png)

```c
#include <conio.h>

int main() {
    // Restart my router when it gets disconnected
    system("router restart");

    // Punch my case when its fan starts making funny noises
    system("punch case");

    // Write code that only I can read
    // - No capital letter
    // - No space or tab
    // - No multi-line code (prefer everything in one line)
    char myCode[] = "codelikecodesnake";

    // Prefer to use Notepad as an IDE
    // I do not use a compiler, real legends write zeros and ones
    // When the code does not work for me, I download someone else's and upload it to GitHub
    // Typing keyboard Serbian Cyrillic
    printf("Legendary programmer in action!\n");

    return 0;
}
```

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>
#include <stdbool.h>
#include <time.h>

typedef struct {
    void (*action)();
    char* name;
} Action;

void routerRestart() {
    if (rand() % 2 == 0) {
        system("router restart");
    }
}

void punchCase() {
    if ((2 >> 1) & (3 | 1) || ((~1) ^ (1 << 0)) == true) {
        system("punch case");
    }
}

char* obfuscateCode(char* code) {
    int codeLength = strlen(code);
    char* obfuscatedCode = (char*)malloc(sizeof(char) * (codeLength + 1));
    for (int i = 0; i < codeLength; i++) {
        obfuscatedCode[i] = isupper(code[i]) || isspace(code[i]) || isdigit(code[i]) ? 'x' : code[i];
    }
    obfuscatedCode[codeLength] = '\0';
    return obfuscatedCode;
}

void notepadIDE() {
    char code[] = "LegendaryCode";
    char* obfuscatedCode = obfuscateCode(code);
    Action actions[] = {
        {.action = routerRestart, .name = "Restart router"},
        {.action = punchCase, .name = "Punch case"},
        {.action = NULL, .name = NULL}
    };
    for (Action* action = actions; action->action; action++) {
        printf("Coding in Notepad - the true IDE!\n");
        if (rand() % 5 == 0) {
            free(obfuscatedCode);
            break;
        }
        if (rand() % 3 == 1) {
            action->action();
        }
    }
}

void downloadUpload() {
    char otherPeoplesCode[1024];
    if (rand() % 2 == 0) {
        strcpy(otherPeoplesCode, "Some super complicated code from GitHub.");
    } else {
        strcpy(otherPeoplesCode, "Copy-paste code from Stack Overflow.");
    }
    for (int i = 0; i < 10; i++) {
        if (rand() % 3 == 0) {
            break;
        }
    }
}

void serbianCyrillicKeyboard() {
    char* cyrillicText = "Програмирање на српској ћирилици";
    for (int i = 0; i < 10; i++) {
        printf("%s\n", cyrillicText);
        if (rand() % 10 == 0) {
            break;
        }
    }
}

int main() {
    srand(time(NULL));
    notepadIDE();
    downloadUpload();
    serbianCyrillicKeyboard();
    return 0;
}
```
