// Java Recursion Program 1: Print numbers from 1 to N
public class Recursion1 {
    public static void printNumbers(int n) {
        if (n == 0) return;
        printNumbers(n - 1);
        System.out.print(n + " ");
    }

    public static void main(String[] args) {
        printNumbers(10);
    }
}

// Java Recursion Program 2: Print numbers from N to 1
public class Recursion2 {
    public static void printReverse(int n) {
        if (n == 0) return;
        System.out.print(n + " ");
        printReverse(n - 1);
    }

    public static void main(String[] args) {
        printReverse(10);
    }
}

// Java Recursion Program 3: Factorial of a number
public class Recursion3 {
    public static int factorial(int n) {
        if (n <= 1) return 1;
        return n * factorial(n - 1);
    }

    public static void main(String[] args) {
        System.out.println(factorial(5));
    }
}

// Java Recursion Program 4: Sum of first N numbers
public class Recursion4 {
    public static int sum(int n) {
        if (n == 0) return 0;
        return n + sum(n - 1);
    }

    public static void main(String[] args) {
        System.out.println(sum(5));
    }
}

// Java Recursion Program 5: Fibonacci series up to N terms
public class Recursion5 {
    public static int fib(int n) {
        if (n <= 1) return n;
        return fib(n - 1) + fib(n - 2);
    }

    public static void main(String[] args) {
        for (int i = 0; i < 10; i++)
            System.out.print(fib(i) + " ");
    }
}

// Java Recursion Program 6: Reverse a string
public class Recursion6 {
    public static String reverse(String str) {
        if (str.isEmpty()) return str;
        return reverse(str.substring(1)) + str.charAt(0);
    }

    public static void main(String[] args) {
        System.out.println(reverse("hello"));
    }
}

// Java Recursion Program 7: Check if a string is palindrome
public class Recursion7 {
    public static boolean isPalindrome(String str, int start, int end) {
        if (start >= end) return true;
        return str.charAt(start) == str.charAt(end) && isPalindrome(str, start + 1, end - 1);
    }

    public static void main(String[] args) {
        System.out.println(isPalindrome("madam", 0, 4));
    }
}

// Java Recursion Program 8: Power of a number (a^b)
public class Recursion8 {
    public static int power(int a, int b) {
        if (b == 0) return 1;
        return a * power(a, b - 1);
    }

    public static void main(String[] args) {
        System.out.println(power(2, 3));
    }
}

// Java Recursion Program 9: GCD of two numbers
public class Recursion9 {
    public static int gcd(int a, int b) {
        if (b == 0) return a;
        return gcd(b, a % b);
    }

    public static void main(String[] args) {
        System.out.println(gcd(48, 18));
    }
}

// Java Recursion Program 10: LCM using recursion
public class Recursion10 {
    public static int gcd(int a, int b) {
        if (b == 0) return a;
        return gcd(b, a % b);
    }

    public static int lcm(int a, int b) {
        return (a * b) / gcd(a, b);
    }

    public static void main(String[] args) {
        System.out.println(lcm(12, 15));
    }
}
// Java Recursion Program 11: Sum of digits of a number
public class Recursion11 {
    public static int sumOfDigits(int n) {
        if (n == 0) return 0;
        return n % 10 + sumOfDigits(n / 10);
    }

    public static void main(String[] args) {
        System.out.println(sumOfDigits(12345));
    }
}

// Java Recursion Program 12: Product of digits of a number
public class Recursion12 {
    public static int productOfDigits(int n) {
        if (n == 0) return 0;
        if (n < 10) return n;
        return (n % 10) * productOfDigits(n / 10);
    }

    public static void main(String[] args) {
        System.out.println(productOfDigits(1234));
    }
}

// Java Recursion Program 13: Count digits of a number
public class Recursion13 {
    public static int countDigits(int n) {
        if (n == 0) return 0;
        return 1 + countDigits(n / 10);
    }

    public static void main(String[] args) {
        System.out.println(countDigits(12345));
    }
}

// Java Recursion Program 14: Check if a number is prime
public class Recursion14 {
    public static boolean isPrime(int n, int i) {
        if (n <= 2) return (n == 2);
        if (n % i == 0) return false;
        if (i * i > n) return true;
        return isPrime(n, i + 1);
    }

    public static void main(String[] args) {
        System.out.println(isPrime(29, 2));
    }
}

// Java Recursion Program 15: Check if a number is Armstrong
public class Recursion15 {
    public static int power(int base, int exp) {
        if (exp == 0) return 1;
        return base * power(base, exp - 1);
    }

    public static int armstrongSum(int num, int digits) {
        if (num == 0) return 0;
        return power(num % 10, digits) + armstrongSum(num / 10, digits);
    }

