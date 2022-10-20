
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: table erd1- rds copyright © ::**
!theme _none_
skinparam shadowing False
left to right direction
skinparam linetype ortho
skinparam packageStyle rectangle
hide circle



entity "<&grid-three-up>** RIGHTS.DATABASECHANGELOG**" as RIGHTS.DATABASECHANGELOG { 
  - ID : VARCHAR2
  - AUTHOR : VARCHAR2
  - FILENAME : VARCHAR2
  - DATEEXECUTED : TIMESTAMP(6)
  - ORDEREXECUTED : NUMBER
  - EXECTYPE : VARCHAR2
  - MD5SUM : VARCHAR2
  - DESCRIPTION : VARCHAR2
  - COMMENTS : VARCHAR2
  - TAG : VARCHAR2
  - LIQUIBASE : VARCHAR2
  - CONTEXTS : VARCHAR2
  - LABELS : VARCHAR2
  ==
  <&pie-chart>** stats**
      total rows : 0
      total cols : 13
      data size : 520 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** RIGHTS.DATABASECHANGELOGLOCK**" as RIGHTS.DATABASECHANGELOGLOCK { 
  + **(pk) ID : NUMBER**
  --
  - LOCKED : NUMBER
  - LOCKGRANTED : TIMESTAMP(6)
  - LOCKEDBY : VARCHAR2
  ==
  <&pie-chart>** stats**
      total rows : 0
      total cols : 4
      data size : 520 KB
      index size : 520 KB
  --
}


entity "<&grid-three-up>** RIGHTS.RIG_MATRIX_LCD**" as RIGHTS.RIG_MATRIX_LCD { 
  + **(pk) RIG_TIR_ID_SEQ : NUMBER**
  + **(pk) T_ID : NUMBER**
  + **(pk) C_ID : NUMBER**
  + **(pk) RH_ID : NUMBER**
  + **(pk) M_ID : NUMBER**
  + **(pk) S_ID : NUMBER**
  --
  - C_FR_DATE : DATE
  - C_TO_DATE : DATE
  - TL_FR_DATE : DATE
  - TL_TO_DATE : DATE
  - M_FR_DATE : DATE
  - M_TO_DATE : DATE
  - S_FR_DATE : DATE
  - S_TO_DATE : DATE
  - M_QTY : NUMBER
  - S_QTY : NUMBER
  - T_GRP_ID : NUMBER
  - L_GRP_ID : NUMBER
  - M_GRP_ID : NUMBER
  - S_GRP_ID : NUMBER
  ==
  <&pie-chart>** stats**
      total rows : 149,869
      total cols : 20
      data size : 22,960 KB
      index size : 14,800 KB
  --
}


entity "<&grid-three-up>** RIGHTS.RIG_TITLE_RIGHTS**" as RIGHTS.RIG_TITLE_RIGHTS { 
  - ID_SEQ : NUMBER
  - ROW_TYPE : VARCHAR2
  - SYN_REG_ID_SEQ : NUMBER
  - RIG_RTP_ID_SEQ : NUMBER
  - CREATED_BY : NUMBER
  - CREATION_DATE : DATE
  - LAST_UPDATED_BY : NUMBER
  - LAST_UPDATE_DATE : DATE
  - RIG_CSE_ID_SEQ : NUMBER
  - RIGHT_QUALIFIER : VARCHAR2
  - RIGHT_STATUS : VARCHAR2
  - IND_MATRIX_LCD_CHANGED : VARCHAR2
  - SYN_REG_ID_SEQ_PROJECT : NUMBER
  - NB_PROD_CONTRACT : NUMBER
  - RIGHT_COMPLETED_DATE : DATE
  - INITIAL_RIGHT_COMPLETED_DATE : DATE
  ==
  <&pie-chart>** stats**
      total rows : 45,267
      total cols : 16
      data size : 4,240 KB
      index size : 5,600 KB
  --
}


