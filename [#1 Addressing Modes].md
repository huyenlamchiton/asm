# Addressing Modes (Chế độ địa chỉ)
## The three basic modes of addressing are :  
- Register addressing  
- Immediate addressing  
- Memory addressing  
### Register addressing (Chế độ địa chỉ thanh ghi):
Các toán hạng là thanh ghi bên trong CPU và thao tác được thực hiện trong CPU
```
MOV CL, BL ;chuyển nội dung BL vào CL
ADD AL, DL ;AL=AL+DL
```
### Immediate Addressing(Chế độ địa chỉ tức thì) :
dest là thanh ghi hoặc ô nhớ ,source là một hằng số 
```
MOV CL, 100
MOV AX, A00h
```
OR
```
BYTE_VALUE  DB  150    ; A byte value is defined
ADD  BYTE_VALUE, 65
```
### Direct Memory Addressing (Chế độ địa chỉ trực tiếp) :
Toán hạng là ô nhớ mà địa chỉ offset của nó là hằng địa chỉ 16 bit cho trực tiếp trong lệnh.
Trong chế độ địa chỉ bộ nhớ trực tiếp, một trong các toán hạng đề cập đến một vị trí bộ nhớ và toán hạng khác tham chiếu một thanh ghi.
```
MOV AL, [1234h]
MOV [1234h], CX
```
### Indirect Memory Addressing (Chế độ địa chỉ gián tiếp qua thanh ghi):
Một toán hạng là một thanh ghi chứa địa chỉ offset của ô nhớ dữ liệu,toán hạng còn lại chỉ có thể là thanh ghi.
```
MOV AX, [BX]
```