    public static void main(String[] args) {
        int num = 153;
        int digits = String.valueOf(num).length();
        System.out.println(armstrongSum(num, digits) == num);
    }
}

// Java Recursion Program 16: Convert decimal to binary
public class Recursion16 {
    public static void decimalToBinary(int n) {
        if (n == 0) return;
        decimalToBinary(n / 2);
        System.out.print(n % 2);
    }

    public static void main(String[] args) {
        decimalToBinary(10);
    }
}

// Java Recursion Program 17: Convert binary to decimal
public class Recursion17 {
    public static int binaryToDecimal(int binary, int power) {
        if (binary == 0) return 0;
        return (binary % 10) * (int)Math.pow(2, power) + binaryToDecimal(binary / 10, power + 1);
    }

    public static void main(String[] args) {
        System.out.println(binaryToDecimal(1010, 0));
    }
}

// Java Recursion Program 18: Convert number to words (basic)
public class Recursion18 {
    static String[] words = {"zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine"};

    public static void numberToWords(int n) {
        if (n == 0) return;
        numberToWords(n / 10);
        System.out.print(words[n % 10] + " ");
    }

    public static void main(String[] args) {
        numberToWords(123);
    }
}

// Java Recursion Program 19: Print all subsets of a string
public class Recursion19 {
    public static void subsets(String str, String ans, int index) {
        if (index == str.length()) {
            System.out.println(ans);
            return;
        }
        subsets(str, ans + str.charAt(index), index + 1);
        subsets(str, ans, index + 1);
    }

    public static void main(String[] args) {
        subsets("abc", "", 0);
    }
}

// Java Recursion Program 20: Find all permutations of a string
public class Recursion20 {
    public static void permute(String str, String ans) {
        if (str.length() == 0) {
            System.out.println(ans);
            return;
        }
        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);
            String ros = str.substring(0, i) + str.substring(i + 1);
            permute(ros, ans + ch);
        }
    }

    public static void main(String[] args) {
        permute("abc", "");
    }
}
// Java Recursion Program 21: Tower of Hanoi
public class Recursion21 {
    public static void towerOfHanoi(int n, char from, char to, char aux) {
        if (n == 1) {
            System.out.println("Move disk 1 from " + from + " to " + to);
            return;
        }
        towerOfHanoi(n - 1, from, aux, to);
        System.out.println("Move disk " + n + " from " + from + " to " + to);
        towerOfHanoi(n - 1, aux, to, from);
    }

    public static void main(String[] args) {
        towerOfHanoi(3, 'A', 'C', 'B');
    }
}

// Java Recursion Program 22: Count paths in a maze (N x N)
public class Recursion22 {
    public static int countPaths(int i, int j, int n, int m) {
        if (i == n - 1 && j == m - 1) return 1;
        if (i >= n || j >= m) return 0;
        return countPaths(i + 1, j, n, m) + countPaths(i, j + 1, n, m);
    }

    public static void main(String[] args) {
        System.out.println(countPaths(0, 0, 3, 3));
    }
}

// Java Recursion Program 23: Balanced parentheses
public class Recursion23 {
    public static void generateParentheses(int open, int close, String str) {
        if (open == 0 && close == 0) {
            System.out.println(str);
            return;
        }
        if (open > 0) generateParentheses(open - 1, close, str + "(");
        if (close > open) generateParentheses(open, close - 1, str + ")");
    }

    public static void main(String[] args) {
        generateParentheses(3, 3, "");
    }
}

// Java Recursion Program 24: Check if array is sorted
public class Recursion24 {
    public static boolean isSorted(int[] arr, int index) {
        if (index == arr.length - 1) return true;
        return arr[index] <= arr[index + 1] && isSorted(arr, index + 1);
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        System.out.println(isSorted(arr, 0));
    }
}

// Java Recursion Program 25: Search element in array
public class Recursion25 {
    public static boolean search(int[] arr, int index, int key) {
        if (index == arr.length) return false;
        if (arr[index] == key) return true;
        return search(arr, index + 1, key);
    }

    public static void main(String[] args) {
        int[] arr = {5, 3, 8, 2, 4};
        System.out.println(search(arr, 0, 8));
    }
}

// Java Recursion Program 26: Find maximum element in array
public class Recursion26 {
    public static int findMax(int[] arr, int index) {
        if (index == arr.length - 1) return arr[index];
        return Math.max(arr[index], findMax(arr, index + 1));
    }

    public static void main(String[] args) {
        int[] arr = {5, 3, 9, 2, 4};
        System.out.println(findMax(arr, 0));
    }
}

