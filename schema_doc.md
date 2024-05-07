# Root

- [1. Property `Root > whitespace`](#whitespace)
  - [1.1. Property `Root > whitespace > spacesOrTabs`](#whitespace_spacesOrTabs)
  - [1.2. Property `Root > whitespace > numberOfSpacesInTabs`](#whitespace_numberOfSpacesInTabs)
  - [1.3. Property `Root > whitespace > wrapLongLines`](#whitespace_wrapLongLines)
  - [1.4. Property `Root > whitespace > wrapLinesLongerThan`](#whitespace_wrapLinesLongerThan)
  - [1.5. Property `Root > whitespace > whiteSpaceBeforeSemiColon`](#whitespace_whiteSpaceBeforeSemiColon)
  - [1.6. Property `Root > whitespace > newLines`](#whitespace_newLines)
    - [1.6.1. Property `Root > whitespace > newLines > preserveExistingEmptyLinesBetweenStatements`](#whitespace_newLines_preserveExistingEmptyLinesBetweenStatements)
    - [1.6.2. Property `Root > whitespace > newLines > preserveExistingEmptyLinesAfterBatchSeparator`](#whitespace_newLines_preserveExistingEmptyLinesAfterBatchSeparator)
    - [1.6.3. Property `Root > whitespace > newLines > emptyLinesBetweenStatements`](#whitespace_newLines_emptyLinesBetweenStatements)
    - [1.6.4. Property `Root > whitespace > newLines > emptyLinesAfterBatchSeparator`](#whitespace_newLines_emptyLinesAfterBatchSeparator)
- [2. Property `Root > lists`](#lists)
  - [2.1. Property `Root > lists > placeFirstItemOnNewLine`](#lists_placeFirstItemOnNewLine)
  - [2.2. Property `Root > lists > placeSubsequentItemsOnNewLines`](#lists_placeSubsequentItemsOnNewLines)
  - [2.3. Property `Root > lists > alignSubsequentItemsWithFirstItem`](#lists_alignSubsequentItemsWithFirstItem)
  - [2.4. Property `Root > lists > alignItemsAcrossClauses`](#lists_alignItemsAcrossClauses)
  - [2.5. Property `Root > lists > indentListItems`](#lists_indentListItems)
  - [2.6. Property `Root > lists > alignItemsToTabStops`](#lists_alignItemsToTabStops)
  - [2.7. Property `Root > lists > alignAliases`](#lists_alignAliases)
  - [2.8. Property `Root > lists > alignComments`](#lists_alignComments)
  - [2.9. Property `Root > lists > placeCommasBeforeItems`](#lists_placeCommasBeforeItems)
  - [2.10. Property `Root > lists > addSpaceBeforeComma`](#lists_addSpaceBeforeComma)
  - [2.11. Property `Root > lists > addSpaceAfterComma`](#lists_addSpaceAfterComma)
  - [2.12. Property `Root > lists > commaAlignment`](#lists_commaAlignment)
- [3. Property `Root > parentheses`](#parentheses)
  - [3.1. Property `Root > parentheses > parenthesisStyle`](#parentheses_parenthesisStyle)
  - [3.2. Property `Root > parentheses > indentParenthesesContents`](#parentheses_indentParenthesesContents)
  - [3.3. Property `Root > parentheses > collapseShortParenthesisContents`](#parentheses_collapseShortParenthesisContents)
  - [3.4. Property `Root > parentheses > collapseParenthesesShorterThan`](#parentheses_collapseParenthesesShorterThan)
  - [3.5. Property `Root > parentheses > addSpacesAroundParentheses`](#parentheses_addSpacesAroundParentheses)
  - [3.6. Property `Root > parentheses > addSpacesInsideParentheses`](#parentheses_addSpacesInsideParentheses)
- [4. Property `Root > casing`](#casing)
  - [4.1. Property `Root > casing > reservedKeywords`](#casing_reservedKeywords)
  - [4.2. Property `Root > casing > builtInFunctions`](#casing_builtInFunctions)
  - [4.3. Property `Root > casing > builtInDataTypes`](#casing_builtInDataTypes)
  - [4.4. Property `Root > casing > globalVariables`](#casing_globalVariables)
  - [4.5. Property `Root > casing > useObjectDefinitionCase`](#casing_useObjectDefinitionCase)
- [5. Property `Root > dml`](#dml)
  - [5.1. Property `Root > dml > placeInsertTableOnNewLine`](#dml_placeInsertTableOnNewLine)
  - [5.2. Property `Root > dml > placeDistinctAndTopClausesOnNewLine`](#dml_placeDistinctAndTopClausesOnNewLine)
  - [5.3. Property `Root > dml > addNewLineAfterDistinctAndTopClauses`](#dml_addNewLineAfterDistinctAndTopClauses)
  - [5.4. Property `Root > dml > collapseShortStatements`](#dml_collapseShortStatements)
  - [5.5. Property `Root > dml > collapseStatementsShorterThan`](#dml_collapseStatementsShorterThan)
  - [5.6. Property `Root > dml > collapseShortSubqueries`](#dml_collapseShortSubqueries)
  - [5.7. Property `Root > dml > collapseSubqueriesShorterThan`](#dml_collapseSubqueriesShorterThan)
  - [5.8. Property `Root > dml > clauses`](#dml_clauses)
    - [5.8.1. Property `Root > dml > clauses > clauseAlignment`](#dml_clauses_clauseAlignment)
    - [5.8.2. Property `Root > dml > clauses > clauseIndentation`](#dml_clauses_clauseIndentation)
  - [5.9. Property `Root > dml > listItems`](#dml_listItems)
    - [5.9.1. Property `Root > dml > listItems > placeFromTableOnNewLine`](#dml_listItems_placeFromTableOnNewLine)
    - [5.9.2. Property `Root > dml > listItems > placeWhereConditionOnNewLine`](#dml_listItems_placeWhereConditionOnNewLine)
    - [5.9.3. Property `Root > dml > listItems > placeGroupByAndOrderByOnNewLine`](#dml_listItems_placeGroupByAndOrderByOnNewLine)
- [6. Property `Root > ddl`](#ddl)
  - [6.1. Property `Root > ddl > parenthesisStyle`](#ddl_parenthesisStyle)
  - [6.2. Property `Root > ddl > indentParenthesesContents`](#ddl_indentParenthesesContents)
  - [6.3. Property `Root > ddl > alignDataTypesAndConstraints`](#ddl_alignDataTypesAndConstraints)
  - [6.4. Property `Root > ddl > placeConstraintsOnNewLines`](#ddl_placeConstraintsOnNewLines)
  - [6.5. Property `Root > ddl > placeConstraintColumnsOnNewLines`](#ddl_placeConstraintColumnsOnNewLines)
  - [6.6. Property `Root > ddl > indentClauses`](#ddl_indentClauses)
  - [6.7. Property `Root > ddl > placeFirstProcedureParameterOnNewLine`](#ddl_placeFirstProcedureParameterOnNewLine)
  - [6.8. Property `Root > ddl > collapseShortStatements`](#ddl_collapseShortStatements)
  - [6.9. Property `Root > ddl > collapseStatementsShorterThan`](#ddl_collapseStatementsShorterThan)
- [7. Property `Root > controlFlow`](#controlFlow)
  - [7.1. Property `Root > controlFlow > placeBeginAndEndOnNewLine`](#controlFlow_placeBeginAndEndOnNewLine)
  - [7.2. Property `Root > controlFlow > indentBeginAndEndKeywords`](#controlFlow_indentBeginAndEndKeywords)
  - [7.3. Property `Root > controlFlow > indentContentsOfStatements`](#controlFlow_indentContentsOfStatements)
  - [7.4. Property `Root > controlFlow > collapseShortStatements`](#controlFlow_collapseShortStatements)
  - [7.5. Property `Root > controlFlow > collapseStatementsShorterThan`](#controlFlow_collapseStatementsShorterThan)
- [8. Property `Root > cte`](#cte)
  - [8.1. Property `Root > cte > parenthesisStyle`](#cte_parenthesisStyle)
  - [8.2. Property `Root > cte > indentContents`](#cte_indentContents)
  - [8.3. Property `Root > cte > placeNameOnNewLine`](#cte_placeNameOnNewLine)
  - [8.4. Property `Root > cte > indentName`](#cte_indentName)
  - [8.5. Property `Root > cte > placeColumnsOnNewLine`](#cte_placeColumnsOnNewLine)
  - [8.6. Property `Root > cte > columnAlignment`](#cte_columnAlignment)
  - [8.7. Property `Root > cte > placeAsOnNewLine`](#cte_placeAsOnNewLine)
  - [8.8. Property `Root > cte > asAlignment`](#cte_asAlignment)
- [9. Property `Root > variables`](#variables)
  - [9.1. Property `Root > variables > alignDataTypesAndValues`](#variables_alignDataTypesAndValues)
  - [9.2. Property `Root > variables > addSpaceBetweenDataTypeAndPrecision`](#variables_addSpaceBetweenDataTypeAndPrecision)
  - [9.3. Property `Root > variables > placeAssignedValueOnNewLineIfLongerThanMaxLineLength`](#variables_placeAssignedValueOnNewLineIfLongerThanMaxLineLength)
  - [9.4. Property `Root > variables > placeEqualsSignOnNewLine`](#variables_placeEqualsSignOnNewLine)
- [10. Property `Root > joinStatements`](#joinStatements)
  - [10.1. Property `Root > joinStatements > join`](#joinStatements_join)
    - [10.1.1. Property `Root > joinStatements > join > placeOnNewLine`](#joinStatements_join_placeOnNewLine)
    - [10.1.2. Property `Root > joinStatements > join > keywordAlignment`](#joinStatements_join_keywordAlignment)
    - [10.1.3. Property `Root > joinStatements > join > insertEmptyLineBetweenJoinClauses`](#joinStatements_join_insertEmptyLineBetweenJoinClauses)
    - [10.1.4. Property `Root > joinStatements > join > placeJoinTableOnNewLine`](#joinStatements_join_placeJoinTableOnNewLine)
    - [10.1.5. Property `Root > joinStatements > join > indentJoinTable`](#joinStatements_join_indentJoinTable)
  - [10.2. Property `Root > joinStatements > on`](#joinStatements_on)
    - [10.2.1. Property `Root > joinStatements > on > placeOnNewLine`](#joinStatements_on_placeOnNewLine)
    - [10.2.2. Property `Root > joinStatements > on > keywordAlignment`](#joinStatements_on_keywordAlignment)
    - [10.2.3. Property `Root > joinStatements > on > placeConditionOnNewLine`](#joinStatements_on_placeConditionOnNewLine)
    - [10.2.4. Property `Root > joinStatements > on > conditionAlignment`](#joinStatements_on_conditionAlignment)
- [11. Property `Root > insertStatements`](#insertStatements)
  - [11.1. Property `Root > insertStatements > columns`](#insertStatements_columns)
    - [11.1.1. Property `Root > insertStatements > columns > parenthesisStyle`](#insertStatements_columns_parenthesisStyle)
    - [11.1.2. Property `Root > insertStatements > columns > indentContents`](#insertStatements_columns_indentContents)
    - [11.1.3. Property `Root > insertStatements > columns > placeSubsequentColumnsOnNewLines`](#insertStatements_columns_placeSubsequentColumnsOnNewLines)
  - [11.2. Property `Root > insertStatements > values`](#insertStatements_values)
    - [11.2.1. Property `Root > insertStatements > values > parenthesisStyle`](#insertStatements_values_parenthesisStyle)
    - [11.2.2. Property `Root > insertStatements > values > indentContents`](#insertStatements_values_indentContents)
    - [11.2.3. Property `Root > insertStatements > values > placeSubsequentValuesOnNewLines`](#insertStatements_values_placeSubsequentValuesOnNewLines)
- [12. Property `Root > functionCalls`](#functionCalls)
  - [12.1. Property `Root > functionCalls > placeArgumentsOnNewLines`](#functionCalls_placeArgumentsOnNewLines)
  - [12.2. Property `Root > functionCalls > addSpacesAroundParentheses`](#functionCalls_addSpacesAroundParentheses)
  - [12.3. Property `Root > functionCalls > addSpacesAroundArgumentList`](#functionCalls_addSpacesAroundArgumentList)
  - [12.4. Property `Root > functionCalls > addSpaceBetweenEmptyParentheses`](#functionCalls_addSpaceBetweenEmptyParentheses)
- [13. Property `Root > caseExpressions`](#caseExpressions)
  - [13.1. Property `Root > caseExpressions > placeExpressionOnNewLine`](#caseExpressions_placeExpressionOnNewLine)
  - [13.2. Property `Root > caseExpressions > placeFirstWhenOnNewLine`](#caseExpressions_placeFirstWhenOnNewLine)
  - [13.3. Property `Root > caseExpressions > whenAlignment`](#caseExpressions_whenAlignment)
  - [13.4. Property `Root > caseExpressions > placeThenOnNewLine`](#caseExpressions_placeThenOnNewLine)
  - [13.5. Property `Root > caseExpressions > thenAlignment`](#caseExpressions_thenAlignment)
  - [13.6. Property `Root > caseExpressions > placeElseOnNewLine`](#caseExpressions_placeElseOnNewLine)
  - [13.7. Property `Root > caseExpressions > alignElseToWhen`](#caseExpressions_alignElseToWhen)
  - [13.8. Property `Root > caseExpressions > placeEndOnNewLine`](#caseExpressions_placeEndOnNewLine)
  - [13.9. Property `Root > caseExpressions > endAlignment`](#caseExpressions_endAlignment)
  - [13.10. Property `Root > caseExpressions > collapseShortCaseExpressions`](#caseExpressions_collapseShortCaseExpressions)
  - [13.11. Property `Root > caseExpressions > collapseCaseExpressionsShorterThan`](#caseExpressions_collapseCaseExpressionsShorterThan)
- [14. Property `Root > operators`](#operators)
  - [14.1. Property `Root > operators > comparison`](#operators_comparison)
    - [14.1.1. Property `Root > operators > comparison > align`](#operators_comparison_align)
    - [14.1.2. Property `Root > operators > comparison > addSpacesAround`](#operators_comparison_addSpacesAround)
  - [14.2. Property `Root > operators > arithmetic`](#operators_arithmetic)
    - [14.2.1. Property `Root > operators > arithmetic > addSpacesAround`](#operators_arithmetic_addSpacesAround)
  - [14.3. Property `Root > operators > andOr`](#operators_andOr)
    - [14.3.1. Property `Root > operators > andOr > placeOnNewLine`](#operators_andOr_placeOnNewLine)
    - [14.3.2. Property `Root > operators > andOr > alignment`](#operators_andOr_alignment)
    - [14.3.3. Property `Root > operators > andOr > placeKeywordBeforeCondition`](#operators_andOr_placeKeywordBeforeCondition)
  - [14.4. Property `Root > operators > between`](#operators_between)
    - [14.4.1. Property `Root > operators > between > placeOnNewLine`](#operators_between_placeOnNewLine)
    - [14.4.2. Property `Root > operators > between > placeAndKeywordOnNewLine`](#operators_between_placeAndKeywordOnNewLine)
    - [14.4.3. Property `Root > operators > between > andAlignment`](#operators_between_andAlignment)
  - [14.5. Property `Root > operators > in`](#operators_in)
    - [14.5.1. Property `Root > operators > in > placeOpeningParenthesisOnNewLine`](#operators_in_placeOpeningParenthesisOnNewLine)
    - [14.5.2. Property `Root > operators > in > alignment`](#operators_in_alignment)
    - [14.5.3. Property `Root > operators > in > placeFirstValueOnNewLine`](#operators_in_placeFirstValueOnNewLine)
    - [14.5.4. Property `Root > operators > in > placeSubsequentValuesOnNewLines`](#operators_in_placeSubsequentValuesOnNewLines)
    - [14.5.5. Property `Root > operators > in > addSpaceAroundInContents`](#operators_in_addSpaceAroundInContents)

**Title:** Root

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

| Property                                 | Pattern | Type   | Deprecated | Definition | Title/Description                      |
| ---------------------------------------- | ------- | ------ | ---------- | ---------- | -------------------------------------- |
| - [whitespace](#whitespace )             | No      | object | No         | -          | Formatting options for whitespace      |
| - [lists](#lists )                       | No      | object | No         | -          | Formatting options for lists           |
| - [parentheses](#parentheses )           | No      | object | No         | -          | Formatting options for parentheses     |
| - [casing](#casing )                     | No      | object | No         | -          | Formatting options for casing          |
| - [dml](#dml )                           | No      | object | No         | -          | Formatting options for data (DML)      |
| - [ddl](#ddl )                           | No      | object | No         | -          | Formatting options for schema (DDL)    |
| - [controlFlow](#controlFlow )           | No      | object | No         | -          | Formatting options for control flow    |
| - [cte](#cte )                           | No      | object | No         | -          | Formatting options for CTEs            |
| - [variables](#variables )               | No      | object | No         | -          | Formatting options for variables       |
| - [joinStatements](#joinStatements )     | No      | object | No         | -          | Formatting options for join statements |
| - [insertStatements](#insertStatements ) | No      | object | No         | -          | Formatting options for inserts         |
| - [functionCalls](#functionCalls )       | No      | object | No         | -          | Formatting options for function calls  |
| - [caseExpressions](#caseExpressions )   | No      | object | No         | -          | Formatting options for CASE            |
| - [operators](#operators )               | No      | object | No         | -          | Formatting options for operators       |

## <a name="whitespace"></a>1. Property `Root > whitespace`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for whitespace

| Property                                                              | Pattern | Type             | Deprecated | Definition | Title/Description                                              |
| --------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | -------------------------------------------------------------- |
| - [spacesOrTabs](#whitespace_spacesOrTabs )                           | No      | enum (of string) | No         | -          | Whether spaces or tabs are used while formatting               |
| - [numberOfSpacesInTabs](#whitespace_numberOfSpacesInTabs )           | No      | integer          | No         | -          | How many spaces are inserted when tab is pressed               |
| - [wrapLongLines](#whitespace_wrapLongLines )                         | No      | boolean          | No         | -          | Whether long lines will be wrapped onto a new line             |
| - [wrapLinesLongerThan](#whitespace_wrapLinesLongerThan )             | No      | integer          | No         | -          | Lines with more than this number of characters will be wrapped |
| - [whiteSpaceBeforeSemiColon](#whitespace_whiteSpaceBeforeSemiColon ) | No      | enum (of string) | No         | -          | Whether spaces will be inserted before semicolons              |
| - [newLines](#whitespace_newLines )                                   | No      | object           | No         | -          | Formatting options for new lines                               |

### <a name="whitespace_spacesOrTabs"></a>1.1. Property `Root > whitespace > spacesOrTabs`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"spaces"`         |

**Description:** Whether spaces or tabs are used while formatting

Must be one of:
* "spaces"
* "tabs"
* "tabsIfPossible"

### <a name="whitespace_numberOfSpacesInTabs"></a>1.2. Property `Root > whitespace > numberOfSpacesInTabs`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `4`       |

**Description:** How many spaces are inserted when tab is pressed

**Examples:** 

```json
2
```

```json
3
```

```json
4
```

```json
6
```

```json
8
```

### <a name="whitespace_wrapLongLines"></a>1.3. Property `Root > whitespace > wrapLongLines`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether long lines will be wrapped onto a new line

### <a name="whitespace_wrapLinesLongerThan"></a>1.4. Property `Root > whitespace > wrapLinesLongerThan`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `120`     |

**Description:** Lines with more than this number of characters will be wrapped

**Examples:** 

```json
80
```

```json
120
```

```json
160
```

### <a name="whitespace_whiteSpaceBeforeSemiColon"></a>1.5. Property `Root > whitespace > whiteSpaceBeforeSemiColon`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"none"`           |

**Description:** Whether spaces will be inserted before semicolons

Must be one of:
* "none"
* "spaceBefore"
* "newLineBefore"

### <a name="whitespace_newLines"></a>1.6. Property `Root > whitespace > newLines`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for new lines

| Property                                                                                                               | Pattern | Type    | Deprecated | Definition | Title/Description                                          |
| ---------------------------------------------------------------------------------------------------------------------- | ------- | ------- | ---------- | ---------- | ---------------------------------------------------------- |
| - [preserveExistingEmptyLinesBetweenStatements](#whitespace_newLines_preserveExistingEmptyLinesBetweenStatements )     | No      | boolean | No         | -          | Preserve existing empty lines between statements           |
| - [preserveExistingEmptyLinesAfterBatchSeparator](#whitespace_newLines_preserveExistingEmptyLinesAfterBatchSeparator ) | No      | boolean | No         | -          | Preserve existing empty lines after batch separator        |
| - [emptyLinesBetweenStatements](#whitespace_newLines_emptyLinesBetweenStatements )                                     | No      | integer | No         | -          | How many empty lines to insert between separate statements |
| - [emptyLinesAfterBatchSeparator](#whitespace_newLines_emptyLinesAfterBatchSeparator )                                 | No      | integer | No         | -          | How many empty lines to insert after a batch separator     |

#### <a name="whitespace_newLines_preserveExistingEmptyLinesBetweenStatements"></a>1.6.1. Property `Root > whitespace > newLines > preserveExistingEmptyLinesBetweenStatements`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Preserve existing empty lines between statements

#### <a name="whitespace_newLines_preserveExistingEmptyLinesAfterBatchSeparator"></a>1.6.2. Property `Root > whitespace > newLines > preserveExistingEmptyLinesAfterBatchSeparator`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Preserve existing empty lines after batch separator

#### <a name="whitespace_newLines_emptyLinesBetweenStatements"></a>1.6.3. Property `Root > whitespace > newLines > emptyLinesBetweenStatements`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `1`       |

**Description:** How many empty lines to insert between separate statements

**Examples:** 

```json
0
```

```json
1
```

```json
2
```

```json
3
```

#### <a name="whitespace_newLines_emptyLinesAfterBatchSeparator"></a>1.6.4. Property `Root > whitespace > newLines > emptyLinesAfterBatchSeparator`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `1`       |

**Description:** How many empty lines to insert after a batch separator

**Examples:** 

```json
0
```

```json
1
```

```json
2
```

```json
3
```

## <a name="lists"></a>2. Property `Root > lists`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for lists

| Property                                                                         | Pattern | Type             | Deprecated | Definition | Title/Description                            |
| -------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | -------------------------------------------- |
| - [placeFirstItemOnNewLine](#lists_placeFirstItemOnNewLine )                     | No      | enum (of string) | No         | -          | -                                            |
| - [placeSubsequentItemsOnNewLines](#lists_placeSubsequentItemsOnNewLines )       | No      | enum (of string) | No         | -          | Place subsequent list items on new lines     |
| - [alignSubsequentItemsWithFirstItem](#lists_alignSubsequentItemsWithFirstItem ) | No      | boolean          | No         | -          | Align subsequent list items with first item  |
| - [alignItemsAcrossClauses](#lists_alignItemsAcrossClauses )                     | No      | boolean          | No         | -          | Align list items across clauses              |
| - [indentListItems](#lists_indentListItems )                                     | No      | boolean          | No         | -          | Indent list items                            |
| - [alignItemsToTabStops](#lists_alignItemsToTabStops )                           | No      | boolean          | No         | -          | Align list items to tab stops                |
| - [alignAliases](#lists_alignAliases )                                           | No      | boolean          | No         | -          | Align aliases to each other                  |
| - [alignComments](#lists_alignComments )                                         | No      | boolean          | No         | -          | Align comments to each other                 |
| - [placeCommasBeforeItems](#lists_placeCommasBeforeItems )                       | No      | boolean          | No         | -          | Place commas before list items               |
| - [addSpaceBeforeComma](#lists_addSpaceBeforeComma )                             | No      | boolean          | No         | -          | Add space before commas                      |
| - [addSpaceAfterComma](#lists_addSpaceAfterComma )                               | No      | boolean          | No         | -          | Add space after commas                       |
| - [commaAlignment](#lists_commaAlignment )                                       | No      | enum (of string) | No         | -          | How commas separating list items are aligned |

### <a name="lists_placeFirstItemOnNewLine"></a>2.1. Property `Root > lists > placeFirstItemOnNewLine`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"never"`          |

Must be one of:
* "always"
* "never"
* "ifSubsequentItems"

### <a name="lists_placeSubsequentItemsOnNewLines"></a>2.2. Property `Root > lists > placeSubsequentItemsOnNewLines`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"always"`         |

**Description:** Place subsequent list items on new lines

Must be one of:
* "always"
* "never"
* "ifLongerThanMaxLineLength"

### <a name="lists_alignSubsequentItemsWithFirstItem"></a>2.3. Property `Root > lists > alignSubsequentItemsWithFirstItem`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Align subsequent list items with first item

### <a name="lists_alignItemsAcrossClauses"></a>2.4. Property `Root > lists > alignItemsAcrossClauses`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Align list items across clauses

### <a name="lists_indentListItems"></a>2.5. Property `Root > lists > indentListItems`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Indent list items

### <a name="lists_alignItemsToTabStops"></a>2.6. Property `Root > lists > alignItemsToTabStops`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Align list items to tab stops

### <a name="lists_alignAliases"></a>2.7. Property `Root > lists > alignAliases`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Align aliases to each other

### <a name="lists_alignComments"></a>2.8. Property `Root > lists > alignComments`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Align comments to each other

### <a name="lists_placeCommasBeforeItems"></a>2.9. Property `Root > lists > placeCommasBeforeItems`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Place commas before list items

### <a name="lists_addSpaceBeforeComma"></a>2.10. Property `Root > lists > addSpaceBeforeComma`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Add space before commas

### <a name="lists_addSpaceAfterComma"></a>2.11. Property `Root > lists > addSpaceAfterComma`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Add space after commas

### <a name="lists_commaAlignment"></a>2.12. Property `Root > lists > commaAlignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"toList"`         |

**Description:** How commas separating list items are aligned

Must be one of:
* "beforeItem"
* "toList"
* "toStatement"

## <a name="parentheses"></a>3. Property `Root > parentheses`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for parentheses

| Property                                                                             | Pattern | Type             | Deprecated | Definition | Title/Description                                                                                  |
| ------------------------------------------------------------------------------------ | ------- | ---------------- | ---------- | ---------- | -------------------------------------------------------------------------------------------------- |
| - [parenthesisStyle](#parentheses_parenthesisStyle )                                 | No      | enum (of string) | No         | -          | The format to use for parenthesized code                                                           |
| - [indentParenthesesContents](#parentheses_indentParenthesesContents )               | No      | boolean          | No         | -          | -                                                                                                  |
| - [collapseShortParenthesisContents](#parentheses_collapseShortParenthesisContents ) | No      | boolean          | No         | -          | Collapse short contents of parentheses onto a single line                                          |
| - [collapseParenthesesShorterThan](#parentheses_collapseParenthesesShorterThan )     | No      | integer          | No         | -          | Contents with fewer than this number of characters will be collapsed onto a single line if enabled |
| - [addSpacesAroundParentheses](#parentheses_addSpacesAroundParentheses )             | No      | boolean          | No         | -          | Whether spaces will be added around parentheses                                                    |
| - [addSpacesInsideParentheses](#parentheses_addSpacesInsideParentheses )             | No      | boolean          | No         | -          | Whether spaces are added around parentheses' contents                                              |

### <a name="parentheses_parenthesisStyle"></a>3.1. Property `Root > parentheses > parenthesisStyle`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"compactSimple"`  |

**Description:** The format to use for parenthesized code

Must be one of:
* "compactSimple"
* "compactToStatement"
* "compactIndented"
* "compactRightAligned"
* "expandedSimple"
* "expandedSplit"
* "expandedToStatement"
* "expandedIndented"
* "expandedRightAligned"

### <a name="parentheses_indentParenthesesContents"></a>3.2. Property `Root > parentheses > indentParenthesesContents`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

### <a name="parentheses_collapseShortParenthesisContents"></a>3.3. Property `Root > parentheses > collapseShortParenthesisContents`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Collapse short contents of parentheses onto a single line

### <a name="parentheses_collapseParenthesesShorterThan"></a>3.4. Property `Root > parentheses > collapseParenthesesShorterThan`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `80`      |

**Description:** Contents with fewer than this number of characters will be collapsed onto a single line if enabled

**Examples:** 

```json
80
```

```json
120
```

```json
160
```

### <a name="parentheses_addSpacesAroundParentheses"></a>3.5. Property `Root > parentheses > addSpacesAroundParentheses`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether spaces will be added around parentheses

### <a name="parentheses_addSpacesInsideParentheses"></a>3.6. Property `Root > parentheses > addSpacesInsideParentheses`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether spaces are added around parentheses' contents

## <a name="casing"></a>4. Property `Root > casing`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for casing

| Property                                                      | Pattern | Type             | Deprecated | Definition | Title/Description                                    |
| ------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ---------------------------------------------------- |
| - [reservedKeywords](#casing_reservedKeywords )               | No      | enum (of string) | No         | -          | How reserved keywords are cased                      |
| - [builtInFunctions](#casing_builtInFunctions )               | No      | enum (of string) | No         | -          | How built-in functions are cased                     |
| - [builtInDataTypes](#casing_builtInDataTypes )               | No      | enum (of string) | No         | -          | How built-in data types are cased                    |
| - [globalVariables](#casing_globalVariables )                 | No      | enum (of string) | No         | -          | How global variables are cased                       |
| - [useObjectDefinitionCase](#casing_useObjectDefinitionCase ) | No      | boolean          | No         | -          | Use the case from the definition when casing objects |

### <a name="casing_reservedKeywords"></a>4.1. Property `Root > casing > reservedKeywords`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"leaveAsIs"`      |

**Description:** How reserved keywords are cased

Must be one of:
* "leaveAsIs"
* "lowercase"
* "uppercase"
* "lowerCamelCase"
* "upperCamelCase"

### <a name="casing_builtInFunctions"></a>4.2. Property `Root > casing > builtInFunctions`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"leaveAsIs"`      |

**Description:** How built-in functions are cased

Must be one of:
* "leaveAsIs"
* "lowercase"
* "uppercase"
* "lowerCamelCase"
* "upperCamelCase"

### <a name="casing_builtInDataTypes"></a>4.3. Property `Root > casing > builtInDataTypes`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"leaveAsIs"`      |

**Description:** How built-in data types are cased

Must be one of:
* "leaveAsIs"
* "lowercase"
* "uppercase"
* "lowerCamelCase"
* "upperCamelCase"

### <a name="casing_globalVariables"></a>4.4. Property `Root > casing > globalVariables`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"leaveAsIs"`      |

**Description:** How global variables are cased

Must be one of:
* "leaveAsIs"
* "lowercase"
* "uppercase"
* "lowerCamelCase"
* "upperCamelCase"

### <a name="casing_useObjectDefinitionCase"></a>4.5. Property `Root > casing > useObjectDefinitionCase`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Use the case from the definition when casing objects

## <a name="dml"></a>5. Property `Root > dml`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for data (DML)

| Property                                                                             | Pattern | Type    | Deprecated | Definition | Title/Description                                                                     |
| ------------------------------------------------------------------------------------ | ------- | ------- | ---------- | ---------- | ------------------------------------------------------------------------------------- |
| - [placeInsertTableOnNewLine](#dml_placeInsertTableOnNewLine )                       | No      | boolean | No         | -          | In INSERT table statements, place table name on a new line                            |
| - [placeDistinctAndTopClausesOnNewLine](#dml_placeDistinctAndTopClausesOnNewLine )   | No      | boolean | No         | -          | Whether to place DISTINCT and TOP clauses on a new line                               |
| - [addNewLineAfterDistinctAndTopClauses](#dml_addNewLineAfterDistinctAndTopClauses ) | No      | boolean | No         | -          | Whether to add a new line after DISTINCT and TOP clauses                              |
| - [collapseShortStatements](#dml_collapseShortStatements )                           | No      | boolean | No         | -          | Collapse short statements onto a single line                                          |
| - [collapseStatementsShorterThan](#dml_collapseStatementsShorterThan )               | No      | integer | No         | -          | Statements that are shorter than this will be collapsed onto a single line if enabled |
| - [collapseShortSubqueries](#dml_collapseShortSubqueries )                           | No      | boolean | No         | -          | Collapse short subqueries onto a single line                                          |
| - [collapseSubqueriesShorterThan](#dml_collapseSubqueriesShorterThan )               | No      | integer | No         | -          | Subqueries that are shorter than this will be collapsed onto a single line if enabled |
| - [clauses](#dml_clauses )                                                           | No      | object  | No         | -          | Formatting options for DML clauses                                                    |
| - [listItems](#dml_listItems )                                                       | No      | object  | No         | -          | Formatting options for DML list items                                                 |

### <a name="dml_placeInsertTableOnNewLine"></a>5.1. Property `Root > dml > placeInsertTableOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** In INSERT table statements, place table name on a new line

### <a name="dml_placeDistinctAndTopClausesOnNewLine"></a>5.2. Property `Root > dml > placeDistinctAndTopClausesOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to place DISTINCT and TOP clauses on a new line

### <a name="dml_addNewLineAfterDistinctAndTopClauses"></a>5.3. Property `Root > dml > addNewLineAfterDistinctAndTopClauses`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to add a new line after DISTINCT and TOP clauses

### <a name="dml_collapseShortStatements"></a>5.4. Property `Root > dml > collapseShortStatements`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Collapse short statements onto a single line

### <a name="dml_collapseStatementsShorterThan"></a>5.5. Property `Root > dml > collapseStatementsShorterThan`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `80`      |

**Description:** Statements that are shorter than this will be collapsed onto a single line if enabled

**Examples:** 

```json
80
```

```json
120
```

```json
160
```

### <a name="dml_collapseShortSubqueries"></a>5.6. Property `Root > dml > collapseShortSubqueries`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Collapse short subqueries onto a single line

### <a name="dml_collapseSubqueriesShorterThan"></a>5.7. Property `Root > dml > collapseSubqueriesShorterThan`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `80`      |

**Description:** Subqueries that are shorter than this will be collapsed onto a single line if enabled

**Examples:** 

```json
80
```

```json
120
```

```json
160
```

### <a name="dml_clauses"></a>5.8. Property `Root > dml > clauses`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for DML clauses

| Property                                               | Pattern | Type             | Deprecated | Definition | Title/Description                                            |
| ------------------------------------------------------ | ------- | ---------------- | ---------- | ---------- | ------------------------------------------------------------ |
| - [clauseAlignment](#dml_clauses_clauseAlignment )     | No      | enum (of string) | No         | -          | How clauses withing DML statements are aligned               |
| - [clauseIndentation](#dml_clauses_clauseIndentation ) | No      | integer          | No         | -          | The number of spaces to indent clauses within DML statements |

#### <a name="dml_clauses_clauseAlignment"></a>5.8.1. Property `Root > dml > clauses > clauseAlignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"leftAligned"`    |

**Description:** How clauses withing DML statements are aligned

Must be one of:
* "leftAligned"
* "rightAligned"
* "toFirstListItem"

#### <a name="dml_clauses_clauseIndentation"></a>5.8.2. Property `Root > dml > clauses > clauseIndentation`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `0`       |

**Description:** The number of spaces to indent clauses within DML statements

**Examples:** 

```json
0
```

```json
1
```

```json
2
```

```json
3
```

```json
4
```

```json
6
```

```json
8
```

### <a name="dml_listItems"></a>5.9. Property `Root > dml > listItems`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for DML list items

| Property                                                                             | Pattern | Type             | Deprecated | Definition | Title/Description                                                            |
| ------------------------------------------------------------------------------------ | ------- | ---------------- | ---------- | ---------- | ---------------------------------------------------------------------------- |
| - [placeFromTableOnNewLine](#dml_listItems_placeFromTableOnNewLine )                 | No      | enum (of string) | No         | -          | When to place the table in a DML statement on a new line                     |
| - [placeWhereConditionOnNewLine](#dml_listItems_placeWhereConditionOnNewLine )       | No      | enum (of string) | No         | -          | When to place a WHERE condition in a DML statement on a new line             |
| - [placeGroupByAndOrderByOnNewLine](#dml_listItems_placeGroupByAndOrderByOnNewLine ) | No      | enum (of string) | No         | -          | When to place GROUP BY and ORDER BY clauses in a DML statement on a new line |

#### <a name="dml_listItems_placeFromTableOnNewLine"></a>5.9.1. Property `Root > dml > listItems > placeFromTableOnNewLine`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"never"`          |

**Description:** When to place the table in a DML statement on a new line

Must be one of:
* "always"
* "never"
* "ifMultiple"

#### <a name="dml_listItems_placeWhereConditionOnNewLine"></a>5.9.2. Property `Root > dml > listItems > placeWhereConditionOnNewLine`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"never"`          |

**Description:** When to place a WHERE condition in a DML statement on a new line

Must be one of:
* "always"
* "never"
* "ifMultiple"

#### <a name="dml_listItems_placeGroupByAndOrderByOnNewLine"></a>5.9.3. Property `Root > dml > listItems > placeGroupByAndOrderByOnNewLine`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"never"`          |

**Description:** When to place GROUP BY and ORDER BY clauses in a DML statement on a new line

Must be one of:
* "always"
* "never"
* "ifMultiple"

## <a name="ddl"></a>6. Property `Root > ddl`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for schema (DDL)

| Property                                                                               | Pattern | Type             | Deprecated | Definition | Title/Description                                                                         |
| -------------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ----------------------------------------------------------------------------------------- |
| - [parenthesisStyle](#ddl_parenthesisStyle )                                           | No      | enum (of string) | No         | -          | The format to use for parenthesized DDL code                                              |
| - [indentParenthesesContents](#ddl_indentParenthesesContents )                         | No      | boolean          | No         | -          | Whether the contents of parentheses in DDL statements are indented                        |
| - [alignDataTypesAndConstraints](#ddl_alignDataTypesAndConstraints )                   | No      | boolean          | No         | -          | Whether to align data types and constraints                                               |
| - [placeConstraintsOnNewLines](#ddl_placeConstraintsOnNewLines )                       | No      | boolean          | No         | -          | Whether to place constraints on a new line                                                |
| - [placeConstraintColumnsOnNewLines](#ddl_placeConstraintColumnsOnNewLines )           | No      | enum (of string) | No         | -          | When to place constraint columns on a new line                                            |
| - [indentClauses](#ddl_indentClauses )                                                 | No      | boolean          | No         | -          | Whether to indent clauses in DDL statements                                               |
| - [placeFirstProcedureParameterOnNewLine](#ddl_placeFirstProcedureParameterOnNewLine ) | No      | enum (of string) | No         | -          | Whether to place the first parameter of a stored procedure on a new line                  |
| - [collapseShortStatements](#ddl_collapseShortStatements )                             | No      | boolean          | No         | -          | Collapse short DDL statements onto a single line                                          |
| - [collapseStatementsShorterThan](#ddl_collapseStatementsShorterThan )                 | No      | integer          | No         | -          | DDL statements that are shorter than this will be collapsed onto a single line if enabled |

### <a name="ddl_parenthesisStyle"></a>6.1. Property `Root > ddl > parenthesisStyle`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"compactSimple"`  |

**Description:** The format to use for parenthesized DDL code

Must be one of:
* "compactSimple"
* "compactToStatement"
* "compactIndented"
* "compactRightAligned"
* "expandedSimple"
* "expandedSplit"
* "expandedToStatement"
* "expandedIndented"
* "expandedRightAligned"

### <a name="ddl_indentParenthesesContents"></a>6.2. Property `Root > ddl > indentParenthesesContents`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether the contents of parentheses in DDL statements are indented

### <a name="ddl_alignDataTypesAndConstraints"></a>6.3. Property `Root > ddl > alignDataTypesAndConstraints`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether to align data types and constraints

### <a name="ddl_placeConstraintsOnNewLines"></a>6.4. Property `Root > ddl > placeConstraintsOnNewLines`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to place constraints on a new line

### <a name="ddl_placeConstraintColumnsOnNewLines"></a>6.5. Property `Root > ddl > placeConstraintColumnsOnNewLines`

|              |                               |
| ------------ | ----------------------------- |
| **Type**     | `enum (of string)`            |
| **Required** | No                            |
| **Default**  | `"ifLongerThanMaxLineLength"` |

**Description:** When to place constraint columns on a new line

Must be one of:
* "always"
* "ifLongerThanMaxLineLength"
* "ifLongerOrMultipleColumns"

### <a name="ddl_indentClauses"></a>6.6. Property `Root > ddl > indentClauses`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to indent clauses in DDL statements

### <a name="ddl_placeFirstProcedureParameterOnNewLine"></a>6.7. Property `Root > ddl > placeFirstProcedureParameterOnNewLine`

|              |                     |
| ------------ | ------------------- |
| **Type**     | `enum (of string)`  |
| **Required** | No                  |
| **Default**  | `"ifMultipleItems"` |

**Description:** Whether to place the first parameter of a stored procedure on a new line

Must be one of:
* "always"
* "never"
* "ifMultipleItems"

### <a name="ddl_collapseShortStatements"></a>6.8. Property `Root > ddl > collapseShortStatements`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Collapse short DDL statements onto a single line

### <a name="ddl_collapseStatementsShorterThan"></a>6.9. Property `Root > ddl > collapseStatementsShorterThan`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `80`      |

**Description:** DDL statements that are shorter than this will be collapsed onto a single line if enabled

**Examples:** 

```json
80
```

```json
120
```

```json
160
```

## <a name="controlFlow"></a>7. Property `Root > controlFlow`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for control flow

| Property                                                                       | Pattern | Type    | Deprecated | Definition | Title/Description                                                                                  |
| ------------------------------------------------------------------------------ | ------- | ------- | ---------- | ---------- | -------------------------------------------------------------------------------------------------- |
| - [placeBeginAndEndOnNewLine](#controlFlow_placeBeginAndEndOnNewLine )         | No      | boolean | No         | -          | Whether BEGIN and END keywords are placed on new lines                                             |
| - [indentBeginAndEndKeywords](#controlFlow_indentBeginAndEndKeywords )         | No      | boolean | No         | -          | Whether to indent BEGIN and END keywords                                                           |
| - [indentContentsOfStatements](#controlFlow_indentContentsOfStatements )       | No      | boolean | No         | -          | Whether the contents of control flow statements are indented                                       |
| - [collapseShortStatements](#controlFlow_collapseShortStatements )             | No      | boolean | No         | -          | Collapse short control flow statements onto a single line                                          |
| - [collapseStatementsShorterThan](#controlFlow_collapseStatementsShorterThan ) | No      | integer | No         | -          | Control flow statements that are shorter than this will be collapsed onto a single line if enabled |

### <a name="controlFlow_placeBeginAndEndOnNewLine"></a>7.1. Property `Root > controlFlow > placeBeginAndEndOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether BEGIN and END keywords are placed on new lines

### <a name="controlFlow_indentBeginAndEndKeywords"></a>7.2. Property `Root > controlFlow > indentBeginAndEndKeywords`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to indent BEGIN and END keywords

### <a name="controlFlow_indentContentsOfStatements"></a>7.3. Property `Root > controlFlow > indentContentsOfStatements`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether the contents of control flow statements are indented

### <a name="controlFlow_collapseShortStatements"></a>7.4. Property `Root > controlFlow > collapseShortStatements`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Collapse short control flow statements onto a single line

### <a name="controlFlow_collapseStatementsShorterThan"></a>7.5. Property `Root > controlFlow > collapseStatementsShorterThan`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `80`      |

**Description:** Control flow statements that are shorter than this will be collapsed onto a single line if enabled

**Examples:** 

```json
80
```

```json
120
```

```json
160
```

## <a name="cte"></a>8. Property `Root > cte`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for CTEs

| Property                                               | Pattern | Type             | Deprecated | Definition | Title/Description                                |
| ------------------------------------------------------ | ------- | ---------------- | ---------- | ---------- | ------------------------------------------------ |
| - [parenthesisStyle](#cte_parenthesisStyle )           | No      | enum (of string) | No         | -          | The format to use for parenthesized CTE code     |
| - [indentContents](#cte_indentContents )               | No      | boolean          | No         | -          | Whether to indent clauses in CTE statements      |
| - [placeNameOnNewLine](#cte_placeNameOnNewLine )       | No      | boolean          | No         | -          | Whether the CTE name is placed on a new line     |
| - [indentName](#cte_indentName )                       | No      | boolean          | No         | -          | Whether the CTE name is indented                 |
| - [placeColumnsOnNewLine](#cte_placeColumnsOnNewLine ) | No      | boolean          | No         | -          | Whether the CTE columns are placed on a new line |
| - [columnAlignment](#cte_columnAlignment )             | No      | enum (of string) | No         | -          | How the columns in a CTE are aligned             |
| - [placeAsOnNewLine](#cte_placeAsOnNewLine )           | No      | boolean          | No         | -          | Whether the AS keyword is placed on a new line   |
| - [asAlignment](#cte_asAlignment )                     | No      | enum (of string) | No         | -          | How the AS keyword is aligned                    |

### <a name="cte_parenthesisStyle"></a>8.1. Property `Root > cte > parenthesisStyle`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"compactSimple"`  |

**Description:** The format to use for parenthesized CTE code

Must be one of:
* "compactSimple"
* "compactToStatement"
* "compactIndented"
* "compactRightAligned"
* "expandedSimple"
* "expandedSplit"
* "expandedToStatement"
* "expandedIndented"
* "expandedRightAligned"

### <a name="cte_indentContents"></a>8.2. Property `Root > cte > indentContents`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to indent clauses in CTE statements

### <a name="cte_placeNameOnNewLine"></a>8.3. Property `Root > cte > placeNameOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether the CTE name is placed on a new line

### <a name="cte_indentName"></a>8.4. Property `Root > cte > indentName`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether the CTE name is indented

### <a name="cte_placeColumnsOnNewLine"></a>8.5. Property `Root > cte > placeColumnsOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether the CTE columns are placed on a new line

### <a name="cte_columnAlignment"></a>8.6. Property `Root > cte > columnAlignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"leftAligned"`    |

**Description:** How the columns in a CTE are aligned

Must be one of:
* "indented"
* "leftAligned"
* "rightAligned"

### <a name="cte_placeAsOnNewLine"></a>8.7. Property `Root > cte > placeAsOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether the AS keyword is placed on a new line

### <a name="cte_asAlignment"></a>8.8. Property `Root > cte > asAlignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"leftAligned"`    |

**Description:** How the AS keyword is aligned

Must be one of:
* "indented"
* "leftAligned"
* "rightAligned"

## <a name="variables"></a>9. Property `Root > variables`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for variables

| Property                                                                                                                   | Pattern | Type    | Deprecated | Definition | Title/Description                                                         |
| -------------------------------------------------------------------------------------------------------------------------- | ------- | ------- | ---------- | ---------- | ------------------------------------------------------------------------- |
| - [alignDataTypesAndValues](#variables_alignDataTypesAndValues )                                                           | No      | boolean | No         | -          | Whether to align the data types and values in DECLARE statements          |
| - [addSpaceBetweenDataTypeAndPrecision](#variables_addSpaceBetweenDataTypeAndPrecision )                                   | No      | boolean | No         | -          | Whether a space is added between a data type and its precision            |
| - [placeAssignedValueOnNewLineIfLongerThanMaxLineLength](#variables_placeAssignedValueOnNewLineIfLongerThanMaxLineLength ) | No      | boolean | No         | -          | Whether the assigned value is placed on a new line in long SET statements |
| - [placeEqualsSignOnNewLine](#variables_placeEqualsSignOnNewLine )                                                         | No      | boolean | No         | -          | Whether the = sign is placed on a new line                                |

### <a name="variables_alignDataTypesAndValues"></a>9.1. Property `Root > variables > alignDataTypesAndValues`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether to align the data types and values in DECLARE statements

### <a name="variables_addSpaceBetweenDataTypeAndPrecision"></a>9.2. Property `Root > variables > addSpaceBetweenDataTypeAndPrecision`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether a space is added between a data type and its precision

### <a name="variables_placeAssignedValueOnNewLineIfLongerThanMaxLineLength"></a>9.3. Property `Root > variables > placeAssignedValueOnNewLineIfLongerThanMaxLineLength`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether the assigned value is placed on a new line in long SET statements

### <a name="variables_placeEqualsSignOnNewLine"></a>9.4. Property `Root > variables > placeEqualsSignOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether the = sign is placed on a new line

## <a name="joinStatements"></a>10. Property `Root > joinStatements`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for join statements

| Property                        | Pattern | Type   | Deprecated | Definition | Title/Description           |
| ------------------------------- | ------- | ------ | ---------- | ---------- | --------------------------- |
| - [join](#joinStatements_join ) | No      | object | No         | -          | Formatting options for JOIN |
| - [on](#joinStatements_on )     | No      | object | No         | -          | Formatting options for ON   |

### <a name="joinStatements_join"></a>10.1. Property `Root > joinStatements > join`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for JOIN

| Property                                                                                       | Pattern | Type             | Deprecated | Definition | Title/Description                                     |
| ---------------------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ----------------------------------------------------- |
| - [placeOnNewLine](#joinStatements_join_placeOnNewLine )                                       | No      | boolean          | No         | -          | Whether the JOIN keyword is placed on a new line      |
| - [keywordAlignment](#joinStatements_join_keywordAlignment )                                   | No      | enum (of string) | No         | -          | How the JOIN keyword is aligned                       |
| - [insertEmptyLineBetweenJoinClauses](#joinStatements_join_insertEmptyLineBetweenJoinClauses ) | No      | boolean          | No         | -          | Whether empty lines are inserted between JOIN clauses |
| - [placeJoinTableOnNewLine](#joinStatements_join_placeJoinTableOnNewLine )                     | No      | boolean          | No         | -          | Whether the join table is placed on a new line        |
| - [indentJoinTable](#joinStatements_join_indentJoinTable )                                     | No      | boolean          | No         | -          | Whether the join table is indented                    |

#### <a name="joinStatements_join_placeOnNewLine"></a>10.1.1. Property `Root > joinStatements > join > placeOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether the JOIN keyword is placed on a new line

#### <a name="joinStatements_join_keywordAlignment"></a>10.1.2. Property `Root > joinStatements > join > keywordAlignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"toFrom"`         |

**Description:** How the JOIN keyword is aligned

Must be one of:
* "toFrom"
* "rightAlignedToFrom"
* "toTable"
* "indented"

#### <a name="joinStatements_join_insertEmptyLineBetweenJoinClauses"></a>10.1.3. Property `Root > joinStatements > join > insertEmptyLineBetweenJoinClauses`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether empty lines are inserted between JOIN clauses

#### <a name="joinStatements_join_placeJoinTableOnNewLine"></a>10.1.4. Property `Root > joinStatements > join > placeJoinTableOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether the join table is placed on a new line

#### <a name="joinStatements_join_indentJoinTable"></a>10.1.5. Property `Root > joinStatements > join > indentJoinTable`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether the join table is indented

### <a name="joinStatements_on"></a>10.2. Property `Root > joinStatements > on`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for ON

| Property                                                                 | Pattern | Type             | Deprecated | Definition | Title/Description                                |
| ------------------------------------------------------------------------ | ------- | ---------------- | ---------- | ---------- | ------------------------------------------------ |
| - [placeOnNewLine](#joinStatements_on_placeOnNewLine )                   | No      | boolean          | No         | -          | Whether the ON keyword is placed on a new line   |
| - [keywordAlignment](#joinStatements_on_keywordAlignment )               | No      | enum (of string) | No         | -          | How the ON keyword is aligned                    |
| - [placeConditionOnNewLine](#joinStatements_on_placeConditionOnNewLine ) | No      | boolean          | No         | -          | Whether a join condition is placed on a new line |
| - [conditionAlignment](#joinStatements_on_conditionAlignment )           | No      | enum (of string) | No         | -          | How join conditions are aligned                  |

#### <a name="joinStatements_on_placeOnNewLine"></a>10.2.1. Property `Root > joinStatements > on > placeOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether the ON keyword is placed on a new line

#### <a name="joinStatements_on_keywordAlignment"></a>10.2.2. Property `Root > joinStatements > on > keywordAlignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"toJoin"`         |

**Description:** How the ON keyword is aligned

Must be one of:
* "toJoin"
* "rightAlignedToJoin"
* "rightAlignedToInner"
* "toTable"
* "indented"

#### <a name="joinStatements_on_placeConditionOnNewLine"></a>10.2.3. Property `Root > joinStatements > on > placeConditionOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether a join condition is placed on a new line

#### <a name="joinStatements_on_conditionAlignment"></a>10.2.4. Property `Root > joinStatements > on > conditionAlignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"toOnKeyword"`    |

**Description:** How join conditions are aligned

Must be one of:
* "toOnKeyword"
* "toInner"
* "toTable"
* "indented"

## <a name="insertStatements"></a>11. Property `Root > insertStatements`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for inserts

| Property                                | Pattern | Type   | Deprecated | Definition | Title/Description              |
| --------------------------------------- | ------- | ------ | ---------- | ---------- | ------------------------------ |
| - [columns](#insertStatements_columns ) | No      | object | No         | -          | Formatting options for columns |
| - [values](#insertStatements_values )   | No      | object | No         | -          | Formatting options for values  |

### <a name="insertStatements_columns"></a>11.1. Property `Root > insertStatements > columns`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for columns

| Property                                                                                          | Pattern | Type             | Deprecated | Definition | Title/Description                                     |
| ------------------------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ----------------------------------------------------- |
| - [parenthesisStyle](#insertStatements_columns_parenthesisStyle )                                 | No      | enum (of string) | No         | -          | The format to use for parenthesized insert statements |
| - [indentContents](#insertStatements_columns_indentContents )                                     | No      | boolean          | No         | -          | Whether to indent content                             |
| - [placeSubsequentColumnsOnNewLines](#insertStatements_columns_placeSubsequentColumnsOnNewLines ) | No      | enum (of string) | No         | -          | When to place subsequent columns on new lines         |

#### <a name="insertStatements_columns_parenthesisStyle"></a>11.1.1. Property `Root > insertStatements > columns > parenthesisStyle`

|              |                         |
| ------------ | ----------------------- |
| **Type**     | `enum (of string)`      |
| **Required** | No                      |
| **Default**  | `"expandedToStatement"` |

**Description:** The format to use for parenthesized insert statements

Must be one of:
* "compactSimple"
* "compactToStatement"
* "compactIndented"
* "compactRightAligned"
* "expandedSimple"
* "expandedSplit"
* "expandedToStatement"
* "expandedIndented"
* "expandedRightAligned"

#### <a name="insertStatements_columns_indentContents"></a>11.1.2. Property `Root > insertStatements > columns > indentContents`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether to indent content

#### <a name="insertStatements_columns_placeSubsequentColumnsOnNewLines"></a>11.1.3. Property `Root > insertStatements > columns > placeSubsequentColumnsOnNewLines`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"always"`         |

**Description:** When to place subsequent columns on new lines

Must be one of:
* "always"
* "never"
* "ifLongerThanMaxLineLength"

### <a name="insertStatements_values"></a>11.2. Property `Root > insertStatements > values`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for values

| Property                                                                                       | Pattern | Type             | Deprecated | Definition | Title/Description                                 |
| ---------------------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ------------------------------------------------- |
| - [parenthesisStyle](#insertStatements_values_parenthesisStyle )                               | No      | enum (of string) | No         | -          | The format to use for values in INSERT statements |
| - [indentContents](#insertStatements_values_indentContents )                                   | No      | boolean          | No         | -          | Whether to indent content                         |
| - [placeSubsequentValuesOnNewLines](#insertStatements_values_placeSubsequentValuesOnNewLines ) | No      | enum (of string) | No         | -          | When to place subsequent values on new lines      |

#### <a name="insertStatements_values_parenthesisStyle"></a>11.2.1. Property `Root > insertStatements > values > parenthesisStyle`

|              |                        |
| ------------ | ---------------------- |
| **Type**     | `enum (of string)`     |
| **Required** | No                     |
| **Default**  | `"compactToStatement"` |

**Description:** The format to use for values in INSERT statements

Must be one of:
* "compactSimple"
* "compactToStatement"
* "compactIndented"
* "compactRightAligned"
* "expandedSimple"
* "expandedSplit"
* "expandedToStatement"
* "expandedIndented"
* "expandedRightAligned"

#### <a name="insertStatements_values_indentContents"></a>11.2.2. Property `Root > insertStatements > values > indentContents`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to indent content

#### <a name="insertStatements_values_placeSubsequentValuesOnNewLines"></a>11.2.3. Property `Root > insertStatements > values > placeSubsequentValuesOnNewLines`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"never"`          |

**Description:** When to place subsequent values on new lines

Must be one of:
* "always"
* "never"
* "ifLongerThanMaxLineLength"

## <a name="functionCalls"></a>12. Property `Root > functionCalls`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for function calls

| Property                                                                             | Pattern | Type             | Deprecated | Definition | Title/Description                              |
| ------------------------------------------------------------------------------------ | ------- | ---------------- | ---------- | ---------- | ---------------------------------------------- |
| - [placeArgumentsOnNewLines](#functionCalls_placeArgumentsOnNewLines )               | No      | enum (of string) | No         | -          | When to place arguments on new lines           |
| - [addSpacesAroundParentheses](#functionCalls_addSpacesAroundParentheses )           | No      | boolean          | No         | -          | Whether to add spaces around parentheses       |
| - [addSpacesAroundArgumentList](#functionCalls_addSpacesAroundArgumentList )         | No      | boolean          | No         | -          | Whether to add spaces around argument list     |
| - [addSpaceBetweenEmptyParentheses](#functionCalls_addSpaceBetweenEmptyParentheses ) | No      | boolean          | No         | -          | Whether to add space between empty parentheses |

### <a name="functionCalls_placeArgumentsOnNewLines"></a>12.1. Property `Root > functionCalls > placeArgumentsOnNewLines`

|              |                               |
| ------------ | ----------------------------- |
| **Type**     | `enum (of string)`            |
| **Required** | No                            |
| **Default**  | `"ifLongerThanMaxLineLength"` |

**Description:** When to place arguments on new lines

Must be one of:
* "always"
* "never"
* "ifLongerThanMaxLineLength"

### <a name="functionCalls_addSpacesAroundParentheses"></a>12.2. Property `Root > functionCalls > addSpacesAroundParentheses`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to add spaces around parentheses

### <a name="functionCalls_addSpacesAroundArgumentList"></a>12.3. Property `Root > functionCalls > addSpacesAroundArgumentList`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to add spaces around argument list

### <a name="functionCalls_addSpaceBetweenEmptyParentheses"></a>12.4. Property `Root > functionCalls > addSpaceBetweenEmptyParentheses`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to add space between empty parentheses

## <a name="caseExpressions"></a>13. Property `Root > caseExpressions`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for CASE

| Property                                                                                     | Pattern | Type             | Deprecated | Definition | Title/Description                                                                  |
| -------------------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ---------------------------------------------------------------------------------- |
| - [placeExpressionOnNewLine](#caseExpressions_placeExpressionOnNewLine )                     | No      | boolean          | No         | -          | Whether to place expression on new line                                            |
| - [placeFirstWhenOnNewLine](#caseExpressions_placeFirstWhenOnNewLine )                       | No      | enum (of string) | No         | -          | When to place the first WHEN keyword on a new line                                 |
| - [whenAlignment](#caseExpressions_whenAlignment )                                           | No      | enum (of string) | No         | -          | How the WHEN keywords are aligned                                                  |
| - [placeThenOnNewLine](#caseExpressions_placeThenOnNewLine )                                 | No      | boolean          | No         | -          | Whether the THEN keyword is placed on a new line                                   |
| - [thenAlignment](#caseExpressions_thenAlignment )                                           | No      | enum (of string) | No         | -          | How the THEN keywords are aligned                                                  |
| - [placeElseOnNewLine](#caseExpressions_placeElseOnNewLine )                                 | No      | boolean          | No         | -          | Whether the ELSE keyword is placed on new line                                     |
| - [alignElseToWhen](#caseExpressions_alignElseToWhen )                                       | No      | boolean          | No         | -          | Whether to align the ELSE keyword to the WHEN keyword                              |
| - [placeEndOnNewLine](#caseExpressions_placeEndOnNewLine )                                   | No      | boolean          | No         | -          | Whether to place the END keyword on new line                                       |
| - [endAlignment](#caseExpressions_endAlignment )                                             | No      | enum (of string) | No         | -          | How the END keyword is aligned                                                     |
| - [collapseShortCaseExpressions](#caseExpressions_collapseShortCaseExpressions )             | No      | boolean          | No         | -          | Collapse short CASE expressions onto a single line                                 |
| - [collapseCaseExpressionsShorterThan](#caseExpressions_collapseCaseExpressionsShorterThan ) | No      | integer          | No         | -          | CASE expressions shorter than this will be collapsed onto a single line if enabled |

### <a name="caseExpressions_placeExpressionOnNewLine"></a>13.1. Property `Root > caseExpressions > placeExpressionOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether to place expression on new line

### <a name="caseExpressions_placeFirstWhenOnNewLine"></a>13.2. Property `Root > caseExpressions > placeFirstWhenOnNewLine`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"always"`         |

**Description:** When to place the first WHEN keyword on a new line

Must be one of:
* "always"
* "never"
* "ifInputExpression"

### <a name="caseExpressions_whenAlignment"></a>13.3. Property `Root > caseExpressions > whenAlignment`

|              |                      |
| ------------ | -------------------- |
| **Type**     | `enum (of string)`   |
| **Required** | No                   |
| **Default**  | `"indentedFromCase"` |

**Description:** How the WHEN keywords are aligned

Must be one of:
* "indentedFromCase"
* "toCase"
* "toFirstItem"

### <a name="caseExpressions_placeThenOnNewLine"></a>13.4. Property `Root > caseExpressions > placeThenOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether the THEN keyword is placed on a new line

### <a name="caseExpressions_thenAlignment"></a>13.5. Property `Root > caseExpressions > thenAlignment`

|              |                      |
| ------------ | -------------------- |
| **Type**     | `enum (of string)`   |
| **Required** | No                   |
| **Default**  | `"indentedFromWhen"` |

**Description:** How the THEN keywords are aligned

Must be one of:
* "indentedFromWhen"
* "toWhen"
* "toWhenExpression"

### <a name="caseExpressions_placeElseOnNewLine"></a>13.6. Property `Root > caseExpressions > placeElseOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether the ELSE keyword is placed on new line

### <a name="caseExpressions_alignElseToWhen"></a>13.7. Property `Root > caseExpressions > alignElseToWhen`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether to align the ELSE keyword to the WHEN keyword

### <a name="caseExpressions_placeEndOnNewLine"></a>13.8. Property `Root > caseExpressions > placeEndOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether to place the END keyword on new line

### <a name="caseExpressions_endAlignment"></a>13.9. Property `Root > caseExpressions > endAlignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"toCase"`         |

**Description:** How the END keyword is aligned

Must be one of:
* "toCase"
* "toWhen"
* "rightAlignedToWhen"

### <a name="caseExpressions_collapseShortCaseExpressions"></a>13.10. Property `Root > caseExpressions > collapseShortCaseExpressions`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Collapse short CASE expressions onto a single line

### <a name="caseExpressions_collapseCaseExpressionsShorterThan"></a>13.11. Property `Root > caseExpressions > collapseCaseExpressionsShorterThan`

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |
| **Default**  | `80`      |

**Description:** CASE expressions shorter than this will be collapsed onto a single line if enabled

**Examples:** 

```json
80
```

```json
120
```

```json
180
```

## <a name="operators"></a>14. Property `Root > operators`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for operators

| Property                               | Pattern | Type   | Deprecated | Definition | Title/Description                  |
| -------------------------------------- | ------- | ------ | ---------- | ---------- | ---------------------------------- |
| - [comparison](#operators_comparison ) | No      | object | No         | -          | Formatting options for comparisons |
| - [arithmetic](#operators_arithmetic ) | No      | object | No         | -          | Formatting options for arithmetic  |
| - [andOr](#operators_andOr )           | No      | object | No         | -          | Formatting options for AND / OR    |
| - [between](#operators_between )       | No      | object | No         | -          | Formatting options for BETWEEN     |
| - [in](#operators_in )                 | No      | object | No         | -          | Formatting options for IN          |

### <a name="operators_comparison"></a>14.1. Property `Root > operators > comparison`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for comparisons

| Property                                                    | Pattern | Type    | Deprecated | Definition | Title/Description                                 |
| ----------------------------------------------------------- | ------- | ------- | ---------- | ---------- | ------------------------------------------------- |
| - [align](#operators_comparison_align )                     | No      | boolean | No         | -          | Whether to align comparison operators             |
| - [addSpacesAround](#operators_comparison_addSpacesAround ) | No      | boolean | No         | -          | Whether to add spaces around comparison operators |

#### <a name="operators_comparison_align"></a>14.1.1. Property `Root > operators > comparison > align`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to align comparison operators

#### <a name="operators_comparison_addSpacesAround"></a>14.1.2. Property `Root > operators > comparison > addSpacesAround`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether to add spaces around comparison operators

### <a name="operators_arithmetic"></a>14.2. Property `Root > operators > arithmetic`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for arithmetic

| Property                                                    | Pattern | Type    | Deprecated | Definition | Title/Description                                 |
| ----------------------------------------------------------- | ------- | ------- | ---------- | ---------- | ------------------------------------------------- |
| - [addSpacesAround](#operators_arithmetic_addSpacesAround ) | No      | boolean | No         | -          | Whether to add spaces around arithmetic operators |

#### <a name="operators_arithmetic_addSpacesAround"></a>14.2.1. Property `Root > operators > arithmetic > addSpacesAround`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether to add spaces around arithmetic operators

### <a name="operators_andOr"></a>14.3. Property `Root > operators > andOr`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for AND / OR

| Property                                                                       | Pattern | Type             | Deprecated | Definition | Title/Description                                  |
| ------------------------------------------------------------------------------ | ------- | ---------------- | ---------- | ---------- | -------------------------------------------------- |
| - [placeOnNewLine](#operators_andOr_placeOnNewLine )                           | No      | enum (of string) | No         | -          | When to place AND / OR operators on a new line     |
| - [alignment](#operators_andOr_alignment )                                     | No      | enum (of string) | No         | -          | How to align AND / OR operators                    |
| - [placeKeywordBeforeCondition](#operators_andOr_placeKeywordBeforeCondition ) | No      | boolean          | No         | -          | Whether to place AND / OR keyword before condition |

#### <a name="operators_andOr_placeOnNewLine"></a>14.3.1. Property `Root > operators > andOr > placeOnNewLine`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"always"`         |

**Description:** When to place AND / OR operators on a new line

Must be one of:
* "always"
* "never"
* "ifLongerThanMaxLineLength"

#### <a name="operators_andOr_alignment"></a>14.3.2. Property `Root > operators > andOr > alignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"leftAligned"`    |

**Description:** How to align AND / OR operators

Must be one of:
* "leftAligned"
* "rightAligned"
* "beforeFirstListItem"
* "toFirstListItem"
* "indented"

#### <a name="operators_andOr_placeKeywordBeforeCondition"></a>14.3.3. Property `Root > operators > andOr > placeKeywordBeforeCondition`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether to place AND / OR keyword before condition

### <a name="operators_between"></a>14.4. Property `Root > operators > between`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for BETWEEN

| Property                                                                   | Pattern | Type             | Deprecated | Definition | Title/Description                                                            |
| -------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ---------------------------------------------------------------------------- |
| - [placeOnNewLine](#operators_between_placeOnNewLine )                     | No      | boolean          | No         | -          | Whether to place BETWEEN operator on a new line                              |
| - [placeAndKeywordOnNewLine](#operators_between_placeAndKeywordOnNewLine ) | No      | boolean          | No         | -          | Whether to place AND keyword on a new line                                   |
| - [andAlignment](#operators_between_andAlignment )                         | No      | enum (of string) | No         | -          | How to align the AND keyword if placing AND keyword on a new line is enabled |

#### <a name="operators_between_placeOnNewLine"></a>14.4.1. Property `Root > operators > between > placeOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `true`    |

**Description:** Whether to place BETWEEN operator on a new line

#### <a name="operators_between_placeAndKeywordOnNewLine"></a>14.4.2. Property `Root > operators > between > placeAndKeywordOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to place AND keyword on a new line

#### <a name="operators_between_andAlignment"></a>14.4.3. Property `Root > operators > between > andAlignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"toBetween"`      |

**Description:** How to align the AND keyword if placing AND keyword on a new line is enabled

Must be one of:
* "toBetween"
* "rightAlignedToBetween"
* "toBeginningOfExpression"

### <a name="operators_in"></a>14.5. Property `Root > operators > in`

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** Formatting options for IN

| Property                                                                              | Pattern | Type             | Deprecated | Definition | Title/Description                                |
| ------------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ------------------------------------------------ |
| - [placeOpeningParenthesisOnNewLine](#operators_in_placeOpeningParenthesisOnNewLine ) | No      | boolean          | No         | -          | Whether to place opening parenthesis on new line |
| - [alignment](#operators_in_alignment )                                               | No      | enum (of string) | No         | -          | How to align the IN keyword                      |
| - [placeFirstValueOnNewLine](#operators_in_placeFirstValueOnNewLine )                 | No      | enum (of string) | No         | -          | When to place the first value on a new line      |
| - [placeSubsequentValuesOnNewLines](#operators_in_placeSubsequentValuesOnNewLines )   | No      | enum (of string) | No         | -          | When to place subsequent values on new lines     |
| - [addSpaceAroundInContents](#operators_in_addSpaceAroundInContents )                 | No      | boolean          | No         | -          | Whether to add a space around IN contents        |

#### <a name="operators_in_placeOpeningParenthesisOnNewLine"></a>14.5.1. Property `Root > operators > in > placeOpeningParenthesisOnNewLine`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to place opening parenthesis on new line

#### <a name="operators_in_alignment"></a>14.5.2. Property `Root > operators > in > alignment`

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | No                 |
| **Default**  | `"leftAligned"`    |

**Description:** How to align the IN keyword

Must be one of:
* "leftAligned"
* "rightAligned"
* "indented"

#### <a name="operators_in_placeFirstValueOnNewLine"></a>14.5.3. Property `Root > operators > in > placeFirstValueOnNewLine`

|              |                               |
| ------------ | ----------------------------- |
| **Type**     | `enum (of string)`            |
| **Required** | No                            |
| **Default**  | `"ifLongerThanMaxLineLength"` |

**Description:** When to place the first value on a new line

Must be one of:
* "always"
* "never"
* "ifLongerThanMaxLineLength"
* "ifSubsequentValues"

#### <a name="operators_in_placeSubsequentValuesOnNewLines"></a>14.5.4. Property `Root > operators > in > placeSubsequentValuesOnNewLines`

|              |                               |
| ------------ | ----------------------------- |
| **Type**     | `enum (of string)`            |
| **Required** | No                            |
| **Default**  | `"ifLongerThanMaxLineLength"` |

**Description:** When to place subsequent values on new lines

Must be one of:
* "always"
* "never"
* "ifLongerThanMaxLineLength"

#### <a name="operators_in_addSpaceAroundInContents"></a>14.5.5. Property `Root > operators > in > addSpaceAroundInContents`

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |
| **Default**  | `false`   |

**Description:** Whether to add a space around IN contents

----------------------------------------------------------------------------------------------------------------------------
Generated using [json-schema-for-humans](https://github.com/coveooss/json-schema-for-humans) on 2023-10-17 at 17:36:36 +0200
