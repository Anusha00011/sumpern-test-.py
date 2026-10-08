# sumpern-test-.py
sumpern test 
# Hopkinson's Test of DC Machines

V = float(input("Enter supply voltage (V): "))
I1 = float(input("Enter current from supply (A): "))
I2 = float(input("Enter motor current (A): "))
I3 = float(input("Enter generator current (A): "))

Rm = float(input("Enter motor armature resistance (ohm): "))
Rg = float(input("Enter generator armature resistance (ohm): "))

# Motor input power
Motor_input = V * I2

# Generator output power
Generator_output = V * I3

# Copper losses
Motor_copper_loss = I2**2 * Rm
Generator_copper_loss = I3**2 * Rg

# Total losses
Total_losses = V * I1

# Motor efficiency
Motor_output = Motor_input - Motor_copper_loss
Motor_efficiency = (Motor_output / Motor_input) * 100

# Generator efficiency
Generator_input = Generator_output + Generator_copper_loss
Generator_efficiency = (Generator_output / Generator_input) * 100

print("\n--- Hopkinson's Test Results ---")
print("Motor