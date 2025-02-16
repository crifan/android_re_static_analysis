# 导出静态字符串资源信息

导出ELF格式的so文件的字符串资源信息：

## 手动运行命令：单个ELF的so文件

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

## shell脚本自动执行：单个ELF的so文件

用脚本批量处理

* `exportElf_StrResInfo.sh`

```sh
#!/bin/bash
# Function: Export/Extract single ELF file string and resources related info
# Author: Crifan Li
# Usage:
#   exportElf_StrResInfo.sh <inputSoLibFile.so> [<outputFolder>]
# Update: 20240824

# SEPERATOR="--------------------"
SEPERATOR="===================="

function log() {
  echo "${SEPERATOR} $1 ${SEPERATOR}"
}

function extractInputFolder(){
  curInputFile=$1
  # echo "curInputFile=${curInputFile}"
  retInputFolder="$(dirname "${curInputFile}")"
  # echo "retInputFolder=${retInputFolder}"
  # return retInputFolder
  # return $retInputFolder
  # echo ${retInputFolder}
  echo $retInputFolder
}

function extractFilenameNoSuffix(){
  curInputFile=$1
  # echo "curInputFile=${curInputFile}"
  filenameWithSuffix="$(basename "${inputFile}")"
  # echo "filenameWithSuffix=${filenameWithSuffix}"
  filenameNoSuffix=${filenameWithSuffix%.*}
  # echo "filenameNoSuffix=${filenameNoSuffix}"
  echo ${filenameNoSuffix}
}

function initOutputFolerFromInputFolder(){
  inputFolder=$1
  # echo "inputFolder=${inputFolder}"
  outputFoler=$2
  # echo "outputFoler=${outputFoler}"
  if [ -z "$outputFoler" ]
  then
    if [ -z "$inputFolder" ]
    then
      outputFoler="."
    else
      outputFoler=${inputFolder}
    fi
    # echo "outputFoler=${outputFoler}"
    echo ${outputFoler}
  else
    echo ${outputFoler}
  fi
}

inputFile=$1
echo "inputFile=${inputFile}"
outputFoler=$2
echo "outputFoler=${outputFoler}"

# inputFolder="$(dirname "${inputFile}")"
inputFolder=$(extractInputFolder $inputFile)
echo "inputFolder=${inputFolder}"

# elfFileWithSuffix="$(basename "${inputFile}")"
# echo "elfFileWithSuffix=${elfFileWithSuffix}"
# elfFile=${elfFileWithSuffix%.*}
# echo "elfFile=${elfFile}"
elfFile=$(extractFilenameNoSuffix $inputFile)
echo "elfFile=${elfFile}"

# if [ -z "$outputFoler" ]
# then
#   if [ -z "$inputFolder" ]
#   then
#     outputFoler="."
#   else
#     outputFoler=${inputFolder}
#   fi
#   echo "outputFoler=${outputFoler}"
# fi

outputFoler=$(initOutputFolerFromInputFolder $inputFolder $outputFoler)
echo "outputFoler=${outputFoler}"

log "Exporting info use rabin2"
rabin2 -I ${inputFile} > ${outputFoler}/${elfFile}_rabin2_I_identification.coffee
rabin2 -i ${inputFile} > ${outputFoler}/${elfFile}_rabin2_i_imports.coffee
rabin2 -E ${inputFile} > ${outputFoler}/${elfFile}_rabin2_E_exports.coffee
rabin2 -l ${inputFile} > ${outputFoler}/${elfFile}_rabin2_l_libraries.coffee
rabin2 -z ${inputFile} > ${outputFoler}/${elfFile}_rabin2_z_strings.coffee
rabin2 -s ${inputFile} > ${outputFoler}/${elfFile}_rabin2_s_symbols.coffee
rabin2 -S ${inputFile} > ${outputFoler}/${elfFile}_rabin2_S_sections.coffee

log "Exporting info use strings"
strings ${inputFile} > ${outputFoler}/${elfFile}_strings.coffee

log "Exporting info use readelf"
readelf -h ${inputFile} > ${outputFoler}/${elfFile}_readelf_h_header.coffee
readelf -a ${inputFile} > ${outputFoler}/${elfFile}_readelf_a_all.coffee
readelf -e ${inputFile} > ${outputFoler}/${elfFile}_readelf_e_hlS.coffee
readelf -s ${inputFile} > ${outputFoler}/${elfFile}_readelf_s_symbols.coffee
readelf -r ${inputFile} > ${outputFoler}/${elfFile}_readelf_r_relocs.coffee
readelf -l ${inputFile} > ${outputFoler}/${elfFile}_readelf_l_programHeaders_segments.coffee
readelf -S ${inputFile} > ${outputFoler}/${elfFile}_readelf_S_sections.coffee
readelf -x .dynsym ${inputFile} > ${outputFoler}/${elfFile}_readelf_x_hexDump_dynsym.coffee
readelf -p .dynsym ${inputFile} > ${outputFoler}/${elfFile}_readelf_p_stringDump_dynsym.coffee
readelf -p .dynstr ${inputFile} > ${outputFoler}/${elfFile}_readelf_p_stringDump_dynstr.coffee
readelf -n ${inputFile} > ${outputFoler}/${elfFile}_readelf_n_notes.coffee
readelf -d ${inputFile} > ${outputFoler}/${elfFile}_readelf_d_dynamic.coffee

log "Exporting info use objdump"
objdump -d -j .text ${inputFile} > ${outputFoler}/${elfFile}_objdump_d_j_disassembleSection_text.coffee
objdump -d -r ${inputFile} > ${outputFoler}/${elfFile}_objdump_d_r_disassemReloc.coffee
objdump -a ${inputFile} > ${outputFoler}/${elfFile}_objdump_a_archiveHeaders.coffee
objdump -f ${inputFile} > ${outputFoler}/${elfFile}_objdump_f_fileHeaders.coffee
objdump -h ${inputFile} > ${outputFoler}/${elfFile}_objdump_h_sectionHeaders.coffee
objdump -x ${inputFile} > ${outputFoler}/${elfFile}_objdump_x_allHeaders.coffee
objdump -s ${inputFile} > ${outputFoler}/${elfFile}_objdump_s_fullContents.coffee
objdump -t ${inputFile} > ${outputFoler}/${elfFile}_objdump_t_syms.coffee
objdump -T ${inputFile} > ${outputFoler}/${elfFile}_objdump_T_dynamicSyms.coffee
objdump -r ${inputFile} > ${outputFoler}/${elfFile}_objdump_r_reloc.coffee
objdump -R ${inputFile} > ${outputFoler}/${elfFile}_objdump_R_dynamicReloc.coffee

log "Exporting info Done"
```