// Java Recursion Program 27: Reverse array
public class Recursion27 {
    public static void reverseArray(int[] arr, int start, int end) {
        if (start >= end) return;
        int temp = arr[start];
        arr[start] = arr[end];
        arr[end] = temp;
        reverseArray(arr, start + 1, end - 1);
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        reverseArray(arr, 0, arr.length - 1);
        for (int i : arr) System.out.print(i + " ");
    }
}

// Java Recursion Program 28: Print all subsequences of a string
public class Recursion28 {
    public static void subsequences(String str, String ans) {
        if (str.isEmpty()) {
            System.out.println(ans);
            return;
        }
        char ch = str.charAt(0);
        subsequences(str.substring(1), ans + ch);
        subsequences(str.substring(1), ans);
    }

    public static void main(String[] args) {
        subsequences("abc", "");
    }
}

// Java Recursion Program 29: Generate all binary strings of length N
public class Recursion29 {
    public static void generateBinary(int n, String str) {
        if (n == 0) {
            System.out.println(str);
            return;
        }
        generateBinary(n - 1, str + "0");
        generateBinary(n - 1, str + "1");
    }

    public static void main(String[] args) {
        generateBinary(3, "");
    }
}

// Java Recursion Program 30: Find Nth Tribonacci number
public class Recursion30 {
    public static int tribonacci(int n) {
        if (n == 0) return 0;
        if (n == 1 || n == 2) return 1;
        return tribonacci(n - 1) + tribonacci(n - 2) + tribonacci(n - 3);
    }

    public static void main(String[] args) {
        System.out.println(tribonacci(6));
    }
}
// Java Recursion Program 31: Solve N-Queens Problem
public class Recursion31 {
    public static boolean isSafe(char[][] board, int row, int col) {
        for (int i = 0; i < row; i++)
            if (board[i][col] == 'Q') return false;
        for (int i = row - 1, j = col - 1; i >= 0 && j >= 0; i--, j--)
            if (board[i][j] == 'Q') return false;
        for (int i = row - 1, j = col + 1; i >= 0 && j < board.length; i--, j++)
            if (board[i][j] == 'Q') return false;
        return true;
    }

    public static void solveNQueens(char[][] board, int row) {
        if (row == board.length) {
            for (char[] arr : board) {
                for (char c : arr) System.out.print(c + " ");
                System.out.println();
            }
            System.out.println();
            return;
        }
        for (int j = 0; j < board.length; j++) {
            if (isSafe(board, row, j)) {
                board[row][j] = 'Q';
                solveNQueens(board, row + 1);
                board[row][j] = '.';
            }
        }
    }

    public static void main(String[] args) {
        int n = 4;
        char[][] board = new char[n][n];
        for (int i = 0; i < n; i++)
            for (int j = 0; j < n; j++)
                board[i][j] = '.';
        solveNQueens(board, 0);
    }
}

// Java Recursion Program 32: Print all palindrome partitions
public class Recursion32 {
    public static boolean isPalindrome(String str) {
        int i = 0, j = str.length() - 1;
        while (i < j) {
            if (str.charAt(i++) != str.charAt(j--)) return false;
        }
        return true;
    }

    public static void partition(String str, String result) {
        if (str.isEmpty()) {
            System.out.println(result.trim());
            return;
        }
        for (int i = 1; i <= str.length(); i++) {
            String prefix = str.substring(0, i);
            if (isPalindrome(prefix)) {
                partition(str.substring(i), result + prefix + " ");
            }
        }
    }

    public static void main(String[] args) {
        partition("nitin", "");
    }
}

// Java Recursion Program 33: Count palindrome partitions
public class Recursion33 {
    public static boolean isPalindrome(String str) {
        int i = 0, j = str.length() - 1;
        while (i < j) {
            if (str.charAt(i++) != str.charAt(j--)) return false;
        }
        return true;
    }

    public static int countPartitions(String str) {
        if (str.isEmpty()) return 1;
        int count = 0;
        for (int i = 1; i <= str.length(); i++) {
            String prefix = str.substring(0, i);
            if (isPalindrome(prefix)) {
                count += countPartitions(str.substring(i));
            }
        }
        return count;
    }

    public static void main(String[] args) {
        System.out.println(countPartitions("aab"));
    }
}

// Java Recursion Program 34: Sum of elements in array
public class Recursion34 {
    public static int arraySum(int[] arr, int index) {
        if (index == arr.length) return 0;
        return arr[index] + arraySum(arr, index + 1);
    }

    public static void main(String[] args) {
        int[] arr = {2, 4, 6, 8};
        System.out.println(arraySum(arr, 0));
    }
}

// Java Recursion Program 35: Find minimum element in array
public class Recursion35 {
    public static int findMin(int[] arr, int index) {
        if (index == arr.length - 1) return arr[index];
        return Math.min(arr[index], findMin(arr, index + 1));
    }

