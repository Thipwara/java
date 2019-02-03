
public class Person {
	public String firstname;
	public String lastname;
	public MyDate birthday;
	public int age;
	public  Person(String aFirstname,String aLastname) {
		firstname=aFirstname;
		lastname=aLastname;
		//birthday = null;
		 MyDate birthday = new MyDate();
	}
	public Person(String aFirstname, String aLastname, int aYear, int aMonth,int aDay) {
		firstname=aFirstname;
		lastname=aLastname;
		MyDate birthday = new MyDate(aYear,aMonth,aDay);
		
	}
	public int getAge(MyDate aDate) {
		age = MyDate.yearDiff(birthday, aDate);
		return age;
	}
	public boolean isEligible(MyDate elecDate) {
		if(age>=18)
			return true;
			else
				return false;
		
	}
	public void printPersonInfo() {
		System.out.println("Person: "+firstname+" "+lastname);
		System.out.println("Birthday: "+birthday);
	}
}
