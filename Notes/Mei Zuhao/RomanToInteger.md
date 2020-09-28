```c++
romanToInt(string s) {
    unordered_map<char, int> map = {{'I', 1},
                                    {'V', 5},
                                    {'X', 10},
                                    {'L', 50},
                                    {'C', 100},
                                    {'D', 500},
                                    {'M', 1000}};
    int Num = map[s[0]], NextNum, ans = 0; 
    // Num保存当前数字，NextNum保存下一个数字
    for (int i = 1; i < s.size(); ++i) {
        NextNum = map[s[i]];
        if (Num < NextNum) { // 当前数字小于下一位数字，减当前数字
            ans -= Num;
        }
        else {
            ans += Num;
        }
        Num = NextNum;
    }
    ans += Num; // 加上最后一位
return ans;
}

string intToRoman(int num) {
    int nums[] = {1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1};
    string str[] = {"M", "CM", "D", "CD", "C", "XC", "L", "XL", "X", "IX", "V", "IV", "I"};
    string ans;
    // 贪心法则：每次尽量使用最大的数来表示
    for (int i = 0; i < end(nums)-begin(nums); ++i) {
        while (num >= nums[i]) {
            num -= nums[i];
            ans += str[i];
        }
    }
    return ans;
}


```


