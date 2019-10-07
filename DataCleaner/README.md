## DataCleaner

### Dockerfile 

Status: not tested yet

Reference:

see this issue:
https://github.com/datacleaner/DataCleaner/issues/1824

especially this post:
https://github.com/datacleaner/DataCleaner/issues/1824#issuecomment-500976843

### Run

docker run --rm -v ~/jdbc_drivers:/dc_custom_libs -v ~/.datacleaner/5.2.2:/dc_data datacleaner:custom -conf /dc_data/conf.xml -job /dc_data/jobs/Test_datacleaner/table_select_itm_alias_src_val.analysis.xml

