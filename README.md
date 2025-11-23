# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
<img width="950" height="1599" alt="image" src="https://github.com/user-attachments/assets/aefbd1e9-f042-4d3b-91b7-33e8d7ca3844" />
<img width="983" height="1600" alt="image" src="https://github.com/user-attachments/assets/f960d84a-4df3-4b53-b2c2-ab8e00a36e18" />
<img width="1080" height="1421" alt="image" src="https://github.com/user-attachments/assets/b362114a-81f5-4959-9116-e2a4f36a0015" />

## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```

## Output:

<img width="1919" height="1042" alt="image" src="https://github.com/user-attachments/assets/2181780d-7618-4310-940b-31bf605d6f09" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12 <br>
Phase Margin = 60 <br>
Gain crossover frequency = 0.907 <br>
Phase crossover frequency = 4.4721 <br>
The system is stable
