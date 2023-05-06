Download Link: https://assignmentchef.com/product/solved-ee316-lab-04
<br>



Implement the Digital to Analog Converter Using Op-Amp

Purpose

The goal of this laboratory is to explore how an Op-Amp and binary resistive ladder network can be used to construct a simple Digital to Analog (D/A) Converter. The concepts of step size, maximum output range, resolution, and accuracy will also be introduced.

Theoretical Background

A Digital to Analog Converter translates digital information, in the form of discrete bits, into equivalent analog information. A resistive binary ladder can be used as the basis for a Digital to Analog Converter. Additional circuitry is required for a standalone design. However, we will not pursue to discuss that circuitry here. Rather we will study and design the main ladder circuit in conjunction with an Op-Amp, which is the main construct of the D/A Converter.

Figure 4.1

In Figure 4.1, a binary resistive ladder circuit is connected to the negative terminal of the operational amplifier. A resistance R has been added to the positive input to null any stray currents at the negative input. This is the basic design of a simple D/A Converter. Inorder to describe how the circuit converts a digital input into an analog output, we begin by finding the Op-Amp output VO. To do so a step by step Thevenin equivalent approach is used. Let the output due to only input VD be defined as VOD as shown in Figure 4.2.

The Thevenin equivalent drawing is shown in Figure 4.4




Figure 4.4

Using the same approach at the jagged line denoted by Y, you could cut and redraw the circuit as shown in Figure 4.5.




Figure 4.5

Now, applying the same steps as before leads to the Thevenin equivalent circuit shown in Figure

4.6. Where now the Thevenin equivalent resistance is

RTH = 2R||2R + R = = 2R

And the Thevenin voltage is given by




Figure 4.6

Apply the same procedure one more time at point Z to get the circuit shown in Figure 4.7.







Figure 4.7

The new Thevenin equivalent circuit is shown in Figure 4.8 and the Thevenin equivalent resistance

is

RTH = 2R||2R + R = 2R

The final Thevenin voltage for the input VD is







Figure 4.8

Next the circuit is reassembled and the final equivalent form, for input VD, is shown in Figure 4.9. Note that it is not necessary to include the resistor 2R, originally connected to VA which is now at ground, because one terminal of the resistor is at ground and the other terminal at point Z is at virtual ground.




Figure 4.9

The output voltage contributed by the input VD can now be written as

Similarly, the rest of the outputs can be found by repeating the procedures at each input. The resulting equations are




By applying superposition the final output (VO), which results from all four inputs, can be written as




Now so that the output can be described, the input values must be defined and their significance in the D/A configuration must be determined. If we choose the same level for all input voltages, which will be the actual case in this laboratory, it is evident that the maximum output voltage contribution will be from the input at VA. Because VA contributes the maximum output, it is defined as the Most Significant Bit or MSB. Similarly by inspection, it can be seen that VD represents the Least Significant Bit or LSB making the smallest voltage contribution. The bit order can now be defined from MSB to LSB as VA, VB, VC, and VD in that order. By choosing the HIGH inputs to be represented by a single voltage, say 5V, and the LOW inputs all equal to a single voltage, say 0V, we can further define the system as follows on the next page.

The total number of possible inputs producing a unique output can be found using the following equation.

Num_ Permutations = 2<sup>N</sup>

N = Number of inputs or Bits

For example, one possible input of 1 0 1 0, where 1 represents HIGH and 0 represents LOW, will produce the unique output voltage of




VO = – (V

The number of steps associated with this N Bit system, or the number of voltages increases needed to go from zero to the maximum output voltage considering all possible permutations, can be found using




And the step size, or the output voltage increase due to adding 1 LSB, is defined as

Where VIN is defined to be the voltage contribution of the Least Significant Bit at the input. Once the number of steps and step size have been determined, the maximum output voltage is found from

The D/A resolution can be defined as:

The accuracy of the D/A output is usually described by a percent error, which describes the reliability of the device giving the expected output value. To calculate the percent error the following equation is used.

Table 1




<table width="520">

 <tbody>

  <tr>

   <td width="40"></td>

   <td width="51"></td>

   <td colspan="2" width="103">Input State</td>

   <td width="51"></td>

   <td width="98">Simulation</td>

   <td width="85">Theoretical</td>

   <td width="91">Experimental</td>

  </tr>

  <tr>

   <td width="40"></td>

   <td width="51">V<sub>A</sub></td>

   <td width="51">V<sub>B</sub></td>

   <td width="51">V<sub>C</sub></td>

   <td width="51">V<sub>D</sub></td>

   <td width="98">V<sub>O</sub> (V)</td>

   <td width="85">V<sub>O</sub> (V)</td>

   <td width="91">V<sub>O</sub> (V)</td>

  </tr>

  <tr>

   <td width="40">0</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">1</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">2</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">3</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">4</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">5</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">6</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">7</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">8</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">9</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">10</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">11</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">12</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="51">0</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">13</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="51">1</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">14</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="51">0</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

  <tr>

   <td width="40">15</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="51">1</td>

   <td width="98"></td>

   <td width="85"></td>

   <td width="91"></td>

  </tr>

 </tbody>

</table>





