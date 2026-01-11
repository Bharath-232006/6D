# 6D
2:1 Multiplexer

module mux_2_1
(input sel,
 input i0, i1, 
output y); 
assign y = sel ? i1 : i0; 
endmodule

4:1 Multiplexer

module mux_4:1
( input[1:0] sel, 
input i0,i1,i2,i3, 
output reg y);
 always @(*) begin 
case(sel) 
2'h0: y = i0; 
2'h1: y = i1; 
2'h2: y = i2; 
2'h3: y = i3; 
default: $display
("Invalid sel input"); 
end case
 end endmodule

8:1 Multiplexer

modulemux8to1(s, i, y); 
input [2:0]s; input [7:0]i; 
output y; reg y; 
always @ (i, s) begin       case(s) 
3'd0:y=i[0];     3'd1:y=i[1];    3'd2:y=i[2]; 
3'd3:y=i[3];     3'd4:y=i[4];    3'd5:y=i[5]; 
3'd6:y=i[6]; 
default :y=i[7];
 endcase 
end
 endmodule
