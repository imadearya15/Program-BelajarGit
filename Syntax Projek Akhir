import java.sql.*;    // connection Database
import java.io.*;     // Input & Output
import javax.swing.*;  // Kombinasi script lebih dari 1 dijadikan 1 form 

public class WarungMadura{

    String str;
    BufferedReader br=new BufferedReader(new InputStreamReader(System.in));

    public void lihat() {
        try{
        Class.forName("org.sqlite.JDBC"); //Load Database
        Connection connection=DriverManager.getConnection("JDBC:sqlite:C:/Users/myama/bluej/sqlite/TugasMieGacoan.db"); //Membuat connection
        Statement statement=connection.createStatement(); //Membuat Statement
        
        WarungMadura opsi=new WarungMadura();
        int d;
         
        System.out.println("1. Tabel Menu Gacoan");
        System.out.println("2. Tabel Pembayaran");
        System.out.println("3. Tabel Pelanggan");
        System.out.println("4. Tabel Pemesanan");
        System.out.println("5  Melihat Semua Tabel");
        System.out.print("Pilih tabel yang ingin anda lihat :");
        d=Integer.parseInt(br.readLine());
        System.out.println("");
        switch(d) {
            
            case 1:
            ResultSet rs=statement.executeQuery("select * from MenuGacoan"); //Memilih nama tabel
            ResultSetMetaData rsmd=rs.getMetaData(); //Ambil MetaData
            int kolom=rsmd.getColumnCount();
            //Menampilkan judul kolom
            for(int i=1;i<=kolom;i++)
            {
                System.out.print(rsmd.getColumnName(i)+"\t | \t");
            }
            System.out.println("\n");
            while(rs.next())
            {
                System.out.println(rs.getInt(1)+"\t\t\t"+rs.getString(2)+"\t\t\t"+rs.getInt(3));
            }
            System.out.print("Apakah Anda Ingin Menginput Lagi:"); break;
            
            
            case 2:
            ResultSet rs2=statement.executeQuery("select * from Pembayaran"); //Memilih nama tabel
            ResultSetMetaData rsmd2=rs2.getMetaData(); //Ambil MetaData
            int kolom2=rsmd2.getColumnCount();
            //Menampilkan judul kolom
            for(int i=1;i<=kolom2;i++)
            {
                System.out.print(rsmd2.getColumnName(i)+"\t | \t");
            }
            System.out.println("\n");
            while(rs2.next())
            {
                System.out.println(rs2.getInt(1)+"\t\t\t"+rs2.getString(2)+"\t\t\t"+rs2.getInt(3));
            }
            System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;     

            
            case 3:
            ResultSet rs3=statement.executeQuery("select * from Pelanggan"); //Memilih nama tabel
            ResultSetMetaData rsmd3=rs3.getMetaData(); //Ambil MetaData
            int kolom3=rsmd3.getColumnCount();
            //Menampilkan judul kolom
            for(int i=1;i<=kolom3;i++)
            {
                System.out.print(rsmd3.getColumnName(i)+"\t | \t");
            }
            System.out.println("\n");
            while(rs3.next())
            {
                System.out.println(rs3.getInt(1)+"\t\t\t"+rs3.getString(2));
            }
            System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;   
            
            
            case 4:
            ResultSet rs4=statement.executeQuery("select * from Pemesanan"); //Memilih nama tabel
            ResultSetMetaData rsmd4=rs4.getMetaData(); //Ambil MetaData
            int kolom4=rsmd4.getColumnCount();
            //Menampilkan judul kolom
            for(int i=1;i<=kolom4;i++)
            {
                System.out.print(rsmd4.getColumnName(i)+"\t | \t");
            }
            System.out.println("\n");
            while(rs4.next())
            {
                System.out.println(rs4.getInt(1)+"\t\t\t"+rs4.getInt(2)+"\t\t\t"+rs4.getInt(3)+"\t\t\t"+rs4.getInt(4)+"\t\t\t"+rs4.getString(5)+"\t\t\t"+rs4.getInt(6)+"\t\t\t"+rs4.getInt(7));
            }
            System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;  
            
              
        }
        }catch(Exception e){System.err.println("Error"+e.getMessage());
        }
    
   }

 
   public void tambah() {
        try{
            Class.forName("org.sqlite.JDBC");
            Connection connection=DriverManager.getConnection("JDBC:sqlite:C:/Users/myama/bluej/sqlite/TugasMieGacoan.db");

            Statement statement=connection.createStatement();
            int f;
            
            System.out.println("1. Tabel Menu Gacoan");
            System.out.println("2. Tabel Pembayaran");
            System.out.println("3. Tabel Pelanggan");
            System.out.println("4. Tabel Pemesanan");
            System.out.print("Pilih tabel yang ingin ditambahkan :");
            f=Integer.parseInt(br.readLine());
            System.out.println("");
                
            switch(f){ 
                case 1:
                System.out.print("Masukan ID Menu  :");
                int a=Integer.parseInt(br.readLine());
                System.out.print("Masukan Nama Menu :");
                String b=br.readLine();
                System.out.print("Masukan Harga :");
                int c=Integer.parseInt(br.readLine());
            
                statement.executeUpdate("insert into MenuGacoan (idMenu,NamaMenu,Harga) values('"+a+"','"+b+"','"+c+"');");
        
                statement.close();
                connection.close(); 
                System.out.print("Apakah Anda Ingin Menginput Lagi:"); break; 
                
                case 2:
                System.out.print("Masukan Nomor Nota :");
                int a2=Integer.parseInt(br.readLine());
                System.out.print("Masukan Tanggal Transaksi :");
                String b2=br.readLine();
                System.out.print("Masukan Total Harga :");
                int c2=Integer.parseInt(br.readLine());
            
                statement.executeUpdate("insert into Pembayaran (NomorNota,TanggalTransaksi,TotalHarga) values('"+a2+"','"+b2+"','"+c2+"');");
        
                statement.close();
                connection.close(); 
                System.out.print("Apakah Anda Ingin Menginput Lagi:"); break; 
            
                case 3:
                System.out.print("Masukan ID Pelanggan :");
                int a3=Integer.parseInt(br.readLine());
                System.out.print("Masukan Nama Pelanggan :");
                String b3=br.readLine();
                
            
                statement.executeUpdate("insert into Pelanggan (idPelanggan,NamaPelanggan) values('"+a3+"','"+b3+"');");
        
                statement.close();
                connection.close(); 
                System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;
                
                case 4:
                System.out.print("Masukan ID Pemesanan :");
                int a4=Integer.parseInt(br.readLine());
                System.out.print("Masukan ID Menu :");
                int b4=Integer.parseInt(br.readLine());
                System.out.print("Masukan ID Pelanggan");
                int c4=Integer.parseInt(br.readLine());
                System.out.print("Masukan Nomor Nota :");
                int d4=Integer.parseInt(br.readLine());
                System.out.print("Masukan Menu Yang Dipilih :");
                String e4=br.readLine();
                System.out.print("Masukan Jumlah Pemesanan:");
                int f4=Integer.parseInt(br.readLine());
                System.out.print("Masukan Sub Total :");
                int g4=Integer.parseInt(br.readLine());
            
                statement.executeUpdate("insert into Pemesanan (idPemesanan,idMenu,idPelanggan,NomorNota,MenuPilihan,JmlhPemesanan,SubTotal) values('"+a4+"','"+b4+"','"+c4+"','"+d4+"','"+e4+"','"+f4+"','"+g4+"');");
        
                statement.close();
                connection.close(); 
                System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;
         
            }    
            }catch(Exception e){System.err.println("Error"+e.getMessage());}
   }
   
