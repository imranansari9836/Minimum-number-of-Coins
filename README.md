class Solution{
    static List<Integer> minPartition(int N)
    {
  
    ArrayList<Integer>set=new ArrayList<>();
    int wallet[]={ 1, 2, 5, 10, 20, 50, 100, 200, 500, 2000 };
    int j=wallet.length-1;
    while(j>=0)
    {
    if(wallet[j]>N)
    {
    j--;
    }
    else
    {
    set.add(wallet[j]);
    N-=wallet[j];
    }
    }
    return set;
    }
}
