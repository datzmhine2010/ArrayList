ArrayList
=========
import java.util.*;
public class Array_List 
{
	private final int Max = 100;
	private int []arr = new int [Max];
	private int n = 0;
	
	public boolean ifExist(int num)
	{
	
	boolean found = false;
	for(int i = 0; i < n; i++)
	{
		if(num == arr[i])
		{
			found = true;
			break;
		}
	}
	return found;
	}
	public void adds(int num)
	{
		if(ifExist(num) == true)
		{
			System.out.println("Exist");
		}
		else
		{
			if(n < Max)
			{
			arr[n] = num;
			System.out.println("Number Added");
			n++;
			}
			else
			{
				System.out.println("Full");
			}
		}
	}
	public void del(int num)
	{
		if(ifExist(num) == true)
		{
			for(int i = 0; i < n; i++)
			{
				if(num == arr[i])//;
				{
					for(int z = i; z < n - 1; z++)
					{
						arr[z] = arr[z + 1];
					}
					System.out.println("Delete Successful");
					n--;
					break;
				}
			}
		}
		else
		{
			System.out.println("Number Not Exist");
		}
	}
	public boolean find(int num)
	{
		if(ifExist(num) == true)
		{
			System.out.println("Number Found...");
		}
		else
		{
			System.out.println("Number Not Found...");
		}
		return false;
	}
	
	public void ins(int index, int element)
	{
		if(ifExist(index) == true)
		{
			System.out.println("NumberExists");
		}
		else
		{
			if(element < n)
			{
				arr[n] = arr[n];
			}
			arr[element] = index;
			n++;
		}
	}
		
	public String toString()
	{
		String display = "{";
		for(int i = 0; i < n; i++)
		{
			if(i == 0)
			{
				display += " " + arr[i];
			}
			else
			{
				display += "," + arr[i];
			}
		}
		display += "}";
		return display;
	}
}
