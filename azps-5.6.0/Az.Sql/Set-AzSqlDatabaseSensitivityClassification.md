---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 88e08a15c864386d2e073f83f437d0db537f2ae7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003019"
---
# <span data-ttu-id="8db43-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="8db43-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="8db43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8db43-102">SYNOPSIS</span></span>
<span data-ttu-id="8db43-103">데이터베이스의 열의 정보 형식 및 민감도 레이블을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="8db43-104">구문</span><span class="sxs-lookup"><span data-stu-id="8db43-104">SYNTAX</span></span>

### <span data-ttu-id="8db43-105">ClassificationObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8db43-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8db43-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8db43-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8db43-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8db43-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db43-108">설명</span><span class="sxs-lookup"><span data-stu-id="8db43-108">DESCRIPTION</span></span>
<span data-ttu-id="8db43-109">Set-AzSqlDatabaseSensitivityClassification cmdlet은 데이터베이스의 열의 정보 형식 및 민감도 레이블을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="8db43-110">예제</span><span class="sxs-lookup"><span data-stu-id="8db43-110">EXAMPLES</span></span>

### <span data-ttu-id="8db43-111">예제 1: Azure SQL 열의 정보 유형 및 민감도 레이블을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="8db43-112">예제 2: Azure SQL 열의 권장 정보 형식 및 민감도 레이블을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="8db43-113">예제 3: 배관을 사용하여 Azure SQL 열의 정보 유형 및 민감도 레이블을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="8db43-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8db43-114">PARAMETERS</span></span>

### <span data-ttu-id="8db43-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8db43-115">-AsJob</span></span>
<span data-ttu-id="8db43-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8db43-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8db43-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="8db43-117">-ClassificationObject</span></span>
<span data-ttu-id="8db43-118">데이터베이스 민감도 분류를 SQL 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8db43-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="8db43-119">-ColumnName</span></span>
<span data-ttu-id="8db43-120">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-120">Name of column.</span></span>

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

### <span data-ttu-id="8db43-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8db43-121">-DatabaseName</span></span>
<span data-ttu-id="8db43-122">Azure 데이터베이스의 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db43-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8db43-123">-DatabaseObject</span></span>
<span data-ttu-id="8db43-124">데이터베이스 SQL 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8db43-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db43-125">-DefaultProfile</span></span>
<span data-ttu-id="8db43-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8db43-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="8db43-127">-InformationType</span></span>
<span data-ttu-id="8db43-128">열에 저장된 데이터의 정보 유형을 설명하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db43-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8db43-129">-PassThru</span></span>
<span data-ttu-id="8db43-130">cmdlet 실행의 끝에 민감도 분류 모델을 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="8db43-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8db43-131">-ResourceGroupName</span></span>
<span data-ttu-id="8db43-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db43-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8db43-133">-SchemaName</span></span>
<span data-ttu-id="8db43-134">Schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-134">Name of schema.</span></span>

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

### <span data-ttu-id="8db43-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="8db43-135">-SensitivityLabel</span></span>
<span data-ttu-id="8db43-136">열에 저장된 데이터의 민감도를 설명하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db43-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8db43-137">-ServerName</span></span>
<span data-ttu-id="8db43-138">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-138">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db43-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="8db43-139">-TableName</span></span>
<span data-ttu-id="8db43-140">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-140">Name of table.</span></span>

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

### <span data-ttu-id="8db43-141">-확인</span><span class="sxs-lookup"><span data-stu-id="8db43-141">-Confirm</span></span>
<span data-ttu-id="8db43-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db43-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db43-143">-WhatIf</span></span>
<span data-ttu-id="8db43-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8db43-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db43-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db43-146">CommonParameters</span></span>
<span data-ttu-id="8db43-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8db43-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db43-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8db43-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db43-149">입력</span><span class="sxs-lookup"><span data-stu-id="8db43-149">INPUTS</span></span>

### <span data-ttu-id="8db43-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="8db43-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="8db43-151">출력</span><span class="sxs-lookup"><span data-stu-id="8db43-151">OUTPUTS</span></span>

### <span data-ttu-id="8db43-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8db43-152">System.Boolean</span></span>

## <span data-ttu-id="8db43-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8db43-153">NOTES</span></span>

## <span data-ttu-id="8db43-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8db43-154">RELATED LINKS</span></span>

[<span data-ttu-id="8db43-155">Azure SQL 데이터베이스 데이터 검색 및 분류에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="8db43-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
