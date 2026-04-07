//Implemetning Stack using Queue

import java.util.*;

class MyStack {

    Queue<Integer> q;

    public MyStack() {
        q = new LinkedList<>();
    }

    public void push(int x) {

        q.add(x);

        int size = q.size();

        for(int i = 0; i < size - 1; i++){
            q.add(q.remove());
        }
    }

    public int pop() {
        return q.remove();
    }

    public int top() {
        return q.peek();
    }

    public boolean empty() {
        return q.isEmpty();
    }
}

<img width="1918" height="860" alt="image" src="https://github.com/user-attachments/assets/dfefc3d3-2852-45c5-af48-ba65fd512f89" />