    public static void main(String[] args) {
        int[] arr = {10, 3, 5, 2, 8};
        System.out.println(findMin(arr, 0));
    }
}

// Java Recursion Program 36: Count even numbers in array
public class Recursion36 {
    public static int countEven(int[] arr, int index) {
        if (index == arr.length) return 0;
        return (arr[index] % 2 == 0 ? 1 : 0) + countEven(arr, index + 1);
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5, 6};
        System.out.println(countEven(arr, 0));
    }
}

// Java Recursion Program 37: Count odd numbers in array
public class Recursion37 {
    public static int countOdd(int[] arr, int index) {
        if (index == arr.length) return 0;
        return (arr[index] % 2 != 0 ? 1 : 0) + countOdd(arr, index + 1);
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5, 6};
        System.out.println(countOdd(arr, 0));
    }
}

// Java Recursion Program 38: Check if string is made up of only digits
public class Recursion38 {
    public static boolean isDigitString(String str, int index) {
        if (index == str.length()) return true;
        if (!Character.isDigit(str.charAt(index))) return false;
        return isDigitString(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(isDigitString("123456", 0));
        System.out.println(isDigitString("123a56", 0));
    }
}

// Java Recursion Program 39: Remove vowels from a string
public class Recursion39 {
    public static String removeVowels(String str, int index) {
        if (index == str.length()) return "";
        char ch = str.charAt(index);
        String rest = removeVowels(str, index + 1);
        if ("aeiouAEIOU".indexOf(ch) != -1) return rest;
        return ch + rest;
    }

    public static void main(String[] args) {
        System.out.println(removeVowels("Hello World", 0));
    }
}

// Java Recursion Program 40: Replace all spaces with underscores
public class Recursion40 {
    public static String replaceSpaces(String str, int index) {
        if (index == str.length()) return "";
        char ch = str.charAt(index);
        String rest = replaceSpaces(str, index + 1);
        if (ch == ' ') return "_" + rest;
        return ch + rest;
    }

    public static void main(String[] args) {
        System.out.println(replaceSpaces("this is a test", 0));
    }
}
// Java Recursion Program 41: Print digits in reverse order
public class Recursion41 {
    public static void printReverseDigits(int n) {
        if (n == 0) return;
        System.out.print(n % 10 + " ");
        printReverseDigits(n / 10);
    }

    public static void main(String[] args) {
        printReverseDigits(12345);
    }
}

// Java Recursion Program 42: Replace character in a string
public class Recursion42 {
    public static String replaceChar(String str, char oldChar, char newChar, int index) {
        if (index == str.length()) return "";
        char ch = str.charAt(index);
        if (ch == oldChar) ch = newChar;
        return ch + replaceChar(str, oldChar, newChar, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(replaceChar("banana", 'a', 'o', 0));
    }
}

// Java Recursion Program 43: Count character frequency
public class Recursion43 {
    public static int countChar(String str, char target, int index) {
        if (index == str.length()) return 0;
        return (str.charAt(index) == target ? 1 : 0) + countChar(str, target, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(countChar("mississippi", 's', 0));
    }
}

// Java Recursion Program 44: Capitalize each character
public class Recursion44 {
    public static String capitalize(String str, int index) {
        if (index == str.length()) return "";
        char ch = Character.toUpperCase(str.charAt(index));
        return ch + capitalize(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(capitalize("hello", 0));
    }
}

// Java Recursion Program 45: Remove consecutive duplicates
public class Recursion45 {
    public static String removeConsecutiveDuplicates(String str, int index) {
        if (index == str.length() - 1) return str.charAt(index) + "";
        String rest = removeConsecutiveDuplicates(str, index + 1);
        if (str.charAt(index) == rest.charAt(0)) return rest;
        return str.charAt(index) + rest;
    }

    public static void main(String[] args) {
        System.out.println(removeConsecutiveDuplicates("aabbccdde", 0));
    }
}

// Java Recursion Program 46: Replace Pi with 3.14 in string
public class Recursion46 {
    public static String replacePi(String str) {
        if (str.length() <= 1) return str;
        if (str.startsWith("pi"))
            return "3.14" + replacePi(str.substring(2));
        return str.charAt(0) + replacePi(str.substring(1));
    }

    public static void main(String[] args) {
        System.out.println(replacePi("pippppiiiipi"));
    }
}

// Java Recursion Program 47: Binary search using recursion
public class Recursion47 {
    public static int binarySearch(int[] arr, int left, int right, int target) {
        if (left > right) return -1;
        int mid = (left + right) / 2;
        if (arr[mid] == target) return mid;
        if (target < arr[mid]) return binarySearch(arr, left, mid - 1, target);
        return binarySearch(arr, mid + 1, right, target);
    }

