# 1 PatchableFunction
The PatchableFunction pass used to implement the 'patchable-function' attribute.
  If the function has attribute 'patchable-function', 
  then find the fisrt generate code instruction in the function and replace it with the instruction, 
  which has opcode PATCHABLE_OP.
# 2 XRayInstrumentation
The XRayInstrumentation pass's task is to insert XRay ops instruction.
  Find every MachineBasicBlock's terminator, traversal the instrs, once the opcode of the instr is Return Or ReturnOpcode,
  replace it with instr, which has PATCHABLE_RET opcode.

