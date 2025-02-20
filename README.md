# IQuitable
csharp
using System;

// 1. Interface definition for IQuitable
public interface IQuitable
{
    void Quit();
}

// 2. Employee class implementing IQuitable
public class Employee : IQuitable
{
    public string Name { get; set; }

    public Employee(string name)
    {
        Name = name;
    }

    // 2. Implementing the Quit() method
    public void Quit()
    {
        Console.WriteLine($"{Name} has quit the job.");
    }
}

class Program
{
    static void Main(string[] args)
    {
        // 3. Using polymorphism: Creating an object of type IQuitable and calling the Quit() method on it
        IQuitable employee = new Employee("John Doe");
        employee.Quit(); // This will call the Quit method of the Employee class

        // 4. Add comments to explain the code
        // The above line creates an instance of the Employee class, but it is referenced as the IQuitable interface type.
        // When we call employee.Quit(), it will call the Quit method implemented in the Employee class.
    }
}