    public static void main(String[] args) {
        int[] arr = {1, 3, 5, 7, 9, 11};
        System.out.println(binarySearch(arr, 0, arr.length - 1, 5));
    }
}

// Java Recursion Program 48: Print all indices of a key in array
public class Recursion48 {
    public static void findIndices(int[] arr, int index, int key) {
        if (index == arr.length) return;
        if (arr[index] == key) System.out.print(index + " ");
        findIndices(arr, index + 1, key);
    }

    public static void main(String[] args) {
        int[] arr = {5, 3, 7, 3, 9, 3};
        findIndices(arr, 0, 3);
    }
}

// Java Recursion Program 49: Count number of ways to climb stairs (1 or 2 steps)
public class Recursion49 {
    public static int countWays(int n) {
        if (n == 0) return 1;
        if (n < 0) return 0;
        return countWays(n - 1) + countWays(n - 2);
    }

    public static void main(String[] args) {
        System.out.println(countWays(5));
    }
}

// Java Recursion Program 50: Count ways to make change for amount
public class Recursion50 {
    public static int countChange(int[] coins, int n, int amount) {
        if (amount == 0) return 1;
        if (amount < 0 || n <= 0) return 0;
        return countChange(coins, n, amount - coins[n - 1]) + countChange(coins, n - 1, amount);
    }

    public static void main(String[] args) {
        int[] coins = {1, 2, 3};
        System.out.println(countChange(coins, coins.length, 4));
    }
}
// Java Recursion Program 51: Print all permutations of array elements
public class Recursion51 {
    public static void permute(int[] arr, int start) {
        if (start == arr.length) {
            for (int num : arr) System.out.print(num + " ");
            System.out.println();
            return;
        }
        for (int i = start; i < arr.length; i++) {
            int temp = arr[start];
            arr[start] = arr[i];
            arr[i] = temp;
            permute(arr, start + 1);
            temp = arr[start];
            arr[start] = arr[i];
            arr[i] = temp;
        }
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3};
        permute(arr, 0);
    }
}

// Java Recursion Program 52: Find power using fast exponentiation
public class Recursion52 {
    public static int fastPower(int a, int b) {
        if (b == 0) return 1;
        int halfPower = fastPower(a, b / 2);
        int result = halfPower * halfPower;
        return (b % 2 == 0) ? result : a * result;
    }

    public static void main(String[] args) {
        System.out.println(fastPower(2, 10));
    }
}

// Java Recursion Program 53: Sum of geometric progression
public class Recursion53 {
    public static double geometricSum(int n) {
        if (n == 0) return 1;
        return 1.0 / Math.pow(2, n) + geometricSum(n - 1);
    }

    public static void main(String[] args) {
        System.out.printf("%.5f", geometricSum(5));
    }
}

// Java Recursion Program 54: Convert integer to string
public class Recursion54 {
    static String[] digits = {"zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine"};

    public static void convertToString(int n) {
        if (n == 0) return;
        convertToString(n / 10);
        System.out.print(digits[n % 10] + " ");
    }

    public static void main(String[] args) {
        convertToString(123);
    }
}

// Java Recursion Program 55: Check if string contains only alphabetic characters
public class Recursion55 {
    public static boolean isAlpha(String str, int index) {
        if (index == str.length()) return true;
        if (!Character.isLetter(str.charAt(index))) return false;
        return isAlpha(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(isAlpha("HelloWorld", 0));
        System.out.println(isAlpha("Hello123", 0));
    }
}

// Java Recursion Program 56: Insert character between every pair of characters in a string
public class Recursion56 {
    public static String insertStars(String str) {
        if (str.length() <= 1) return str;
        return str.charAt(0) + "*" + insertStars(str.substring(1));
    }

    public static void main(String[] args) {
        System.out.println(insertStars("hello"));
    }
}

// Java Recursion Program 57: Sum of array elements in given range
public class Recursion57 {
    public static int sumInRange(int[] arr, int start, int end) {
        if (start > end) return 0;
        return arr[start] + sumInRange(arr, start + 1, end);
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        System.out.println(sumInRange(arr, 1, 3));
    }
}

// Java Recursion Program 58: Count lowercase letters in string
public class Recursion58 {
    public static int countLowerCase(String str, int index) {
        if (index == str.length()) return 0;
        char ch = str.charAt(index);
        return (Character.isLowerCase(ch) ? 1 : 0) + countLowerCase(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(countLowerCase("HelloWorld", 0));
    }
}

// Java Recursion Program 59: Replace space with '%20'
public class Recursion59 {
    public static String replaceSpaces(String str, int index) {
        if (index == str.length()) return "";
        char ch = str.charAt(index);
        return (ch == ' ' ? "%20" : ch + "") + replaceSpaces(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(replaceSpaces("Mr John Smith", 0));
    }
}

// Java Recursion Program 60: Print binary representation of a number
public class Recursion60 {
    public static void printBinary(int n) {
        if (n == 0) return;
        printBinary(n / 2);
        System.out.print(n % 2);
    }

