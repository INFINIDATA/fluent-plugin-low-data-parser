# fluent-plugin-low-data-parser
Fluent source parser plugin for parsing kye/value fileds in Low Data.

# Installation
Use RubyGems:
 not support yet.(comming)
 
# Configuration

<source>
  type tail
  format lowdata
  pType testParser
  pColumn time,test1,test2,test3,test4,test5,test6
  pPattern 14,2,4,4,4,2,4
  tag td.log.data
</source>

<match td.log.data>
  type tdlog
  endpoint xxxxx
  apikey xxxxx
  auto_create_table
  buffer_type file
  buffer_path /path/path
  use_ssl true
</match>


# Output
input log
 : 20160318094049 40 1208 0881 6427 14 6806

output 
 : Key : value
   time : 20160318094049
   test1 : 40
   test2 : 1208
   test3 : 0881
   test4 : 6427
   test5 : 14
   test6 : 6806
   pType : testParser




 
