#include <iostream>
using namespace std;

class Time { 
	private:
		int hours,
			minutes,
			seconds;
	
	public:	Time() {
		hours=0;
		minutes=0;
		seconds=0;
	}

	Time(int h,int m,int s) {   
		if (h >= 23) {
			h = 0;
		}
		if(s >= 60) {
			s=0;
		}
		if(m >= 60) {
			m = 0;
		}

		hours = h;
		minutes = m;
		seconds = s;
	}

	void addTime(Time t1,Time t2) {         
		seconds = t1.seconds+t2.seconds;
		minutes = seconds / 60;     
		seconds = seconds % 60;
		minutes += (t1.minutes+t2.minutes);
		
		hours += minutes / 60;     
		minutes = minutes % 60;
		hours += (t1.hours+t2.hours);
	}

	void showtime()	{    
		string h = hours < 10 ? "0" + to_string(hours) : to_string(hours);
		string m = minutes < 10 ? "0" + to_string(minutes) : to_string(minutes);
		string s = seconds < 10 ? "0" + to_string(seconds) : to_string(seconds);

		cout<< h <<":"<< m <<":"<< s <<".\n";
	}
};

int main() {
	int hours1, minutes1, seconds1,hours2, minutes2, seconds2;
	cout<<"What o`clock is it (hours)?"<<endl;
	cin>>hours1;
	cout<<"What o`clock is it (minutes)?"<<endl;
	cin>>minutes1;
	cout<<"What o`clock is it (seconds)?"<<endl;
	cin>>seconds1;

	cout<<"What time do you want to add (hours)?"<<endl;
	cin>>hours2;
	cout<<"What time do you want to add (minutes)?"<<endl;
	cin>>minutes2;
	cout<<"What time do you want to add (seconds)?"<<endl;
	cin>>seconds2;
	Time t1(hours1,minutes1,seconds1);
	Time t2(hours2,minutes2,seconds2);
	Time t3;
	t3.addTime(t1,t2);
	cout<<"Time 1 is ";
	t1.showtime();
	cout<<"Time 2 is ";
	t2.showtime();
	cout<<"Sum of two times: ";
	t3.showtime();
}
