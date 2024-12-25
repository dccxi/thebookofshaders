## in
Кваліфікатор доступу аргументів. Позначає аргумент лише на читання. Застосовується по замовчуванню.

### Приклад
```glsl
// Кваліфікатор "in" можна не прописувати явно, бо він застосовується по замовчуванню
float updateValue(in float x) {
    // ці зміни для змінної "х" відбудуться лише усередині функції
    x = x + x; // x = (0.5 + 0.5) = 1.0

    return x;  // 1.0
}

void main() {
    float x = 0.5;
    float totalSum = updateValue(x); // totalSum == 1.0
    
    // x == 0.5, оскільки параметр був переданий лише на читання, то після виконання функції його значення залишається як і було
}
```

### Опис
**```in```** — кваліфікатор доступу аргументів, який дозволяє лише читати позначену змінну. Зміни всередині функції не вплинуть на значення переданої змінної поза її межами.

### Дивіться також
[out](/glossary/?lan=ua&search=out), [inout](/glossary/?lan=ua&search=inout)