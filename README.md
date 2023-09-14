# priority_queue

class Solution {
public:
    int lastStoneWeight(vector<int>& stones) {
        priority_queue<int>pq;//maxheap return max element
        int n=stones.size();
        for(int i=0;i<n;i++){
            
            pq.push(stones[i]);
        }
        while(pq.size()>1){
            int x=pq.top();
            pq.pop();
            int y=pq.top();
            pq.pop();
            
            if(x>y)//x will bw greater always
                pq.push(x-y);
            
            
            }
        
        return pq.empty() ? 0 : pq.top();//if not empty return top of queue
    }
};
