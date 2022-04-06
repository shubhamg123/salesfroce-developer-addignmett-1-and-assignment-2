# salesfroce-developer-addignmett-1-and-assignment-2
public class assignment1 {
    public static void JG(list<list<String>> dd)
    {   list<list<String>> temp=new list<list<String>>();
        integer z=0;
        for(list<String> kl:dd)
        {
            integer t= kl.size();
             list<String> gl=new list<String>();
            for(integer o=0;o<t;o++)
            {
                list<String> ds=kl[o].Split(';');
                ds.sort();
                set<string> pq=new set<String>();
                pq.addALL(ds);
                list<String> fd=new list<String>();
                fd.addALL(pq);
                String sq=String.join(fd,';');
                gl.add(sq);

               }
            temp.add(gl);
            z++;
            
        } System.debug(temp);
        
        
            }
}

/*
 public class q2
{
public static void rotate()
{
 Integer[] l1 = new Integer[li.size()];
        integer size=li.size();
       
        for(integer i=0;i<size;i++)
        {
            integer r = i+shift;
            if(r>=size)
            {
                r=r-(size);
                l1[r]=li[i];
            }
            else
            {
                l1[r]=li[i];
            }
        }
       
        return l1;
    }
    public static List<Integer> rotatingLeft(List<Integer> li,Integer Shift)
    {
        Integer[] l1 = new Integer[li.size()];
        integer size=li.size();
       
        for(integer i=size-1;i>=0;i--)
        {
            integer r = i-shift;
            if(r<0)
            {
                r=r+(size);
                l1[r]=li[i];
            }
            else
            {
                l1[r]=li[i];
            }
        }
       
        return l1;

}
} */


/* public class quetion3
{
public static void commonelement()
{
list<integer> s=new list<integer>{4,8,7};
list<integer> s2=new list<integer>{4,8,233};
list<integer> s3=new list<integer>{4,8,33};
set<integer> s5=new set<integer>();
s5.addall(s);
s5.retainall(s2);
s5.retainall(s3);
system.debug(s5);
}
}
*/
 /*
 public class quetion4
{
public static void leader()
{
list<integer> l=new list<integer>{149,9,256,80,90,5};
integer n=l.size();
system.debug(l[n-1]);
for(integer i=n-2;i>=0;i--)
{

if(l[i]>max)
{
max=l[i];
system.debug(l[i]);
}
}
}}
*/
  public class assignment2 {
    public static void question1()
    {
List<aggregateresult> li = [Select sum(amount)total,fiscal_year(CreatedDate) from opportunity 
                    where stagename = 'closed won' and Ownerid=:userInfo.getUserid() 
                   Group By fiscal_Year(CreatedDate)];
System.debug(li[0].get('total'));
    }
}
/*
 public class quetion2()
{
public static void main(date first,date last)
{
list<sobject> l=[select id,name from opportunity where closedate>=:first and closdate<=:last and owner.name='saurman d \'souza'];
}
}

in anonymous window
date first=date.newinstance(2022,03,24);
date last=date.newinstance(2022,05,01);


public class ass2question3 {
    public static void apart()
    {
       Map<id,list<opportunity>> d1=new Map<id,list<opportunity>>(); 
         Map<id,list<contact>> d2=new Map<id,list<contact>>();  
        Map<id,list<note>> d3 =new Map<id,list<note>>(); 
        list<account> sc1=[select id,name,(select id,name from opportunities),(select id,name from contacts),(select id from notes) from account where name like 'b%'];
        for(account d:sc1)
        {  System.debug(d.contacts);
         System.debug(d.opportunities);
        System.debug(d.notes);
         d1.put(d.id,d.opportunities);
         d2.put(d.id,d.contacts);
         d3.put(d.id,d.notes);
         }
        System.debug(d1);
        System.debug(d2);
        System.debug(d3);
    }
       

public static void bpart()
    {
       List<Account> ac = [Select id,name,
                        (Select name from Opportunities where name like '%a'),
                        (Select name from Contacts),
                        (Select ID from Notes) from account
                        where id in (Select accountId from Opportunity where name like '%a')];
}}

public class ass2q4 {
public static  void jj()
{
    list<list<sobject>> l1=[FIND 'Test' IN ALL FIELDS RETURNING opportunity(name,id where closedate=THIS_FISCAL_YEAR),account(name,id where OwnerId=:userinfo.getuserid())];
    System.debug(l1);
}
}

public class Assignment2_Q5
{
public static void main()
    {
        List<Account> ac = [Select id,name,
                         (Select name from Opportunities where name like '%a'),
                         (Select name from Contacts),
                         (Select ID from Notes) from account
                         where id in (Select accountId from Opportunity where name like '%a')];
     
        Map<id,List<opportunity>> mp1 = new  Map<id,List<opportunity>>();
        Map<id,List<contact>> mp2 = new  Map<id,List<contact>>();
        Map<id,List<note>> mp3 = new  Map<id,List<note>>();
       
        for(Account a:ac)
        {
           mp1.put(a.id, a.Opportunities);
           mp2.put(a.id, a.Contacts);
           mp3.put(a.id, a.Notes);
        }
       
        System.debug(mp1);
        System.debug(mp2);
        System.debug(mp3);
       
    }
}
 Q6(a): Select Batch_where_student__r.name,count(id) from Student_in_batch__c group by Batch_where_student__r.name;
Q6(b): Select name,Average__c from student__c where Average__c!= null order by Average__c asc;
Q6(c): Select Student_Name__c from student__c where Student_Name__c like '%aa%';
Q6(d): Select (Select name from batches__r),Name,Faculty_for_course__r.name from Course__c
Q6(e): Select COUNT_DISTINCT(Student_Name__c) from student__c;
Q6(f): Select Student_Name__c,Age__c from student__c where Age__c>25;
Q6(g): FIND {testing} In All Fields returning student__c(Student_Name__c),Faculty__c(Name);
Q6(h):
Q6(i): Select name,student__r.Student_Name__c,Faculty_for_course__r.name from Course__c where student__r.Student_Name__c like 'Kri%' and Faculty_for_course__r.name like 'kri%' and name !='php';
        Q6(j):
    

   public static void Q6j(String name,Integer fee1, Integer fee2)
    {
List<Course__c> li  = [Select name,student__r.Student_Name__c from Course__c where name =:name and student__r.Fees_deposited__c >:fee1 and student__r.Fees_deposited__c <:fee2];        
        System.debug(li);
    }
    public static void Q6h(List<String> li)
    {
List<student__c> li1  = [Select Student_Name__c from student__c where Student_Name__c in:li and Admission_date__c = THIS_FISCAL_QUARTER];        
        System.debug(li1);
    }
}

*/
