# finding-maximum-and-minimum-in-an-array




#include <iostream>
#include <vector>
#include <climits>

using namespace std;

pair<int, int> findMinMax(const vector<int>& nums) {
    int n = nums.size();
    int minVal = INT_MAX, maxVal = INT_MIN;
    for (int i = 0; i < n; i++) {
        minVal = min(minVal, nums[i]);
        maxVal = max(maxVal, nums[i]);
    }
    return {minVal, maxVal};
}

int main() {
    vector<int> nums = {5, 1, 8, 3, 9, 4, 6};
    auto [minVal, maxVal] = findMinMax(nums);
    cout << "Minimum value: " << minVal << endl;
    cout << "Maximum value: " << maxVal << endl;
    return 0;
}
