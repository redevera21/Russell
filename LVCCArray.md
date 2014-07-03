
=======
public class LVCCArray {

    int max;
    int min;
    int[] numbers;
 
    public LVCCArray(int[] numbers) {
        this.numbers = numbers;
        this.determineMin();
        this.determineMax();
    }
 
    private void determineMin() {
        int i;
        this.min = this.numbers[0];
        for (i = 1; i < this.numbers.length; i++) {
            if (this.numbers[i] < this.min) {
                this.min = this.numbers[i];
            }
        }
    }
 
    private void determineMax() {
        int i;
        this.max = this.numbers[0];
        for (i = 1; i < this.numbers.length; i++) {
            if (this.numbers[i] > this.max) {
                this.max = this.numbers[i];
            }
        }
    }
 
    public int getMin() {
        return this.min;
    }
 
    public int getMax() {
        return this.max;
    }
}
