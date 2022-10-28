# index-Equilibrium
index equilibrium


package TimeComplexity;

public class equikibrium {
    public static int equilibrium(int arr[]){
        if(arr.length==0){ 
            return -1;
        }
        if(arr.length==1){
            return 0;
        }
        int eqindex=1;
        int suml=arr[0];
        int sumr=0;
        for(int i=eqindex+1;i<arr.length;i++){
            sumr=sumr+arr[i];
        }

        while(eqindex<arr.length-1){
            if(sumr==suml){
                return eqindex;
            }
            else{
                suml=suml+arr[eqindex];
                sumr=sumr-arr[eqindex+1];
                eqindex++;
            }
        }
        if(sumr==suml){
            return eqindex;
        }
        return -1;
    }
    public static void main(String[] args) {
        int arr[]= {0,2};//{1,4,9,3,2}; //{1,-1,4};
        System.out.println(equilibrium(arr));
    }
}
