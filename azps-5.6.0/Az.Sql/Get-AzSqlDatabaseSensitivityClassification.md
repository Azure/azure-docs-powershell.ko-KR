---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 32459ad76bb118e97ba29e1730c6006a69b4a3b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014736"
---
# <span data-ttu-id="308a1-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="308a1-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="308a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="308a1-102">SYNOPSIS</span></span>
<span data-ttu-id="308a1-103">데이터베이스의 열의 현재 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="308a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="308a1-104">SYNTAX</span></span>

### <span data-ttu-id="308a1-105">DatabaseObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="308a1-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="308a1-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="308a1-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="308a1-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="308a1-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="308a1-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="308a1-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="308a1-109">설명</span><span class="sxs-lookup"><span data-stu-id="308a1-109">DESCRIPTION</span></span>
<span data-ttu-id="308a1-110">Get-AzSqlDatabaseSensitivityClassification cmdlet은 Azure SQL 열의 현재 정보 형식 및 민감도 레이블을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="308a1-111">예제</span><span class="sxs-lookup"><span data-stu-id="308a1-111">EXAMPLES</span></span>

### <span data-ttu-id="308a1-112">예제 1: Azure 데이터베이스 데이터베이스의 현재 정보 유형 및 민감도 레이블을 SQL.</span><span class="sxs-lookup"><span data-stu-id="308a1-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="308a1-113">예제 2: Piping을 사용하여 Azure SQL 데이터베이스의 현재 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="308a1-114">예제 3: Azure 데이터베이스의 특정 열의 현재 정보 유형 및 민감도 레이블을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="308a1-115">예제 4: Piping을 사용하여 Azure SQL 열의 현재 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="308a1-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="308a1-116">PARAMETERS</span></span>

### <span data-ttu-id="308a1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="308a1-117">-AsJob</span></span>
<span data-ttu-id="308a1-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="308a1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="308a1-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="308a1-119">-ColumnName</span></span>
<span data-ttu-id="308a1-120">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-120">Name of column.</span></span>

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

### <span data-ttu-id="308a1-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="308a1-121">-DatabaseName</span></span>
<span data-ttu-id="308a1-122">Azure 데이터베이스의 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="308a1-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="308a1-123">-DatabaseObject</span></span>
<span data-ttu-id="308a1-124">데이터베이스 SQL 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-124">The SQL database object.</span></span>

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

### <span data-ttu-id="308a1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308a1-125">-DefaultProfile</span></span>
<span data-ttu-id="308a1-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="308a1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="308a1-127">-ResourceGroupName</span></span>
<span data-ttu-id="308a1-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="308a1-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="308a1-129">-SchemaName</span></span>
<span data-ttu-id="308a1-130">Schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-130">Name of schema.</span></span>

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

### <span data-ttu-id="308a1-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="308a1-131">-ServerName</span></span>
<span data-ttu-id="308a1-132">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-132">SQL server name.</span></span>

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

### <span data-ttu-id="308a1-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="308a1-133">-TableName</span></span>
<span data-ttu-id="308a1-134">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-134">Name of table.</span></span>

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

### <span data-ttu-id="308a1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308a1-135">CommonParameters</span></span>
<span data-ttu-id="308a1-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="308a1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308a1-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="308a1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308a1-138">입력</span><span class="sxs-lookup"><span data-stu-id="308a1-138">INPUTS</span></span>

### <span data-ttu-id="308a1-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="308a1-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="308a1-140">출력</span><span class="sxs-lookup"><span data-stu-id="308a1-140">OUTPUTS</span></span>

### <span data-ttu-id="308a1-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="308a1-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="308a1-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="308a1-142">NOTES</span></span>

## <span data-ttu-id="308a1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="308a1-143">RELATED LINKS</span></span>

[<span data-ttu-id="308a1-144">Azure SQL 데이터베이스 데이터 검색 및 분류에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="308a1-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