    public static void main(String[] args) {
        printBinary(19);
    }
}
// Java Recursion Program 61: Sum of digits of a number
public class Recursion61 {
    public static int sumDigits(int n) {
        if (n == 0) return 0;
        return n % 10 + sumDigits(n / 10);
    }

    public static void main(String[] args) {
        System.out.println(sumDigits(12345));
    }
}

// Java Recursion Program 62: Check if a number is power of 2
public class Recursion62 {
    public static boolean isPowerOfTwo(int n) {
        if (n == 1) return true;
        if (n == 0 || n % 2 != 0) return false;
        return isPowerOfTwo(n / 2);
    }

    public static void main(String[] args) {
        System.out.println(isPowerOfTwo(16));
        System.out.println(isPowerOfTwo(18));
    }
}

// Java Recursion Program 63: Reverse number
public class Recursion63 {
    public static int reverseNumber(int n, int rev) {
        if (n == 0) return rev;
        return reverseNumber(n / 10, rev * 10 + n % 10);
    }

    public static void main(String[] args) {
        System.out.println(reverseNumber(1234, 0));
    }
}

// Java Recursion Program 64: Find length of string
public class Recursion64 {
    public static int stringLength(String str) {
        if (str.equals("")) return 0;
        return 1 + stringLength(str.substring(1));
    }

    public static void main(String[] args) {
        System.out.println(stringLength("hello world"));
    }
}

// Java Recursion Program 65: Convert all uppercase to lowercase
public class Recursion65 {
    public static String toLower(String str, int index) {
        if (index == str.length()) return "";
        char ch = Character.toLowerCase(str.charAt(index));
        return ch + toLower(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(toLower("HeLLo WoRLD", 0));
    }
}

// Java Recursion Program 66: Find GCD of two numbers
public class Recursion66 {
    public static int gcd(int a, int b) {
        if (b == 0) return a;
        return gcd(b, a % b);
    }

    public static void main(String[] args) {
        System.out.println(gcd(48, 18));
    }
}

// Java Recursion Program 67: Product of digits
public class Recursion67 {
    public static int productDigits(int n) {
        if (n == 0) return 0;
        if (n < 10) return n;
        return (n % 10) * productDigits(n / 10);
    }

    public static void main(String[] args) {
        System.out.println(productDigits(123));
    }
}

// Java Recursion Program 68: Count even digits in number
public class Recursion68 {
    public static int countEvenDigits(int n) {
        if (n == 0) return 0;
        return ((n % 10) % 2 == 0 ? 1 : 0) + countEvenDigits(n / 10);
    }

    public static void main(String[] args) {
        System.out.println(countEvenDigits(24863));
    }
}

// Java Recursion Program 69: Count odd digits in number
public class Recursion69 {
    public static int countOddDigits(int n) {
        if (n == 0) return 0;
        return ((n % 10) % 2 != 0 ? 1 : 0) + countOddDigits(n / 10);
    }

    public static void main(String[] args) {
        System.out.println(countOddDigits(24863));
    }
}

// Java Recursion Program 70: Convert decimal to octal
public class Recursion70 {
    public static void toOctal(int n) {
        if (n == 0) return;
        toOctal(n / 8);
        System.out.print(n % 8);
    }

    public static void main(String[] args) {
        toOctal(83);  // Expected output: 123
    }
}
// Java Recursion Program 71: Convert decimal to hexadecimal
public class Recursion71 {
    public static void toHex(int n) {
        if (n == 0) return;
        toHex(n / 16);
        int rem = n % 16;
        if (rem < 10) System.out.print(rem);
        else System.out.print((char) ('A' + rem - 10));
    }

    public static void main(String[] args) {
        toHex(254); // Expected output: FE
    }
}

// Java Recursion Program 72: Convert binary to decimal
public class Recursion72 {
    public static int binaryToDecimal(String binary, int index) {
        if (index == binary.length()) return 0;
        int bit = binary.charAt(index) - '0';
        return bit * (int)Math.pow(2, binary.length() - 1 - index) + binaryToDecimal(binary, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(binaryToDecimal("1101", 0)); // 13
    }
}

// Java Recursion Program 73: Sum of squares of first N natural numbers
public class Recursion73 {
    public static int sumSquares(int n) {
        if (n == 1) return 1;
        return n * n + sumSquares(n - 1);
    }

