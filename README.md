# multiple-inheritance-
Using System;
namespace MyInheritance 
{
   class Shape 
{
      public void setWidth(int w) 
 {
         width = w;
      }
      public void setHeight(int h)
 {
         height = h;
      }
      protected int width;
      protected int height;
   }
   public interface PaintCost 
{
      int getCost(int area);
   }
   class Rectangle : Shape, PaintCost
 {
      public int getArea()
 {
         return (width * height);
      }

      public int getCost(int area)
 {
         return area * 80;
      }
   }
   class RectangleDemo
 {
      static void Main(string[] args) 
{
         Rectangle Rect = new Rectangle();
         int area;
         Rect.setWidth(8);
         Rect.setHeight(10);
         area = Rect.getArea();
         
         Console.WriteLine("Total area: {0}", Rect.getArea());
         Console.WriteLine("Total paint cost: ${0}" , Rect.getCost(area));
         Console.ReadKey();
      }
   }
}
