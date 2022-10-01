# Price-per-Square-Foot-C-
Program that accepts as input the base price and the finished area in square feet of the three models.


#include <iostream>
#include <iomanip>
#include <string>
#include <cmath>

using namespace std;

int main() {
    // Write your main here
// Variables for colonial
  double bpColon, areaColon, priceColon;
//variables for split entry
  double bpSplit, areaSplit, priceSplit;
//variables for single floor
  double bpSingle,areaSingle, priceSingle;

//getting values for colonial house
  cout<<"Enter base price of Colonial: " <<endl;
  cin>>bpColon;
  cout<<"Enter area of Colonial: "<<endl;
  cin>>areaColon;
  priceColon = bpColon/areaColon;

//getting values for Split entry house
cout<<"Enter base price of Split-Entry: " <<endl;
cin>>bpSplit;
cout<<"Enter area of Split-Entry: "<<endl;
cin>>areaSplit;
priceSplit = bpSplit/areaSplit;

//getting values for single floor house
cout<<"Enter base price of Single floor: " <<endl;
cin>>bpSingle;
cout<<"Enter area of Single floor: "<<endl;
cin>>areaSingle;
priceSingle = bpSingle/areaSingle;

//these statments check to see which house has the least price per foot and gives proper out put
if (priceColon < priceSingle && priceColon < priceSplit){
  cout<< "The price per square foot of the colonial model is the least."<< endl;
} else if (priceSplit < priceColon && priceSplit < priceSingle){
  cout<<"The price per square foot of the split-entry model is the least.";
}else if(priceSingle < priceColon && priceSingle < priceSplit){
  cout<<"The price per square foot of the single-story model is the least.";
}else if (priceColon == priceSplit && priceColon < priceSingle){
  cout<<"The price per square foot of the colonial and split-entry models tie for the least.";
}else if (priceColon == priceSingle && priceColon < priceSplit){
  cout<<"The price per square foot of the colonial and single-story models tie for the least.";
}else if(priceSingle == priceSplit && priceSingle < priceColon){
   cout<<"The price per square foot of the single-story and split-entry models tie for the least.";
}else if(priceColon == priceSingle && priceColon == priceSplit){
  cout<<"The price per square foot all three models are the same.";
}
 

    return 0;
}