    public static void main(String[] args) {
        System.out.println(sumSquares(5));
    }
}

// Java Recursion Program 74: Check if number is palindrome
public class Recursion74 {
    public static int reverse(int n, int rev) {
        if (n == 0) return rev;
        return reverse(n / 10, rev * 10 + n % 10);
    }

    public static boolean isPalindrome(int n) {
        return n == reverse(n, 0);
    }

    public static void main(String[] args) {
        System.out.println(isPalindrome(121));
        System.out.println(isPalindrome(123));
    }
}

// Java Recursion Program 75: Count digits of a number
public class Recursion75 {
    public static int countDigits(int n) {
        if (n == 0) return 0;
        return 1 + countDigits(n / 10);
    }

    public static void main(String[] args) {
        System.out.println(countDigits(12345));
    }
}

// Java Recursion Program 76: Count uppercase letters in string
public class Recursion76 {
    public static int countUpper(String str, int index) {
        if (index == str.length()) return 0;
        return (Character.isUpperCase(str.charAt(index)) ? 1 : 0) + countUpper(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(countUpper("HeLLo World", 0));
    }
}

// Java Recursion Program 77: Check if array is palindrome
public class Recursion77 {
    public static boolean isPalindrome(int[] arr, int start, int end) {
        if (start >= end) return true;
        if (arr[start] != arr[end]) return false;
        return isPalindrome(arr, start + 1, end - 1);
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 2, 1};
        System.out.println(isPalindrome(arr, 0, arr.length - 1));
    }
}

// Java Recursion Program 78: Remove all spaces from a string
public class Recursion78 {
    public static String removeSpaces(String str, int index) {
        if (index == str.length()) return "";
        char ch = str.charAt(index);
        return (ch == ' ' ? "" : ch + "") + removeSpaces(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(removeSpaces(" Java is fun ", 0));
    }
}

// Java Recursion Program 79: Replace each digit with its word representation
public class Recursion79 {
    static String[] digits = {"zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine"};

    public static void printWords(int n) {
        if (n == 0) return;
        printWords(n / 10);
        System.out.print(digits[n % 10] + " ");
    }

    public static void main(String[] args) {
        printWords(204);
    }
}

// Java Recursion Program 80: Convert decimal to binary
public class Recursion80 {
    public static void toBinary(int n) {
        if (n == 0) return;
        toBinary(n / 2);
        System.out.print(n % 2);
    }

    public static void main(String[] args) {
        toBinary(10); // Output: 1010
    }
}
// Java Recursion Program 81: Print all subsets of a string
public class Recursion81 {
    public static void printSubsets(String str, String current, int index) {
        if (index == str.length()) {
            System.out.println(current);
            return;
        }
        printSubsets(str, current + str.charAt(index), index + 1);
        printSubsets(str, current, index + 1);
    }

    public static void main(String[] args) {
        printSubsets("abc", "", 0);
    }
}

// Java Recursion Program 82: Count subsets of a string
public class Recursion82 {
    public static int countSubsets(String str, int index) {
        if (index == str.length()) return 1;
        return countSubsets(str, index + 1) + countSubsets(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(countSubsets("abc", 0));
    }
}

// Java Recursion Program 83: Print all binary strings of length N
public class Recursion83 {
    public static void printBinary(int n, String output) {
        if (n == 0) {
            System.out.println(output);
            return;
        }
        printBinary(n - 1, output + "0");
        printBinary(n - 1, output + "1");
    }

    public static void main(String[] args) {
        printBinary(3, "");
    }
}

// Java Recursion Program 84: Count number of binary strings of length N
public class Recursion84 {
    public static int countBinary(int n) {
        if (n == 0) return 1;
        return 2 * countBinary(n - 1);
    }

    public static void main(String[] args) {
        System.out.println(countBinary(3));
    }
}

// Java Recursion Program 85: Convert a number to base k
public class Recursion85 {
    public static void convertToBase(int n, int k) {
        if (n == 0) return;
        convertToBase(n / k, k);
        System.out.print(n % k);
    }

    public static void main(String[] args) {
        convertToBase(100, 3); // Output in base 3
    }
}

// Java Recursion Program 86: Find last index of a character in a string
public class Recursion86 {
    public static int lastIndex(String str, char ch, int index) {
        if (index < 0) return -1;
        if (str.charAt(index) == ch) return index;
        return lastIndex(str, ch, index - 1);
    }