   public void ubah() {
     try{
         Class.forName("org.sqlite.JDBC");
         Connection connection=DriverManager.getConnection("JDBC:sqlite:C:/Users/myama/bluej/sqlite/TugasMieGacoan.db");
         Statement statement=connection.createStatement();
         int g;
            
            System.out.println("1. Tabel Menu Gacoan");
            System.out.println("2. Tabel Pembayaran");
            System.out.println("3. Tabel Pelanggan");
            System.out.println("4. Tabel Pemesanan");
            System.out.print("Pilih tabel yang ingin diubah :");
            g=Integer.parseInt(br.readLine());
            System.out.println("");
            
         switch(g){
         case 1:
         System.out.print("Masukan ID Menu Baru :");
         int a=Integer.parseInt(br.readLine());
         System.out.print("Masukan Nama Menu Baru :");
         String b=br.readLine();
         System.out.print("Masukan Harga Baru:");
         int c=Integer.parseInt(br.readLine());
         System.out.print("Masukan ID Menu lama :");
         int d=Integer.parseInt(br.readLine());
         statement.executeUpdate("update MenuGacoan set idMenu='"+a+"',NamaMenu='"+b+"',Harga='"+c+"' where idMenu='"+d+"';");
       
         statement.close();
         connection.close();
         System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;
         
         case 2:
         System.out.print("Masukan Nomor Nota Baru :");
         int a2=Integer.parseInt(br.readLine());
         System.out.print("Masukan Tanggal Transaksi Baru :");
         String b2=br.readLine();
         System.out.print("Masukan Total Harga Baru :");
         int c2=Integer.parseInt(br.readLine());
         System.out.print("Masukan Nomor Nota lama :");
         int d2=Integer.parseInt(br.readLine());
         statement.executeUpdate("update Pembayaran set NomorNota='"+a2+"',TanggalTransaksi='"+b2+"',TotalHarga='"+c2+"' where NomorNota='"+d2+"';");
       
         statement.close();
         connection.close();
         System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;
         
         case 3:
         System.out.print("Masukan ID Pelanggan Baru :");
         int a3=Integer.parseInt(br.readLine());
         System.out.print("Masukan Nama Pelanggan Baru :");
         String b3=br.readLine();
         System.out.print("Masukan ID Pelanggan lama :");
         int d3=Integer.parseInt(br.readLine());
         statement.executeUpdate("update Pelanggan set idPelanggan='"+a3+"',NamaPelanggan='"+b3+"' where idPelanggan ='"+d3+"';");
       
         statement.close();
         connection.close();
         System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;
         
         case 4:
         System.out.print("Masukan ID Pemesanan Baru :");
         int a4=Integer.parseInt(br.readLine());
         System.out.print("Masukan ID Menu Baru :");
         int b4=Integer.parseInt(br.readLine());
         System.out.print("Masukan ID Pelanggan Baru :");
         int c4=Integer.parseInt(br.readLine());
         System.out.print("Masukan Nomor Nota Baru :");
         int d4=Integer.parseInt(br.readLine());
         System.out.print("Masukan Menu Yang Dipilih Baru :");
         String e4=br.readLine();
         System.out.print("Masukan Jumlah Pemesanan Baru :");
         int f4=Integer.parseInt(br.readLine());
         System.out.print("Masukan Sub Total Baru :");
         int g4=Integer.parseInt(br.readLine());
         System.out.print("Masukan ID Pemesanan lama :");
         int h4=Integer.parseInt(br.readLine());
            
         statement.executeUpdate("update Pemesanan set idPemesanaan='"+a4+"',idMenu='"+b4+"',idPelanggan='"+c4+"',NomorNota='"+d4+"',MenuPilihan='"+e4+"',JmlhPemesanan='"+f4+"',SubTotal='"+g4+"' where idPemesanaan='"+h4+"';");
       
         statement.close();
         connection.close();
         System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;

         
         
         
        }
        }catch(Exception e){System.err.println("eror"+e.getMessage());}
   }

