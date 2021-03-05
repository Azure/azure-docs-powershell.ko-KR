---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e7e13e62407018559835f4703d0b94edeced930b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986370"
---
# <span data-ttu-id="7e3dd-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="7e3dd-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="7e3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3dd-103">데이터베이스의 열에 대한 민감도 권장 사항(권장 사항은 기본적으로 모든 열에서 사용하도록 설정)을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="7e3dd-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e3dd-104">SYNTAX</span></span>

### <span data-ttu-id="7e3dd-105">InputObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e3dd-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e3dd-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e3dd-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e3dd-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e3dd-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e3dd-108">설명</span><span class="sxs-lookup"><span data-stu-id="7e3dd-108">DESCRIPTION</span></span>
<span data-ttu-id="7e3dd-109">Enable-AzSqlDatabaseSensitivityRecommendation cmdlet을 사용하면 데이터베이스의 열에 대한 민감도 권장 사항을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="7e3dd-110">예제</span><span class="sxs-lookup"><span data-stu-id="7e3dd-110">EXAMPLES</span></span>

### <span data-ttu-id="7e3dd-111">예제 1: Azure SQL 열에 대해 민감도 권장 사항을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="7e3dd-112">예제 2: Piping을 사용하여 Azure SQL 열에서 민감도 권장 사항을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="7e3dd-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7e3dd-113">PARAMETERS</span></span>

### <span data-ttu-id="7e3dd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e3dd-114">-AsJob</span></span>
<span data-ttu-id="7e3dd-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7e3dd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e3dd-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7e3dd-116">-ColumnName</span></span>
<span data-ttu-id="7e3dd-117">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-117">Name of column.</span></span>

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

### <span data-ttu-id="7e3dd-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e3dd-118">-DatabaseName</span></span>
<span data-ttu-id="7e3dd-119">Azure 데이터베이스의 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="7e3dd-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7e3dd-120">-DatabaseObject</span></span>
<span data-ttu-id="7e3dd-121">데이터베이스 SQL 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-121">The SQL database object.</span></span>

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

### <span data-ttu-id="7e3dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3dd-122">-DefaultProfile</span></span>
<span data-ttu-id="7e3dd-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e3dd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e3dd-124">-InputObject</span></span>
<span data-ttu-id="7e3dd-125">데이터베이스 민감도 분류를 SQL 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-125">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e3dd-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e3dd-126">-PassThru</span></span>
<span data-ttu-id="7e3dd-127">cmdlet 실행의 끝에 민감도 분류 모델을 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7e3dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e3dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e3dd-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e3dd-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7e3dd-130">-SchemaName</span></span>
<span data-ttu-id="7e3dd-131">Schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-131">Name of schema.</span></span>

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

### <span data-ttu-id="7e3dd-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e3dd-132">-ServerName</span></span>
<span data-ttu-id="7e3dd-133">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-133">SQL server name.</span></span>

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

### <span data-ttu-id="7e3dd-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="7e3dd-134">-TableName</span></span>
<span data-ttu-id="7e3dd-135">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-135">Name of table.</span></span>

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

### <span data-ttu-id="7e3dd-136">-확인</span><span class="sxs-lookup"><span data-stu-id="7e3dd-136">-Confirm</span></span>
<span data-ttu-id="7e3dd-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e3dd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e3dd-138">-WhatIf</span></span>
<span data-ttu-id="7e3dd-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e3dd-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e3dd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3dd-141">CommonParameters</span></span>
<span data-ttu-id="7e3dd-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3dd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3dd-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e3dd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3dd-144">입력</span><span class="sxs-lookup"><span data-stu-id="7e3dd-144">INPUTS</span></span>

### <span data-ttu-id="7e3dd-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7e3dd-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="7e3dd-146">출력</span><span class="sxs-lookup"><span data-stu-id="7e3dd-146">OUTPUTS</span></span>

### <span data-ttu-id="7e3dd-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7e3dd-147">System.Boolean</span></span>

## <span data-ttu-id="7e3dd-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e3dd-148">NOTES</span></span>

## <span data-ttu-id="7e3dd-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e3dd-149">RELATED LINKS</span></span>

[<span data-ttu-id="7e3dd-150">Azure SQL 데이터베이스 데이터 검색 및 분류에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="7e3dd-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)