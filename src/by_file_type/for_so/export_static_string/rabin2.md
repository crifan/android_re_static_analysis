# razbin2

## 语法

```bash
rabin2 -I elfFile.so > elfFile_rabin2_I_identification.coffee
rabin2 -i elfFile.so > elfFile_rabin2_i_imports.coffee
rabin2 -E elfFile.so > elfFile_rabin2_E_exports.coffee
rabin2 -l elfFile.so > elfFile_rabin2_l_libraries.coffee
rabin2 -z elfFile.so > elfFile_rabin2_z_strings.coffee
rabin2 -s elfFile.so > elfFile_rabin2_s_symbols.coffee
rabin2 -S elfFile.so > elfFile_rabin2_S_sections.coffee
```

## 举例

### libRehADGd

```bash
rabin2 -I libRehADGd_arm64v8a.so > libRehADGd_rabin2_I_identification.coffee
rabin2 -i libRehADGd_arm64v8a.so > libRehADGd_rabin2_i_imports.coffee
rabin2 -E libRehADGd_arm64v8a.so > libRehADGd_rabin2_E_exports.coffee
rabin2 -l libRehADGd_arm64v8a.so > libRehADGd_rabin2_l_libraries.coffee
rabin2 -z libRehADGd_arm64v8a.so > libRehADGd_rabin2_z_strings.coffee
rabin2 -s libRehADGd_arm64v8a.so > libRehADGd_rabin2_s_symbols.coffee
rabin2 -S libRehADGd_arm64v8a.so > libRehADGd_rabin2_S_sections.coffee
```
