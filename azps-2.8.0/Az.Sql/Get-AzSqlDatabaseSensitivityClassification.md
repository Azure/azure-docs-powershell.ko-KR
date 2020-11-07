---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 50bd23f0c0be638683dae4acb5b43165a8c5b4f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873694"
---
# <span data-ttu-id="98b04-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="98b04-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="98b04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98b04-102">SYNOPSIS</span></span>
<span data-ttu-id="98b04-103">데이터베이스의 열에 대 한 현재 정보 유형 및 민감도 레이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="98b04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="98b04-104">SYNTAX</span></span>

### <span data-ttu-id="98b04-105">DatabaseObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="98b04-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b04-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="98b04-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b04-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="98b04-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98b04-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="98b04-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98b04-109">설명은</span><span class="sxs-lookup"><span data-stu-id="98b04-109">DESCRIPTION</span></span>
<span data-ttu-id="98b04-110">Get-AzSqlDatabaseSensitivityClassification cmdlet은 Azure SQL 데이터베이스의 열에 대 한 현재 정보 유형 및 민감도 레이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="98b04-111">예제의</span><span class="sxs-lookup"><span data-stu-id="98b04-111">EXAMPLES</span></span>

### <span data-ttu-id="98b04-112">예제 1: Azure SQL 데이터베이스의 현재 정보 유형 및 민감도 레이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="98b04-113">예제 2: 파이핑을 사용 하 여 Azure SQL 데이터베이스의 현재 정보 유형 및 민감도 레이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="98b04-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="98b04-114">예제 3: Azure SQL 데이터베이스의 특정 열에 대 한 현재 정보 유형 및 민감도 레이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="98b04-115">예제 4: 파이핑을 사용 하 여 Azure SQL 데이터베이스의 특정 열에 대 한 현재 정보 유형 및 민감도 레이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="98b04-116">변수</span><span class="sxs-lookup"><span data-stu-id="98b04-116">PARAMETERS</span></span>

### <span data-ttu-id="98b04-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98b04-117">-AsJob</span></span>
<span data-ttu-id="98b04-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="98b04-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b04-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="98b04-119">-ColumnName</span></span>
<span data-ttu-id="98b04-120">열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b04-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="98b04-121">-DatabaseName</span></span>
<span data-ttu-id="98b04-122">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b04-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="98b04-123">-DatabaseObject</span></span>
<span data-ttu-id="98b04-124">SQL 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98b04-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b04-125">-DefaultProfile</span></span>
<span data-ttu-id="98b04-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b04-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98b04-127">-ResourceGroupName</span></span>
<span data-ttu-id="98b04-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b04-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="98b04-129">-SchemaName</span></span>
<span data-ttu-id="98b04-130">스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-130">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b04-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="98b04-131">-ServerName</span></span>
<span data-ttu-id="98b04-132">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-132">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b04-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="98b04-133">-TableName</span></span>
<span data-ttu-id="98b04-134">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-134">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b04-135">CommonParameters</span></span>
<span data-ttu-id="98b04-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b04-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="98b04-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b04-138">입력</span><span class="sxs-lookup"><span data-stu-id="98b04-138">INPUTS</span></span>

### <span data-ttu-id="98b04-139">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="98b04-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="98b04-140">출력</span><span class="sxs-lookup"><span data-stu-id="98b04-140">OUTPUTS</span></span>

### <span data-ttu-id="98b04-141">DataClassification. SqlDatabaseSensitivityClassificationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="98b04-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="98b04-142">상속자</span><span class="sxs-lookup"><span data-stu-id="98b04-142">NOTES</span></span>

## <span data-ttu-id="98b04-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98b04-143">RELATED LINKS</span></span>

[<span data-ttu-id="98b04-144">Azure SQL 데이터베이스 데이터 검색 및 분류에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="98b04-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
