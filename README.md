# CariDataMhsArr1
import java.io.*;
import java.util.*;
public class CariDataMhsArr1{

//lakukan pengujian method anda disini
public static void main(String []strd) throws IOException
{
 BufferedReader br = new BufferedReader (new InputStreamReader(System.in));
  int bil1=0;
  int bil2=0;
  int bil3=0;
  int bil4=0;
  
  String [][]dataList = {
  {"12410100213","Rudi Tri Setiawan"},
  {"12410100233","Nugraha Caturriyanto Utama"},
  {"13410100002","Bagus Rahmadan"},
  {"13410100019","Irfan Listyo Pamungkas"},
  {"13410100020","Umar"},
  {"13410100021","Bagas Ferry Pradityo"},
  {"13410100028","Iman Nurbela"},
  {"13410100046","Flavianus Yoga Perdana"},
  {"13410100054","Risky Fitri Islamiati"},
  {"13410100064","Achmad Misbahuddin Alharits"},
  {"13410100074","Muchammad Ainul Chakim"},
  {"13410100111","Bagus Handoko"},
  {"13410100121","Adhi Setiawan"},
  {"13410100145","Belly Purna Bahesa"},
  {"13410100147","Satria Wina Adhiguna"},
  {"13410100148","Ahmad Aditiya"},
  {"13410100154","Arizal Azhfahani"},
  {"13410100156","Teghar Firmansyah"},
  {"13410100158","Muchamad Nasrullah"},
  {"13410100160","Moh. Miftahussalam"},
  {"13410100161","Fammy Ibnu Pribadi"},
  {"13410100163","Ryan Gusti Erlangga"},
  {"13410100170","Wildan Bimantoro"},
  {"13410100176","Dhimas Sulistyo Basuki"},
  {"13410100186","M. Ali Fikri"},
  {"13410100203","Aditya Putra Setiajie"},
  {"13410100212","Farid Denianto"},
  {"13410100223","Zainudin Adi Kusuma"},
  {"13410100227","Imas Setiawan Raharja"},
  {"13410100235","Riyo Tata Hubang"},
  {"13410100239","Ahmad Faris"}
  };
 
 Scanner sc = new Scanner (System.in);
  boolean Selesai = false;
  do{
   System.out.println ("");
   System.out.println ("==========================");
   System.out.println (" PENCARIAN DATA MAHASISWA ");
   System.out.println ("==========================");
   System.out.println ("");
   System.out.println ("1. CARI BERDASARKAN NIM");
   System.out.println ("2. CARI BERDASARKAN NAMA");
   System.out.println ("3. EXIT");
   System.out.print ("Pilih pilihan [1-2] : ");
   int piluser = sc.nextInt();
   
   if (piluser == 1)
    {
      System.out.print("Input Nim : ");
      String nim=br.readLine();

      for(int k =0;k<dataList.length;k++){
        if(dataList[k][0].startsWith(nim)){
          System.out.println(dataList[k][0]+" - "+ dataList[k][1] +"\t - Pada data ke "+k);
          bil2=1;
        }
        else{ }
      }
      if(bil2==1){
        // Tidak melakukan apa2
      }
      else{
        System.out.println("data tidak ada ");
       }

    }
    
   if (piluser == 2)
    {
      System.out.print("Input Nama : ");
      String nama=br.readLine();

      for(int k =0;k<dataList.length;k++){
        if(dataList[k][1].contains(nama )){
          System.out.println(dataList[k][0]+" - "+dataList[k][1]+"\t - Pada data ke "+k);
          bil2=1;
        }
        else{ }
      }
      if(bil2==1){ }
      else{
        System.out.println("data tidak ada ");
       }
    } 
    
   if (piluser == 3)
    {
     Selesai = true;
     
    } 
   
    
   
    } while (!Selesai);
    
 }

 
}

