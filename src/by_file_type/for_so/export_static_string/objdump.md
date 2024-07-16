# objdump

## 语法

```bash
objdump -d -j .text elfFile.so > elfFile_objdump_d_j_disassembleSection_text.coffee
objdump -d -r elfFile.so > elfFile_objdump_d_r_disassemReloc.coffee
objdump -a elfFile.so > elfFile_objdump_a_archiveHeaders.coffee
objdump -f elfFile.so > elfFile_objdump_f_fileHeaders.coffee
objdump -h elfFile.so > elfFile_objdump_h_sectionHeaders.coffee
objdump -x elfFile.so > elfFile_objdump_x_allHeaders.coffee
objdump -s elfFile.so > elfFile_objdump_s_fullContents.coffee
objdump -t elfFile.so > elfFile_objdump_t_syms.coffee
objdump -T elfFile.so > elfFile_objdump_T_dynamicSyms.coffee
objdump -r elfFile.so > elfFile_objdump_r_reloc.coffee
objdump -R elfFile.so > elfFile_objdump_R_dynamicReloc.coffee
```

## 举例

### libRehADGd

```bash
objdump -d -j .text libRehADGd_arm64v8a.so > libRehADGd_objdump_d_j_disassembleSection_text.coffee
objdump -d -r libRehADGd_arm64v8a.so > libRehADGd_objdump_d_r_disassemReloc.coffee
objdump -a libRehADGd_arm64v8a.so > libRehADGd_objdump_a_archiveHeaders.coffee
objdump -f libRehADGd_arm64v8a.so > libRehADGd_objdump_f_fileHeaders.coffee
objdump -h libRehADGd_arm64v8a.so > libRehADGd_objdump_h_sectionHeaders.coffee
objdump -x libRehADGd_arm64v8a.so > libRehADGd_objdump_x_allHeaders.coffee
objdump -s libRehADGd_arm64v8a.so > libRehADGd_objdump_s_fullContents.coffee
objdump -t libRehADGd_arm64v8a.so > libRehADGd_objdump_t_syms.coffee
objdump -T libRehADGd_arm64v8a.so > libRehADGd_objdump_T_dynamicSyms.coffee
objdump -r libRehADGd_arm64v8a.so > libRehADGd_objdump_r_reloc.coffee
objdump -R libRehADGd_arm64v8a.so > libRehADGd_objdump_R_dynamicReloc.coffee
```
