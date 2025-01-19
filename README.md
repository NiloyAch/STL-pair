#include<bits/stdc++.h>
using namespace std;

#define endl '\n'
#define optimize() ios_base::sync_with_stdio(0);cin.tie(0);cout.tie(0);

int main()
{
    optimize();

    pair<string, vector<int>> p;

    p.first = "niloy";
    p.second = {1,2,3};

    cout << p.first << endl;       //niloy

    for(auto u : p.second)  cout << u << " ";   //1,2,3
    cout << endl;


    pair<string, vector<int>> p;
    p = {"niloy", {1,2,3,4}};

    cout << p.first << " " << p.second.size() << endl;     //niloy  4


    // Declear a pair o integers

	pair<int,int> p;

	p = make_pair ( 2, 3 );
	cout << p.first << " " << p.second << endl;  // 2 3

	p.first++;
	cout << p.first << " " << p.second << endl;  // 3 3


    pair<int,int> p1,p2;

    p1 = {3,5};
    p2 = {1,6};

    if(p1<p2) cout << "YES" << endl;
    else cout << "NO\n";        // no 1st value r dependable


    // Getting minimum of 2 pairs

	p = min ( p1, p2 );
	cout << p.first << " " << p.second << endl; /// 1 6   //small pair tai nibe

	/// Getting maximum of 2 pairs
	p = max ( p1, p2 );
	cout << p.first << " " << p.second << endl; /// 3 5



    /// Sorting pair of integers increasing order

	vector<pair<int,int>> v;
	v.push_back ( { 1, 5 } );
	v.push_back ( { 2, 5 } );
	v.push_back ( { 7, 1 } );
	v.push_back ( { 3, 6 } );
	v.push_back ( { 3, 6 } );
	v.push_back ( { 7, 1 } );

	sort ( v.begin(), v.end() );
	for ( auto u : v ) cout << u.first << " " << u.second << endl;
	cout << endl;
	/**
	1 5
	2 5
	3 6
	3 6
	7 1
	7 1




     /// Sorting pair of integers decreasing order

	vector<pair<int,int>> v;
	v.push_back ( { 1, 5 } );
	v.push_back ( { 2, 5 } );
	v.push_back ( { 7, 1 } );
	v.push_back ( { 3, 6 } );
	v.push_back ( { 3, 6 } );
	v.push_back ( { 7, 1 } );

	sort ( v.rbegin(), v.rend() );
	for ( auto u : v ) cout << u.first << " " << u.second << endl;
	cout << endl;
	/**
	7 1
	7 1
	3 6
	3 6
	2 5
    1 5



    pair<int,int> p[] = {{6,5},{2,3},{4,5},{6,1},{1,9}};

    sort(p,p+5);

    for(int i=0;i<5;i++)  cout << p[i].first << " " << p[i].second << endl;

    /**
    1 9
    2 3
    4 5
    6 1
    6 5
    **/


    vector<pair<string,int>> v;
    v.push_back( {"niloy", 21} );
    v.push_back( {"nihal", 12} );
    v.push_back( {"roni", 11} );
    v.push_back( {"sahir", 9} );
    v.push_back( {"tumu", 56} );


    sort(v.begin(),v.end());

    for(auto u : v)  cout << u.first << " " << u.second << endl;


    /**
    nihal 12
    niloy 21
    roni 11
    sahir 9
    tumu 56
    **/


    /// Making unique pair of integers

	int Sz = unique ( v.begin(), v.end() ) - v.begin();
	cout << Sz << endl;
	for ( int i = 0; i < Sz; i++ ) cout << v[i].first << " " << v[i].second << endl;
	cout << endl;



    ///user input

    pair<int, int> p;
    cin >> p.first >> p.second;

    cout << p.first << " " << p.second << endl;



    /// sorting using comparator
	v = { {2, 3}, {4, 5}, {1, 5}, {1, 6}, {6, 7}, {6, 8} };

	sort ( v.begin(), v.end(), cmp );
	for ( auto u : v ) cout << u.first << " " << u.second << endl;
	cout << endl;

	/**

	6 7
	6 8
	4 5
	2 3
	1 5
	1 6

	*/


	v = { {2, 3}, {4, 5}, {1, 5}, {1, 6}, {6, 7}, {6, 8} };

	for ( int i = 0; i < v.size(); i++ ) v[i].first *= -1;
	sort ( v.begin(), v.end() );
	for ( auto u : v ) cout << (u.first*-1) << " " << u.second << endl;
	cout << endl;

	/**

	6 7
	6 8
	4 5
	2 3
	1 5
	1 6

	*/


	return 0;

}
