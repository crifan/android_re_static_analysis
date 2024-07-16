# readelf


## 语法

```
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
```

## 举例

### libRehADGd

```bash
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
```
