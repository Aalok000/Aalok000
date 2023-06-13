- 👋 Hi, I’m @Aalok000
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

public class MajorityElement {
    public static int findMajorityElement(int[] nums) {
        int n = nums.length;
        Map<Integer, Integer> frequencyMap = new HashMap<>();

        for (int num : nums) {
            frequencyMap.put(num, frequencyMap.getOrDefault(num, 0) + 1);
            if (frequencyMap.get(num) > n / 2) {
                return num;
            }
        }

        return -1; // No majority element found
    }

    public static void main(String[] args) {
        int[] arr1 = {1, 2, 2, 2, 3};
        int majority1 = findMajorityElement(arr1);
        System.out.println("Majority element: " + majority1); // Output: 2

        int[] arr2 = {1, 2, 3, 4, 5};
        int majority2 = findMajorityElement(arr2);
        System.out.println("Majority element: " + majority2); // Output: -1
    }
}