   public void hapus() {
     try{
         Class.forName("org.sqlite.JDBC");
         Connection connection=DriverManager.getConnection("JDBC:sqlite:C:/Users/myama/bluej/sqlite/TugasMieGacoan.db");
         Statement statement=connection.createStatement();
         
         int h;
            
            System.out.println("1. Tabel Menu Gacoan");
            System.out.println("2. Tabel Pembayaran");
            System.out.println("3. Tabel Pelanggan");
            System.out.println("4. Tabel Pemesanan");
            System.out.print("Pilih tabel yang ingin diubah :");
            h=Integer.parseInt(br.readLine());
            System.out.println("");
            
         
        switch(h){
         case 1:
         System.out.print("Masukan ID Menu yang ingin anda hapus :");
         int a=Integer.parseInt(br.readLine());
        
         statement.executeUpdate("delete from MenuGacoan where idMenu='"+a+"';");
         
         statement.close();
         connection.close();
         System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;
         
         case 2:
         System.out.print("Masukan ID Nota yang ingin anda hapus :");
         int a2=Integer.parseInt(br.readLine());
         
         statement.executeUpdate("delete from Pembayaran where NomorNota='"+a2+"';");
         
         statement.close();
         connection.close();
         System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;
         
         case 3:
         System.out.print("Masukan ID Pelanggan yang ingin anda hapus :");
         int a3=Integer.parseInt(br.readLine());
        
         statement.executeUpdate("delete from Pelanggan where idPelanggan='"+a3+"';");
         
         statement.close();
         connection.close();
         System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;
         
         case 4:
         System.out.print("Masukan ID Pemesanan yang ingin anda hapus:");
         int a4=Integer.parseInt(br.readLine());
       
            
         statement.executeUpdate("delete from Pemesanan where idPemesanaan='"+a4+"';");
         
         statement.close();
         connection.close();
         
         System.out.print("Apakah Anda Ingin Menginput Lagi :"); break;

         
         
         
        }
        }catch(Exception e){System.err.println("error"+e.getMessage());
   }      
}
   public void keluar() { 
      try{
          System.exit(0);
      }catch(Exception e){System.err.print("Error"+e.getMessage());}
   }

public static void main(String[]args) {
 MIEGACOAN opsi=new MIEGACOAN ();
 BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
 int c,d;
 String k;
 System.out.println("============Menu Utama============");
 System.out.println("==========1.Lihat Data============");    // select
 System.out.println("==========2.Tambah Data===========");    // insert
 System.out.println("==========3.Ubah Data=============");    // update
 System.out.println("==========4.Hapus Data============");    // delete
 System.out.println("==========5.Keluar================");    // keluar
 
 try{
 System.out.print("Apakah Anda Ingin Menginput Lagi :");
 while((k=br.readLine()).equals("iya")) {
 System.out.print("Masukan angka yang anda ingin pilih:");
 c=Integer.parseInt(br.readLine());
 System.out.println("");
 
 switch(c) {
     case 1:opsi.lihat(); break;
     case 2:opsi.tambah(); break;
     case 3:opsi.ubah(); break;
     case 4:opsi.hapus(); break;
     case 5:opsi.keluar(); break;
     
     default:System.out.println("Salah Ketik");
 }
}     
}catch(Exception e) {System.err.println("Error"+e.getMessage());}
}
}
