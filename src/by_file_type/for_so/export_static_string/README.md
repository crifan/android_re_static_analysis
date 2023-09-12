# 导出静态资源字符串

## 导出ELF格式的so文件的字符串信息

```bash
rabin2 -I elfFile.so > elfFile_rabin2_I_identification.coffee
rabin2 -i elfFile.so > elfFile_rabin2_i_imports.coffee
rabin2 -E elfFile.so > elfFile_rabin2_E_exports.coffee
rabin2 -l elfFile.so > elfFile_rabin2_l_libraries.coffee
rabin2 -z elfFile.so > elfFile_rabin2_z_strings.coffee
rabin2 -s elfFile.so > elfFile_rabin2_s_symbols.coffee
rabin2 -S elfFile.so > elfFile_rabin2_S_sections.coffee


strings elfFile.so > elfFile_strings.coffee


readelf -h elfFile.so > elfFile_readelf_h_header.coffee
readelf -a elfFile.so > elfFile_readelf_a_all.coffee
readelf -e elfFile.so > elfFile_readelf_e_hlS.coffee
readelf -s elfFile.so > elfFile_readelf_s_symbols.coffee
readelf -r elfFile.so > elfFile_readelf_r_relocs.coffee
readelf -l elfFile.so > elfFile_readelf_l_programHeaders_segments.coffee
readelf -S elfFile.so > elfFile_readelf_S_sections.coffee
readelf -x .dynsym elfFile.so > elfFile_readelf_x_hexDump_dynsym.coffee
readelf -p .dynsym elfFile.so > elfFile_readelf_p_stringDump_dynsym.coffee
readelf -p .dynstr elfFile.so > elfFile_readelf_p_stringDump_dynstr.coffee
readelf -n elfFile.so > elfFile_readelf_n_notes.coffee
readelf -d elfFile.so > elfFile_readelf_d_dynamic.coffee


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

### 举例

```bash
rabin2 -I libRehADGd_arm64v8a.so > libRehADGd_rabin2_I_identification.coffee
rabin2 -i libRehADGd_arm64v8a.so > libRehADGd_rabin2_i_imports.coffee
rabin2 -E libRehADGd_arm64v8a.so > libRehADGd_rabin2_E_exports.coffee
rabin2 -l libRehADGd_arm64v8a.so > libRehADGd_rabin2_l_libraries.coffee
rabin2 -z libRehADGd_arm64v8a.so > libRehADGd_rabin2_z_strings.coffee
rabin2 -s libRehADGd_arm64v8a.so > libRehADGd_rabin2_s_symbols.coffee
rabin2 -S libRehADGd_arm64v8a.so > libRehADGd_rabin2_S_sections.coffee

strings libRehADGd_arm64v8a.so > libRehADGd_strings.coffee

readelf -h libRehADGd_arm64v8a.so > libRehADGd_readelf_h_header.coffee
readelf -a libRehADGd_arm64v8a.so > libRehADGd_readelf_a_all.coffee
readelf -e libRehADGd_arm64v8a.so > libRehADGd_readelf_e_hlS.coffee
readelf -s libRehADGd_arm64v8a.so > libRehADGd_readelf_s_symbols.coffee
readelf -r libRehADGd_arm64v8a.so > libRehADGd_readelf_r_relocs.coffee
readelf -l libRehADGd_arm64v8a.so > libRehADGd_readelf_l_programHeaders_segments.coffee
readelf -S libRehADGd_arm64v8a.so > libRehADGd_readelf_S_sections.coffee
readelf -x .dynsym libRehADGd_arm64v8a.so > libRehADGd_readelf_x_hexDump_dynsym.coffee
readelf -p .dynsym libRehADGd_arm64v8a.so > libRehADGd_readelf_p_stringDump_dynsym.coffee
readelf -p .dynstr libRehADGd_arm64v8a.so > libRehADGd_readelf_p_stringDump_dynstr.coffee
readelf -n libRehADGd_arm64v8a.so > libRehADGd_readelf_n_notes.coffee
readelf -d libRehADGd_arm64v8a.so > libRehADGd_readelf_d_dynamic.coffee

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
