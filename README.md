# hello-world
My first Repository
If I have a string A of concatenated substrings A1, A2, A3, ... AN which are mapped to another string B of concatenated substrings B1, B2, B3, ... BN using some token separator say ("|")
How will you parse a string X to find Y using A and B? Obviously N can be any arbitrary integer > 1.

e.g. (if N = 4)

A = "what|is|the|weather"
B = "red|green|blue|yellow"
Given an input X = "theweatherwhatisthe"
 I need an output of Y ="blueyellowredgreenblue"
 
 import java.util.Scanner;

class Program
{
	public static void main(String args[])
	{
		String s,s1,s2;
		boolean eq;
		StringBuffer buff = new StringBuffer();
		Scanner input = new Scanner(System.in);
		s=input.nextLine();
		s1=input.nextLine();
		String arr[] = s.trim().split("[|]");
		String arr1[] = s1.trim().split("[|]");	
		while(true){
		s2=input.nextLine();
		int size=s2.length();
		for(int i=0;i<s2.length();i++)
		{
			char c = s2.charAt(i);
			buff.append(c);			
			for(int j=0;j<arr.length;j++)
			{
				if(buff.toString().equals(arr[j]))
				{	System.out.print(arr1[j]);
					buff.delete(0,i+1);
					break;
				}
			}
		}
		}
	}
}
