# Vlsi-3
module multiplier(

    input [3:0] a,

    input [3:0] b,

    output [7:0] c

    );

wire [7:0]pp1,pp2,pp3,pp4;

assign pp1={4'b0,a[3]&b[0],a[2]&b[0],a[1]&b[0],a[0]&b[0]};

assign pp2={3'b0,a[3]&b[1],a[2]&b[1],a[1]&b[1],a[0]&b[1],1'b0};

assign pp3={2'b0,a[3]&b[2],a[2]&b[2],a[1]&b[2],a[0]&b[2],2'b0};

assign pp4={1'b0,a[3]&b[3],a[2]&b[3],a[1]&b[3],a[0]&b[3],3'b0};

assign c=pp1+pp2+pp3+pp4;



endmodule

