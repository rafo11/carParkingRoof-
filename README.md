Import java.util.Arrays;


public class Main {
    public static void main(String[] args) {
        int[] cars = {6, 2, 12, 7};
        int k = 3;
        System.out.println(carParkingRoof(cars,k));
    }

    public static int carParkingRoof(int[] cars, int k) {
        Arrays.sort(cars);
        int res = cars[cars.length - 1] - cars[0] + 1;
        for (int i = 0; i + k - 1 < cars.length; i++) {
            res = Math.min(res, cars[i + k - 1] - cars[i] +1);

        }
        return res;
    }
}
