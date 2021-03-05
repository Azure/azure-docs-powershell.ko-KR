---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 9a33504fb27d7c1cf623b03f6c4ea8fefb32c85f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999408"
---
# <span data-ttu-id="2b03a-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="2b03a-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="2b03a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b03a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b03a-103">Azure 관리되는 인스턴스 데이터베이스에서 열의 현재 정보 형식 및 민감도 레이블을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="2b03a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2b03a-104">SYNTAX</span></span>

### <span data-ttu-id="2b03a-105">DatabaseObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2b03a-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b03a-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b03a-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b03a-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b03a-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b03a-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b03a-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b03a-109">설명</span><span class="sxs-lookup"><span data-stu-id="2b03a-109">DESCRIPTION</span></span>
<span data-ttu-id="2b03a-110">Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet은 Azure SQL 관리되는 인스턴스 데이터베이스의 열의 현재 정보 유형 및 민감도 레이블을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="2b03a-111">예제</span><span class="sxs-lookup"><span data-stu-id="2b03a-111">EXAMPLES</span></span>

### <span data-ttu-id="2b03a-112">예제 1: Azure 관리되는 인스턴스 데이터베이스의 현재 정보 유형 및 민감도 레이블을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="2b03a-113">예제 2: Piping을 사용하여 Azure SQL 관리되는 인스턴스 데이터베이스의 현재 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="2b03a-114">예제 3: Azure 관리되는 인스턴스 데이터베이스의 특정 열의 현재 정보 유형 및 민감도 레이블을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="2b03a-115">예제 4: Piping을 사용하여 Azure SQL 특정 열의 현재 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

## <span data-ttu-id="2b03a-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2b03a-116">PARAMETERS</span></span>

### <span data-ttu-id="2b03a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b03a-117">-AsJob</span></span>
<span data-ttu-id="2b03a-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2b03a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b03a-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="2b03a-119">-ColumnName</span></span>
<span data-ttu-id="2b03a-120">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-120">Name of column.</span></span>

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

### <span data-ttu-id="2b03a-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2b03a-121">-DatabaseName</span></span>
<span data-ttu-id="2b03a-122">Azure SQL 관리되는 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="2b03a-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2b03a-123">-DatabaseObject</span></span>
<span data-ttu-id="2b03a-124">Azure SQL 관리되는 인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b03a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b03a-125">-DefaultProfile</span></span>
<span data-ttu-id="2b03a-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b03a-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2b03a-127">-InstanceName</span></span>
<span data-ttu-id="2b03a-128">Azure SQL 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="2b03a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b03a-129">-ResourceGroupName</span></span>
<span data-ttu-id="2b03a-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b03a-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="2b03a-131">-SchemaName</span></span>
<span data-ttu-id="2b03a-132">Schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-132">Name of schema.</span></span>

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

### <span data-ttu-id="2b03a-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="2b03a-133">-TableName</span></span>
<span data-ttu-id="2b03a-134">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-134">Name of table.</span></span>

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

### <span data-ttu-id="2b03a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b03a-135">CommonParameters</span></span>
<span data-ttu-id="2b03a-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b03a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b03a-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b03a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b03a-138">입력</span><span class="sxs-lookup"><span data-stu-id="2b03a-138">INPUTS</span></span>

### <span data-ttu-id="2b03a-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2b03a-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="2b03a-140">출력</span><span class="sxs-lookup"><span data-stu-id="2b03a-140">OUTPUTS</span></span>

### <span data-ttu-id="2b03a-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="2b03a-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="2b03a-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2b03a-142">NOTES</span></span>

## <span data-ttu-id="2b03a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b03a-143">RELATED LINKS</span></span>

[<span data-ttu-id="2b03a-144">Azure SQL 데이터베이스 데이터 검색 및 분류에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="2b03a-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
