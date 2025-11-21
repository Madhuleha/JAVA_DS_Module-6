public class InversionCount { 

    // Function to merge two halves and count inversions
    private static long merge(int[] arr, int left, int mid, int right) {
        int[] leftArr = new int[mid - left + 1];
        int[] rightArr = new int[right - mid];

        // Copy data to temporary arrays
        for (int i = 0; i < leftArr.length; i++)
            leftArr[i] = arr[left + i];

        for (int i = 0; i < rightArr.length; i++)
            rightArr[i] = arr[mid + 1 + i];

        int i = 0, j = 0, k = left;
        long inversions = 0;

        // Merge while counting inversions
        while (i < leftArr.length && j < rightArr.length) {
            if (leftArr[i] <= rightArr[j]) {
                arr[k++] = leftArr[i++];
            } else {
                arr[k++] = rightArr[j++];
                inversions += (leftArr.length - i); 
                // because leftArr[i...end] > rightArr[j]
            }
        }

        // Copy remaining elements
        while (i < leftArr.length) arr[k++] = leftArr[i++];
        while (j < rightArr.length) arr[k++] = rightArr[j++];

        return inversions;
    }

    // Recursive merge sort to count inversions
    private static long mergeSort(int[] arr, int left, int right) {
        long count = 0;

        if (left < right) {
            int mid = (left + right) / 2;

            count += mergeSort(arr, left, mid);
            count += mergeSort(arr, mid + 1, right);
            count += merge(arr, left, mid, right);
        }

        return count;
    }

    // Main function
    public static void main(String[] args) {
        int[] arr = {2, 4, 1, 3, 5};

        long inversions = mergeSort(arr, 0, arr.length - 1);

        System.out.println("Number of inversions: " + inversions);
    }
}
