# Mobile-Developer-Interview-Questions-Snippet

# String

### Reverse the word (accd -> dcca)

```typescript
for(int i = 0; i < str.length(); i++){
      ch = str.charAt(i);
      nStr = ch + nStr;
}
```

### Reverse the sentence (i love pooh -> pooh love i)

```typescript

Pattern pattern = Pattern.compile("\\s");
String[] temp  = pattern.split(str);
for(int i = 0; i < str.length(); i++){
      if(i == temp.length - 1){
            result = temp[i]  + result;
      }else{
            result = " " + temp[i]  + result;
      }
}
```


### Repeating elements in integer array 
``` typescript
for (i = 0; i < size-1; i++){
      for (j = i + 1; j < size; j++){
          if (arr[i] == arr[j])
              System.out.print(arr[i] + " ");
      }
}
```
## Complexity O(n*n)

### Count the occurence of each character
```typscript
int count[] = new int[MAX_CHAR];
int len = str.length();
for (int i = 0; i < len; i++)
count[str.charAt(i)]++;
char ch[] = new char[str.length()];
      for (int i = 0; i < len; i++) {
            ch[i] = str.charAt(i);
            int find = 0;
            for (int j = 0; j <= i; j++) {
                if (str.charAt(i) == ch[j])
                    find++;
            }
            if (find == 1)
                System.out.println(
                    "Number of Occurrence of "
                    + str.charAt(i)
                    + " is:" + count[str.charAt(i)]);
       }
}
```