    public static void main(String[] args) {
        System.out.println(lastIndex("recursion", 'r', 8));
    }
}

// Java Recursion Program 87: Count non-space characters in a string
public class Recursion87 {
    public static int countNonSpaces(String str, int index) {
        if (index == str.length()) return 0;
        return (str.charAt(index) != ' ' ? 1 : 0) + countNonSpaces(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(countNonSpaces("Hello World", 0));
    }
}

// Java Recursion Program 88: Replace digits in a string with '*'
public class Recursion88 {
    public static String replaceDigits(String str, int index) {
        if (index == str.length()) return "";
        char ch = str.charAt(index);
        return (Character.isDigit(ch) ? "*" : ch + "") + replaceDigits(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(replaceDigits("a1b2c3", 0));
    }
}

// Java Recursion Program 89: Reverse a string using recursion
public class Recursion89 {
    public static String reverse(String str) {
        if (str.isEmpty()) return str;
        return reverse(str.substring(1)) + str.charAt(0);
    }

    public static void main(String[] args) {
        System.out.println(reverse("recursion"));
    }
}

// Java Recursion Program 90: Find max digit in a number
public class Recursion90 {
    public static int maxDigit(int n) {
        if (n < 10) return n;
        return Math.max(n % 10, maxDigit(n / 10));
    }

    public static void main(String[] args) {
        System.out.println(maxDigit(394276));
    }
}
// Java Recursion Program 91: Check if string is palindrome
public class Recursion91 {
    public static boolean isPalindrome(String str, int left, int right) {
        if (left >= right) return true;
        if (str.charAt(left) != str.charAt(right)) return false;
        return isPalindrome(str, left + 1, right - 1);
    }

    public static void main(String[] args) {
        System.out.println(isPalindrome("madam", 0, 4));
        System.out.println(isPalindrome("hello", 0, 4));
    }
}

// Java Recursion Program 92: Find sum of even numbers from 1 to N
public class Recursion92 {
    public static int sumEven(int n) {
        if (n <= 0) return 0;
        return (n % 2 == 0 ? n : 0) + sumEven(n - 1);
    }

    public static void main(String[] args) {
        System.out.println(sumEven(10));
    }
}

// Java Recursion Program 93: Find sum of odd numbers from 1 to N
public class Recursion93 {
    public static int sumOdd(int n) {
        if (n <= 0) return 0;
        return (n % 2 != 0 ? n : 0) + sumOdd(n - 1);
    }

    public static void main(String[] args) {
        System.out.println(sumOdd(10));
    }
}

// Java Recursion Program 94: Replace vowels in string with '#'
public class Recursion94 {
    public static String replaceVowels(String str, int index) {
        if (index == str.length()) return "";
        char ch = str.charAt(index);
        if ("aeiouAEIOU".indexOf(ch) != -1) ch = '#';
        return ch + replaceVowels(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(replaceVowels("Recursion is powerful", 0));
    }
}

// Java Recursion Program 95: Find sum of elements in a matrix
public class Recursion95 {
    public static int matrixSum(int[][] matrix, int i, int j) {
        if (i == matrix.length) return 0;
        if (j == matrix[i].length) return matrixSum(matrix, i + 1, 0);
        return matrix[i][j] + matrixSum(matrix, i, j + 1);
    }

    public static void main(String[] args) {
        int[][] mat = {{1, 2}, {3, 4}, {5, 6}};
        System.out.println(matrixSum(mat, 0, 0));
    }
}

// Java Recursion Program 96: Count capital letters in string
public class Recursion96 {
    public static int countCapital(String str, int index) {
        if (index == str.length()) return 0;
        return (Character.isUpperCase(str.charAt(index)) ? 1 : 0) + countCapital(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(countCapital("Hello World", 0));
    }
}

// Java Recursion Program 97: Replace all capital letters with lowercase
public class Recursion97 {
    public static String toLowerCase(String str, int index) {
        if (index == str.length()) return "";
        char ch = Character.toLowerCase(str.charAt(index));
        return ch + toLowerCase(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(toLowerCase("ReCuRsIoN", 0));
    }
}

// Java Recursion Program 98: Count number of 'a' in string
public class Recursion98 {
    public static int countA(String str, int index) {
        if (index == str.length()) return 0;
        return (str.charAt(index) == 'a' ? 1 : 0) + countA(str, index + 1);
    }

    public static void main(String[] args) {
        System.out.println(countA("banana", 0));
    }
}

// Java Recursion Program 99: Print first N even numbers
public class Recursion99 {
    public static void printEven(int n) {
        if (n == 0) return;
        printEven(n - 1);
        System.out.print((n * 2) + " ");
    }

    public static void main(String[] args) {
        printEven(5);
    }
}

// Java Recursion Program 100: Print first N odd numbers
public class Recursion100 {
    public static void printOdd(int n) {
        if (n == 0) return;
        printOdd(n - 1);
        System.out.print((n * 2 - 1) + " ");
    }

    public static void main(String[] args) {
        printOdd(5);
    }
}
