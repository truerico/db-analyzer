```yaml
@startyaml
info:
  version: 1.10.28
dbaccess:
  db_engine: mssql
  user: XXXXXXX
  password: XXXXXXX
  host: test-server
  instance: MSSQLSERVER
  database: adventureworks
  charset: utf8
  raise_on_warnings: true
  port: 1433
  compatibility: mssql_2k12
  sleep_time_after_op: 1.5
  long_op_timeout: 10
option:
  debug_mode: 0
  test_mode: 0
  do_copy_to_static_folder: 0
  result_output_folder: ./result/sample/mssql/adventureworks
  result_static_folder: ./result/static/mssql/test/adventureworks
  csv_delimiter: ','
  csv_quote_char: '"'
  csv_line_terminator: "\r\n"
  csv_quote_mode: 1
  log_loop_every: 1000
  discovery_mode: 0
  debug_start_at_database: ''
diagram:
  table_treemap_padding: true
  table_standard_rows_lower_limit: 0
  table_standard_rows_higer_limit: 100000000
  table_standard_rows_total_item_in_graph: 30
  table_user_rows_lower_limit: 0
  table_user_rows_higer_limit: 0
  table_user_rows_total_item_in_graph: 40
  table_standard_dtsize_lower_limit: 0
  table_standard_dtsize_higer_limit: 1000000000
  table_standard_dtsize_total_item_in_graph: 25
  table_user_dtsize_lower_limit: 10000
  table_user_dtsize_higer_limit: 100000
  table_user_dtsize_total_item_in_graph: 20
  table_standard_cols_lower_limit: 0
  table_standard_cols_higer_limit: 50
  table_standard_cols_total_item_in_graph: 35
  table_user_cols_lower_limit: 51
  table_user_cols_higer_limit: 1000000
  table_user_cols_total_item_in_graph: 20
  plantuml_txt_diagram: 1
  plantuml_png_diagram: 1
  plantuml_svg_diagram: 1
  plantuml_cmd_run_mode: 0
  plantuml_default_limit_size: 20192
meta_analyser:
  do_analyze: 1
  level: 1
  console_mode: 0
  generate_diagram: 1
  generate_csv: 1
  objects_incl:
    tables: null
    views: null
  objects_excl:
    tables: null
    views: null
  columns_incl:
    tables: null
    views: null
  columns_excl:
    tables: null
    views: null
data_analyser:
  do_analyze: 1
  level: 1
  console_mode: 0
  generate_diagram: 1
  generate_csv: 1
  max_txt_length: -1
  min_ratio_percent: -1
  number_top_element: 10
  objects_incl:
    tables: null
    views: null
  objects_excl:
    tables: null
    views: null
  columns_incl:
    tables: null
    views: null
  columns_excl:
    tables: null
    views: null
  datatype_excl:
  - varbinary
  - geography
  - json
  - xml
  - hierarchyid
  - geo_point
  debug_start_at_table: ''
  debug_start_at_combination: -1
data_sampler:
  do_analyze: 1
  level: 1
  console_mode: 0
  generate_csv: 1
  generate_diagram: 1
  number_top_element: 5
  objects_incl:
    tables: null
    views: null
  objects_excl:
    tables: null
    views: null
  columns_incl:
    tables: null
    views: null
  columns_excl:
    tables: null
    views: null
  datatype_excl:
  - varbinary
  - geography
  - json
  - xml
  - hierarchyid
  - geo_point
erd_analyser:
  erd1:
    do_analyze: 1
    level: 3
    include_table_stats: 1
    include_view_stats: 1
    parse_view_related_table: 1
    layout_ventilated: 1
    max_column_count_per_entity: -1
    show_fk_key_on_relation: 1
    fk_filter_mode: 2
    orphan_table_mode: 2
    console_mode: 1
    generate_diagram: 1
    plantuml_shadowing: false
    plantuml_theme: _none_
    plantuml_layout_direction: left to right
    plantuml_linetype: polyline
    plantuml_limit_size: 20192
    plantuml_table_title: "**:: table erd1 \xA9 ::**"
    plantuml_view_title: "**:: view erd1 \xA9 ::**"
    plantuml_use_case_title: "**:: use case \xA9 ::**"
    generate_neo4j_cypher: 1
    generate_use_case: 1
    objects_incl:
      tables: null
      views: null
    objects_excl:
      tables: null
      views: null
    columns_incl:
      tables: null
      views: null
    columns_excl:
      tables: null
      views: null
    manual_table_relation:
    - tbl_aaa .. tbl_bbb
    manual_view_relation:
    - vw_aaa .. vw_bbb
  erd2:
    do_analyze: 0
    level: 3
    include_table_stats: 1
    include_view_stats: 1
    parse_view_related_table: 1
    layout_ventilated: 1
    max_column_count_per_entity: -1
    show_fk_key_on_relation: 0
    fk_filter_mode: 2
    orphan_table_mode: 2
    console_mode: 1
    generate_diagram: 1
    plantuml_shadowing: false
    plantuml_theme: _none_
    plantuml_layout_direction: left to right
    plantuml_linetype: polyline
    plantuml_limit_size: 20192
    plantuml_table_title: "**:: table erd2 \xA9 ::**"
    plantuml_view_title: "**:: view erd2 \xA9 ::**"
    plantuml_use_case_title: "**:: use case \xA9 ::**"
    generate_neo4j_cypher: 1
    generate_use_case: 1
    objects_incl:
      tables: null
      views: null
    objects_excl:
      tables: null
      views: null
    columns_incl:
      tables: null
      views: null
    columns_excl:
      tables: null
      views: null
    manual_table_relation:
    - tbl_aaa .. tbl_bbb
    manual_view_relation:
    - vw_aaa .. vw_bbb

@endyaml
```
