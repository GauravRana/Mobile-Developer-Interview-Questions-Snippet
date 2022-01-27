# Mobile-Developer-Interview-Questions-Snippet

## String

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

