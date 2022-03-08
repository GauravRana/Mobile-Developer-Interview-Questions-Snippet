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
for (int i = 0; i < len; i++){
    count[str.charAt(i)]++;
}
char ch[] = new char[str.length()];
for (int i = 0; i < len; i++) {
      ch[i] = str.charAt(i);
      int find = 0;
      for (int j = 0; j <= i; j++) {
          if (str.charAt(i) == ch[j]){
                  find++;
          }
      }
      if (find == 1){
          System.out.println("Number of Occurrence of "+ str.charAt(i)+ " is:" + count[str.charAt(i)]);
      }
 }
```


# Stack

### Simple stack

```typescript
// Online Java Compiler
// Use this editor to write, compile and run your Java code online

class Stack {
    int arr[];
    int top = 0;
    int capacity = 0;

    Stack(int size){
        arr = new int[size];
        top = -1;
        capacity = size;
    }
    public void push(int val){
        if(isFull()){
            System.out.println("Stack Full");
            System.exit(1);
        }
        arr[++top] = val;
    }
    
    public int pop(){
        if(isEmpty()){
            System.out.println("Stack Empty");
            System.exit(1);
        }
        return arr[top--];
    }
    
    public boolean isFull(){
        return top == capacity - 1;
    }
    
    public boolean isEmpty(){
        return top == -1;
    }
    
    public void printStack(){
        for (int i = 0; i <= top; i++){
            System.out.println(arr[i]+"\n");
        }
    }
    
    public static void main(String[] args) {
        Stack stack = new Stack(5);
        stack.push(1);
        stack.push(2);
        stack.push(3);
        stack.push(4);
        stack.push(5);
        stack.printStack();
        System.out.print("pop called \n");
        stack.pop();
        stack.printStack();
    }
}
}
```

# Queue

### Simple queue

```typescript
// Online Java Compiler
// Use this editor to write, compile and run your Java code online

class Queue {
    int arr[];
    int front = 0;
    int rear = 0;
    int SIZE = 0;

    Queue(int size){
        arr = new int[size];
        front = -1;
        rear = -1;
        SIZE = size;
    }
    public void enqueue(int element){
        if(isFull()){
            System.out.println("Queue Full");
            System.exit(1);
        }
        if(front == -1)
            front = 0;
        rear++;
        arr[rear] = element;
        System.out.println("Deleted -> " + element);
    }
    
    public int dequeue(){
        int element = 0;
        if(isEmpty()){
            System.out.println("Queue Empty");
            System.exit(1);
        }else{
            element = arr[front];
            if(front >= rear){
                front = -1;
                rear = -1;
            }else{
                front++;
            }
            System.out.println("Deleted -> " + element);
        }
        return element;
    }
    
    public boolean isFull(){
        if(front == 0 && rear == SIZE - 1){
            return true;
        }else{
            return false;
        }
    }
    
    public boolean isEmpty(){
        return front == -1;
    }
    
    public void printStack(){
        for (int i = 0; i <= rear; i++){
            System.out.println(arr[i]+"\n");
        }
    }
    
    public static void main(String[] args) {
        Queue queue = new Queue(5);
        queue.enqueue(1);
        queue.enqueue(2);
        queue.enqueue(3);
        queue.enqueue(4);
        queue.enqueue(5);
        queue.printStack();
        System.out.print("dequeue called \n");
        queue.dequeue();
        queue.printStack();
    }
}
```





