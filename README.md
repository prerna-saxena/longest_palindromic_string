# longest_palindromic_string



#include <iostream>
#include <bits/stdc++.h>

using namespace std;

int longestpalsubstring(String str) 
{
    int n=str.size();
    if(n<2)
    return n;
    int maxlength=1, start=0;
    int low, high;
    for(int i=0; i<n; i++)
    int low=i-1;
    int high=i+1;
    
    while(high<n && str[high]==str[i])
    high++;
    while(low>=0 && str[low]==str[i])
    low--;
    while(low>=0&& high<n &&str[low]==str[high])
    low--;
    high++;
    
    int length=high-low-1;
    if(maxlength<length){
        maxlength=length;
        start=low+1;
    }
}
cout<<str.substr(start, maxlength);
return maxlength;
}

    }
    
    
    
    return 0;
}
