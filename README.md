# test
var str = "CMXCIX";
        var hash = { I: 1, V: 5, X: 10, L: 50, C: 100, D: 500, M: 1000 };

        var max = 0;

        for (var i = 1; i < str.length; i++) {
            if (hash[str.charAt(i)] >= hash[str.charAt(i - 1)]) {
                max -= hash[str.charAt(i - 1)];
            } else {
                max += hash[str.charAt(i - 1)];
            }

        }
        var result = max + hash[str.charAt(str.length - 1)];

        console.log(result);
