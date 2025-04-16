### Name: PELLETI SINDHU SRI
### Reg no: 24006305

# EXP2-BOOLEAN FUNCTION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

        module exp2(a,b,c,d,w,x,y,z,f1,f2);
      input a,b,c,d,w,x,y,z;
      output f1,f2;
      wire x1,x2,x3,x4,x5,y1,y2,y3,y4,y5;
      assign x1=((~a)&(~b)&(~c)&(~d));
      assign x2=(a&(~c)&(~d));
      assign x3=((~b)&(c)&(~d));
      assign x4=((~a)&(b)&(c)&(d));
      assign x5=(b&(~c)&(d));
      assign f1=x1|x2|x3|x4|x5;
      
      assign y1=(x&(~y)&(z));
      assign y2=((~x)&(~y)&z);
      assign y3=((~w)&x&y);
      assign y4=(w&(~x)&(y));
      assign y5=(w&x&y);
      assign f2=y1|y2|y3|y4|y5;
      endmodule





**Truth Table**

![2fa4946d-f447-4f44-81dd-0719458fe326](https://github.com/user-attachments/assets/72e25607-056a-4e9b-bbee-c3d26f7841a9)

![f8f0a8ea-a633-46c2-8144-79aca49dbc30](https://github.com/user-attachments/assets/7261c805-9918-4fc6-8995-3a5f2098e4e7)


**RTL**

![5c94a1b4-9d71-41e7-b81e-a5b9e3a42dff](https://github.com/user-attachments/assets/fe00b5fd-93b3-4551-acaf-06882616e247)

![4b7b2d31-3938-41ce-8f79-9380368a5f92](https://github.com/user-attachments/assets/97c31033-e143-453a-ad79-2c4c961d7cc7)


**Waveform**

![285c7fa9-506a-47cb-a95b-6a426a39f5fb](https://github.com/user-attachments/assets/ead68adc-946b-4cca-a635-6b1d1f584090)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