entity "<&grid-three-up>** RIGHTS.RIG_TITLE_STREAMING_CACHE**" as RIGHTS.RIG_TITLE_STREAMING_CACHE { 
  - ID_SEQ : NUMBER
  - SYN_REG_ID_SEQ : NUMBER
  - VALID_FROM_DATE : DATE
  - VALID_TO_DATE : DATE
  - TERRITORY_CODE : VARCHAR2
  - LANGUAGE_CODE : VARCHAR2
  - MARKET_CODE : VARCHAR2
  - SUPPORT_CODE : VARCHAR2
  - SALE_QUALIFIER : VARCHAR2
  - SYN_REG_ID_SEQ_IR : NUMBER
  - SYN_REG_ID_SEQ_OR : NUMBER
  - VALID_IND : VARCHAR2
  - VALID_MSG : VARCHAR2
  - NB_REQUEST : NUMBER
  ==
  <&pie-chart>** stats**
      total rows : 7,571,991
      total cols : 14
      data size : 1,019,264 KB
      index size : 600,384 KB
  --
}


entity "<&grid-three-up>** RIGHTS.RIG_TITLE_STREAMING_CACHE_OLD**" as RIGHTS.RIG_TITLE_STREAMING_CACHE_OLD { 
  - ID_SEQ : NUMBER
  - SYN_REG_ID_SEQ : NUMBER
  - VALID_FROM_DATE : DATE
  - VALID_TO_DATE : DATE
  - TERRITORY_CODE : VARCHAR2
  - LANGUAGE_CODE : VARCHAR2
  - MARKET_CODE : VARCHAR2
  - SUPPORT_CODE : VARCHAR2
  - SALE_QUALIFIER : VARCHAR2
  - SYN_REG_ID_SEQ_IR : NUMBER
  - SYN_REG_ID_SEQ_OR : NUMBER
  - VALID_IND : VARCHAR2
  - VALID_MSG : VARCHAR2
  - NB_REQUEST : NUMBER
  - PURGE_DATE : DATE
  ==
  <&pie-chart>** stats**
      total rows : 0
      total cols : 15
      data size : 80 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** RIGHTS.RIG_TITLE_STREAMING_LOG**" as RIGHTS.RIG_TITLE_STREAMING_LOG { 
  + **(pk) ID_SEQ : NUMBER**
  --
  - SYN_REG_ID_SEQ : NUMBER
  - START_DATE : DATE
  - END_DATE : DATE
  - TERRITORY_CODE : VARCHAR2
  - LANGUAGE_CODE : VARCHAR2
  - MARKET_CODE : VARCHAR2
  - SUPPORT_CODE : VARCHAR2
  - SALE_QUALIFIER : VARCHAR2
  - SYN_REG_ID_SEQ_IR : NUMBER
  - SYN_REG_ID_SEQ_OR : NUMBER
  - VALID_IND : VARCHAR2
  - VALID_MSG : VARCHAR2
  - CACHE_USED : VARCHAR2
  ==
  <&pie-chart>** stats**
      total rows : 31,498,810
      total cols : 14
      data size : 4,285,856 KB
      index size : 1,033,024 KB
  --
}


entity "<&grid-three-up>** RIGHTS.RIG_TREE_RIGHTS**" as RIGHTS.RIG_TREE_RIGHTS { 
  - ID_SEQ : NUMBER
  - ID_SEQ_PARENT : NUMBER
  - RIG_TIR_ID_SEQ : NUMBER
  - RIG_TST_ID_SEQ : NUMBER
  - NODE_ID_SEQ : NUMBER
  - CREATED_BY : NUMBER
  - CREATION_DATE : DATE
  - LAST_UPDATED_BY : NUMBER
  - LAST_UPDATE_DATE : DATE
  ==
  <&pie-chart>** stats**
      total rows : 2,716,681
      total cols : 9
      data size : 163,840 KB
      index size : 294,912 KB
  --
}


@enduml