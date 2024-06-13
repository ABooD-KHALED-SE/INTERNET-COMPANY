package javaapplication54;
import java.util.Scanner;
public class JavaApplication54 {
    
public static void ShowNamesOfServices(String NamesOfServices[][]){
    for (int Row = 0; Row< NamesOfServices.length; Row++) 
        for (int Column = 0; Column < NamesOfServices[Row].length; Column++) 
            System.out.println(NamesOfServices[Row][Column]+" ");
    }

public static void BuyTypeOfService(int BuyService,int ServiceMoney [],int TotalMoney[]){  
   
 for (int i =BuyService - 1  ; i < 3  ; i++) {
      if (TotalMoney[0] >= ServiceMoney[i]){
          TotalMoney[0] = TotalMoney[0] - ServiceMoney[i];
          System.out.println("تم شراء الباقة ✔");
          System.out.println( "رصيدك المتبقي "+TotalMoney[0]);
          Sleep(2000);
          Clean();
        }
        else 
            System.out.println("رصيد لا يسمح لك ان تشتري هذه الباقة");
        break;
    }  
}

  public static void Clean(){
      System.out.print("\033[H\033[2J");
  }
 public static void Sleep(int SleepingTime){
   try {
       Thread.sleep(SleepingTime);
       
   }catch(InterruptedException e){
   } 
 }
 public static class RequirementFromCoustmer {
   String CoustmerName;
    long PhoneNumber;
   
        
 }
  public static void main(String[] args) {
Scanner in = new Scanner (System.in);
short CodeNumber = 6004;
int BuyService; 
short TestCodeNumber; 
int ChoiceServiceOfNumber,Exit=0,AttemptOfTimes=3 ;    
int [] TotalMoney =new int []{30000};

String  [][]NamesOfServices ={ {"1- باقات المكالمات والرسائل"},{"2- باقات سوا"},{"3- باقات الانترنت"},{"4- باقات مكس  "}  };
String  [][]NamesOfServices1 ={{": باقات المكالمات والرسائل"},{"1- باقة400 دقيقه الشهرية  (1000 رييال )"},{"2- باقة600 دقيقه الاسبوعية(1000 رييال )"},{"3- باقة 750 رسالة نصية(1000 رييال )\n"} } ; 
String  [][]NamesOfServices2 ={{": باقات سوا"},{"1- 65 دقيقه و65 رسالة لمدة يوم  (500 رييال )"},{"2- 100 دقيقة و 100 رسالة لمدة يومين(800 رييال )"},{"3- 250 دقيقه و 300 رسالة لمدة شهر(1500 رييال )\n"} } ; 
String  [][]NamesOfServices3 = {{": باقات الانترنت"},{"1- 10 جيجا لمدة شهر  (2000 رييال )"},{"2- 15 جيجا لمدة شهر(2500 رييال )"},{"3- 8 جيجا لمدة اسبوع(1500 رييال )\n"} } ; 
String  [][]NamesOfServices4 ={{": باقات مكس \n "},{"1- 5جيجا و45 دقيقه و50 رسالة لمدة اسبوع (1500 رييال )"},{"2- 5 جيجا و45 دقيقه و 50 رسالة لمدة اسبوع(1500 رييال )"},{"3- 10 جيجا و 300 دقيقه و150 رسالة لمدة شهر(10000 رييال )\n"} } ; 
  
int ServiceCosts1 []= new int []{1000,1000,1000}; 
int ServiceCosts2 []= new int []{500,800,1500}; 
int ServiceCosts3 []= new int []{2000,2500,1500};
int ServiceCosts4 []= new int []{1500,1500,10000};  

RequirementFromCoustmer Coustmer = new RequirementFromCoustmer();

System.out.println("أدخل ألاسم   :   ");
    Coustmer.CoustmerName=in.nextLine();     
System.out.println("أدخل رقم هاتفك : ");
      Coustmer.PhoneNumber=in.nextLong();
      
System.out.println(" جاري التحقق من الرقم....");
      Sleep(3000);
      
 for (int Count = 2; Count >= 0; Count--) { 
          
 System.out.println("أدخل هذا الكود  6004 :");
      TestCodeNumber=in.nextShort();  
    
  if(TestCodeNumber ==CodeNumber ){
 System.out.println("    ~ اهلا وسهلا بك في شركة عبود للاتصالات والانترنت  ~        "   );
     Sleep(1000);   
 System.out.println("مبلغك الاجمالي في الحساب 30000");
     Sleep(1000);
     Clean();
     break;
  }
  else {
      if(Count != 0)
      System.out.println("أخطأت بادخال الكود  لديك من المحاولات :  "+ Count);    
      else
          System.out.println("انتهت عدد المحاولات لديك الى اللقاء");
      Sleep(1000);
      AttemptOfTimes --; 
  }
     }
 
 if(AttemptOfTimes != Exit){
  for (int Count = 1; Count != Exit ; Count++) { 
     Clean();
 System.out.println("\n أختر احدى الباقات لعرض محتواها ");
    ShowNamesOfServices(NamesOfServices);
 System.out.println("اذا اردت الخروج اضغط على الرقم 0"); 
       ChoiceServiceOfNumber=in.nextInt();
      

 if(ChoiceServiceOfNumber == Exit){
    System.out.println("المتبقي من رصيدك:"+TotalMoney[0]);
     System.out.println("شكرا لاختيار شركتنا عزيزي العميل");
          Exit= Count +1; }
          
switch(ChoiceServiceOfNumber){
 case 1: 
  
      ShowNamesOfServices(NamesOfServices1);
      BuyService=in.nextInt();  
      BuyTypeOfService( BuyService, ServiceCosts1 ,TotalMoney);
     Sleep(1000);
      Clean();
      break;
 case 2:
      System.out.println("أختر احدى الباقات :");
      ShowNamesOfServices(NamesOfServices2);
      BuyService=in.nextInt();
      BuyTypeOfService( BuyService,ServiceCosts2 ,TotalMoney);
       Sleep(1000);
       Clean();
       break;
  case 3:
      System.out.println("أختر احدى الباقات :");
      ShowNamesOfServices(NamesOfServices3);
      BuyService=in.nextInt();
      BuyTypeOfService( BuyService,ServiceCosts3 ,TotalMoney);
      Sleep(1000);
      Clean();
      break;
  case 4:
      System.out.println("أختر احدى الباقات :");
      ShowNamesOfServices(NamesOfServices4);
      BuyService=in.nextInt();
      BuyTypeOfService( BuyService,ServiceCosts4 ,TotalMoney);
      Sleep(1000);
      Clean();
      break;
  default:
        if(ChoiceServiceOfNumber < Exit || ChoiceServiceOfNumber > NamesOfServices.length ){
        System.out.println("عذرا, لا توجد خدمة يرجى ادخال رقم احدى الباقات الموجودة");
        Sleep(2000);
        Clean();
        }
 }
      }
  }
  }
}