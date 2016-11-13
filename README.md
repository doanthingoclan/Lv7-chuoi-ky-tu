# Lv7-chuoi-ky-tu
=========================
## I. Chuỗi ký tự .

  - **Khái niệm** .
  
    > + Trong C chuỗi ký tự là một dãy các ký tự trong hai dấu nháy kép. Chuỗi rỗng được ký hiệu như sau
"" bao gồm hai dấu nháy kép đi liền nhau. Khi gặp một chuỗi ký tự, máy sẽ cấp phát một khoảng nhớ cho một 
mảng kiểu char đủ lớn để chứa các ký tự của chuỗi và chứa thêm ký tự '\0' là ký tự kết thúc chuỗi.

    > + **Chú ý** : Cần phân biệt giữa ký tự và chuỗi bao gồm một ký tự. **Ví dụ** : 'A' là ký tự A được mã hóa bằng 1 byte, trong khi "A" là một chuỗi ký tự chứa ký tự A chuỗi này được mã hóa bằng
2 bytes cho ký tự A và ký tự '\0'.

### II. Các thao tác trên chuỗi ký tự.

 **1.Một số hàm thông dụng thuộc string.h**.
  
  - **Hàm strlen** :
        
    > + **Cú pháp** : `int strlen(char s[])` .
        
    > + **Ý nghĩa** : Trả về độ dài của chuỗi s, chính là chỉ số của ký tự NUL trong chuỗi.
    
  - **Hàm strcpy** :
    
    > + **Cú pháp** : `strcpy(char dest[], char source[])` .
    
    > + **Ý nghĩa** : Sao chép nội dung chuỗi source vào chuỗi dest.
    
  - **Hàm strncpy** :
  
    > + **Cú pháp** : ``strncpy(char dest[],char source[],int n)` .
    
    > + **Ý nghĩa** : Tương tự như strcpy nhưng ngừng sao chép sau n ký tự. Trong trường hợp không
    đủ số kýt ự tring source thì hàm sẽ điềm thêm các ký tự trắng vào chuỗi dest.
    
  - **Hàm strcat** :
  
    > + **Cú pháp** : `strcat(char ch1[], char ch2[])` .
    
    > + **Ý nghĩa** : Nối chuỗi ch2 vào cuối chuỗi ch1. Sau lời gọi hàm này độ dài chuỗi ch1 bằng tỏng độ
    dài của cả hai chuỗi ch1 và ch2 trước lời gọi hàm .
    
  - **Hàm strncat** :
  
    > + **Cú pháp** : `strcat(char ch1[],char ch2[],int n)` .
    
    > + **Ý nghĩa** : Tương tự như strcat nhưng chỉ giới hạn n ký tự đầu tiền chủa ch2.
    
  - **Hàm strcmp** :
  
    > + **Cú pháp** : `int strcmp(char ch1[],char ch2[])` .
    
    > + **Ý nghĩa**: So sánh hai chuỗi ch1 và ch2. Nguyễn tắc so sánh theo kiểu từ điền.
    Giá trị trả về:
      
    >                   0 nếu chuoix ch1 bằng chuỗi 2
    >                   >0 nếu chuỗi ch1 lớn hơn chuỗi  ch2
    >                   <0 nếu chuỗi ch1 nhỏ hơn chuỗi ch2
                       
  - **Hàm strncmp** :
  
    > + **Cú pháp** : `int strncmp(char ch1[],char ch2[],int n)` .
    
    > + **Ý nghĩa** : Tương tự hàm strcmp(), nhưng chỉ giới hạn việc so sánh với n ký tự đầu 
    tiên của hai chuỗi .
    
  - **Hàm stricmp** :
  
    > + **Cú pháp** : `int stricmp(char ch1[], char ch2[])` .
    
    > + **Ý nghĩa** : Tương tự hàm strcmp() nhưng không phân biệt chữ in và chữ thường.
    
  - **Hàm strincmp** :
  
    > + **Cú pháp** : `int strincmp(char ch1[],char ch2[],int n)` .
    
    > + **Ý nghĩa** : Tương tự strcmp() nhưng việc so sánh chỉ gới hạn với ký tự đầu tiên của mỗi chuỗi.
    
  - **Hàm strchr** :
  
    > + **Cú pháp** : `char *strchr(char[],char c)` .
    
    > + **Ý nghĩa** : Tìm lần xuất hiện đầu tiên của ký tự c trong chuỗi s, trả về địa chỉ của ký tự này
    
  - **Hàm strrcchar** :
  
    > + **Cú pháp** : `char *strrcchar(char s[],char c)` .
    
    > + **Ý nghĩa** : Nối chuỗi ch2 vào cuối chuỗi ch1. Sau lời gọi hàm này độ dài chuỗi ch1 bằng tỏng độ
    dài của cả hai chuỗi ch1 và ch2 trước lời gọi hàm .
    
  - **Hàm strlwr** :
  
    > + **Cú pháp** : `strlwr(char s[])` .
    
    > + **Ý nghĩa** : Chuyển đổi các chữ in trong chuỗi s sang các chữ thường.
    
  - **Hàm struppr** :
  
    > + **Cú pháp** : `struppr(char s[])` .
    
    > + **Ý nghĩa** : Ngược lại với hàm strlwr().
    
  - **Hàm strset** :
  
    > + **Cú pháp** : `strset(char s[],char c)` .
    
    > + **Ý nghĩa** : Khởi đầu tất cả các ký tự của s bằng ký tự c.
    
  - **Hàm strnset** :
  
    > + **Cú pháp** : `strnset(char s[],char c,int n)` .
    
    > + **Ý nghĩa** : Khởi đầu giá trị cho n ký tự của s bằng ký tự c.
    
  - **Hàm strstr** :
  
    > + **Cú pháp** : `char *strstr(char s1[],char s2[])` .
    
    > + **Ý nghĩa** : Tìm kiếm chuỗi s2 trong chuỗi s1, trả về địa chỉ của lần xuấ hiện đâu tiên của s2 trong s1
    hoặc NULL khi không tìm thấy.
    
 **2. Một số hàm nhập xuất chuỗi thuộc stdio.h**.
 
  - **Hàm gets**: Hàm gets() đọc từ bàm phím tất cả các ký tự và điền vào chuỗi s. Việc đọc kết thúc khi số
    ký tự đọc vào bằng chiều dài cực đại của chuỗi hoặc gặp ký tự xuống dòng '\n' sinh ra khi ra ấn ENTER.
    Kết thúc việc đọc ký tự, một ký tự '\0' (NUL) được gắn vào cuối chuỗi.
 
  - **Hàm puts** :Hàm puts() in nội dung chuỗi ký tự s ra màn hình và thay thế ký hiệu '\0'(NUL) kết thức
  chuỗi bằng ký hiệu xuống dòng '\n'.
  
### 3. Còn trỏ và chuỗi ký tự.

 **1. Cách khai báo**: Trong một chương trình nếu chúng ta có sử dụng chuỗi ký tự, thì máy sẽ cung cấp một
vùng nhớ cho một mảng kiểu char đủ lớn để lưu các ký tự của chuỗi ký tự này và ký tự \0
ở cuối. Khi đó bản thân chuỗi ký tự này là một hằng địa chỉ. Nó chứa địa chỉ đầu của
mảng lưu trữ nó.

 **2. Hàm và chuỗi ký tự.**
 
  - Nếu tham số thực là tên chuỗi ký tự chuoi[20], doiten_chuoi của hàm được khai báo theo 2 mẫu:
  
      + *char ten_chuoi[ ] 
      + *char *ten_chuoi
  
  - Ví dụ: 
  
                        #include <stdio.h>
                         void ham(char ten_chuoi[]);
                         void main()
                         {
                            char chuoi[20];
                            printf("Ten em la gi? => ");
                            gets(chuoi);
                            ham(chuoi); 
                            }
                            void ham(char ten_chuoi[])
                            {
                          printf("%s yeu dau cua long toi!",ten_chuoi);
                      
      
#### 4. Mảng và chuỗi ký tự.  

 - type *pointer_array[size];
  + Ví dụ : char *ma[10]; :sẽ khai báo một mảng 10 con trỏ char có thể được dùng để khai báo một mảng để lưu trữ
địa chỉ của mười chuỗi ký tự nào đó.
 
 - char slist[10][100]; or char *plist[10]; :đều khiến cho C hiểu rằng slist[i] và plist[i] là các con trỏ chỉ đến một đối tượng là char,
hoặc là mảng char



=========================================================
                                                            HẾT

      
      
      
      
      
      
      
      
      
      
      
 
 

  
     
 

 
 
  
    

    
    
    
    
    
        
    
                           
      
      

    