调用：

```bash
exportElf_StrResInfo.sh xxx.so

exportElf_StrResInfo.sh inputFolder/xxx.so outputFolder
```

提示：

* 运行前，记得加上可执行权限：`chmod +x exportElf_StrResInfo.sh`

## shell脚本自动执行：某目录下所有的ELF的so文件

脚本：

* `batchExportElfInfo.sh`

```sh
#!/bin/bash
# Function: Batch export so file symbols/functions
# Author: Crifan Li
# Usage:
#   batchExportElfInfo.sh <inputFolder_AllSoLibs> <outputFolder>
# Update: 20240824

# SEPERATOR="--------------------"
SEPERATOR="===================="

function log() {
  echo "${SEPERATOR} $1 ${SEPERATOR}"
}

function initOutputFolerFromInputFolder(){
  inputFolder=$1
  # echo "inputFolder=${inputFolder}"
  outputFoler=$2
  # echo "outputFoler=${outputFoler}"
  if [ -z "$outputFoler" ]
  then
    if [ -z "$inputFolder" ]
    then
      outputFoler="."
    else
      outputFoler=${inputFolder}
    fi
    # echo "outputFoler=${outputFoler}"
    echo ${outputFoler}
  else
    echo ${outputFoler}
  fi
}

inputFolder=$1
echo "inputFolder=${inputFolder}"
outputFoler=$2
echo "outputFoler=${outputFoler}"

outputFoler=$(initOutputFolerFromInputFolder $inputFolder $outputFoler)
echo "outputFoler=${outputFoler}"

soFileList=$(ls $inputFolder)
# soFileList=$(ls ${inputFolder})
# soFileList=`ls $inputFolder`
# soFileList=`ls ${inputFolder}`
# echo "soFileList=${soFileList}"
for eachSoFilename in $soFileList
do
  # eachFilename=$eachSoFilename[0,-3]
  # eachFilename=${eachSoFilename%???}
  eachFilename=${eachSoFilename%.*}
  # echo "eachFilename=${eachFilename}"
  # outputFilename="${eachFilename}_rabin2_E_exports.coffee"
  outputFilename="${eachFilename}_rabin2_l_libraries.coffee"
  inputFullFile=$inputFolder/$eachSoFilename
  outputFullFile=$outputFoler/$outputFilename
  echo "$eachSoFilename => $outputFullFile"
  # rabin2 -E $inputFullFile > $outputFullFile
  rabin2 -l $inputFullFile > $outputFullFile
done
```

调用举例：

```bash
batchExportElfInfo.sh inputFoler_allSoLibs oututFoler_exportedAllSoLibsInfo
```

提示：

* 运行前，记得加上可执行权限：`chmod +x batchExportElfInfo.sh`
