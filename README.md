# CodeForces-URI-UVA-Online-Judge-Accepted-Soultions
#include <bits/stdc++.h>
using namespace std;
int main()
{
	int n;
	cin>>n;
	while (n--)
	{
		vector <int> a;
		queue <pair<int, int> > b;
		int x,y;
		cin>>x>>y;
		for(int i=0;i<x;i++)
		{
			int z;
			cin>>z;
			b.push({i,z});
			a.push_back(z);
		}
		int j =0;
		sort(a.begin(), a.end(), greater<int>());
		int c=0;
		while(1)
		{
			int f = b.front().first;
			int s = b.front().second;
			b.pop();
			if(s==a[j])
			{
				c++;
				if(f==y)
					break;
				j++;	
			}
			else
			{
				b.push({f,s});
			}
		 }
		 cout<<c<<endl; 
	}
}
