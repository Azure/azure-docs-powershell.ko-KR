---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327935"
---
# <span data-ttu-id="8984d-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="8984d-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="8984d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8984d-102">SYNOPSIS</span></span>
<span data-ttu-id="8984d-103">데이터베이스의 열에 대한 민감도 권장 사항(기본적으로 모든 열에서 권장 사항 사용)을 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="8984d-104">구문</span><span class="sxs-lookup"><span data-stu-id="8984d-104">SYNTAX</span></span>

### <span data-ttu-id="8984d-105">InputObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8984d-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8984d-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8984d-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8984d-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8984d-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8984d-108">설명</span><span class="sxs-lookup"><span data-stu-id="8984d-108">DESCRIPTION</span></span>
<span data-ttu-id="8984d-109">Enable-AzSqlDatabaseSensitivityRecommendation cmdlet을 사용하면 데이터베이스의 열에 대한 민감도 권장 사항을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="8984d-110">예제</span><span class="sxs-lookup"><span data-stu-id="8984d-110">EXAMPLES</span></span>

### <span data-ttu-id="8984d-111">예제 1: Azure SQL Database의 주어진 열에서 민감도 권장 사항을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="8984d-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="8984d-112">예제 2: Piping을 사용하여 Azure SQL 열에 대한 민감도 권장 사항을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="8984d-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="8984d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8984d-113">PARAMETERS</span></span>

### <span data-ttu-id="8984d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8984d-114">-AsJob</span></span>
<span data-ttu-id="8984d-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8984d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8984d-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="8984d-116">-ColumnName</span></span>
<span data-ttu-id="8984d-117">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-117">Name of column.</span></span>

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

### <span data-ttu-id="8984d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8984d-118">-DatabaseName</span></span>
<span data-ttu-id="8984d-119">Azure SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="8984d-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8984d-120">-DatabaseObject</span></span>
<span data-ttu-id="8984d-121">SQL 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-121">The SQL database object.</span></span>

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

### <span data-ttu-id="8984d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8984d-122">-DefaultProfile</span></span>
<span data-ttu-id="8984d-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8984d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8984d-124">-InputObject</span></span>
<span data-ttu-id="8984d-125">데이터베이스 민감도 SQL 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-125">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="8984d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8984d-126">-PassThru</span></span>
<span data-ttu-id="8984d-127">cmdlet 실행의 끝에서 민감도 분류 모델을 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="8984d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8984d-128">-ResourceGroupName</span></span>
<span data-ttu-id="8984d-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="8984d-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8984d-130">-SchemaName</span></span>
<span data-ttu-id="8984d-131">schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-131">Name of schema.</span></span>

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

### <span data-ttu-id="8984d-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8984d-132">-ServerName</span></span>
<span data-ttu-id="8984d-133">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-133">SQL server name.</span></span>

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

### <span data-ttu-id="8984d-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="8984d-134">-TableName</span></span>
<span data-ttu-id="8984d-135">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-135">Name of table.</span></span>

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

### <span data-ttu-id="8984d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8984d-136">-Confirm</span></span>
<span data-ttu-id="8984d-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8984d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8984d-138">-WhatIf</span></span>
<span data-ttu-id="8984d-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8984d-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8984d-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8984d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8984d-141">CommonParameters</span></span>
<span data-ttu-id="8984d-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8984d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8984d-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8984d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8984d-144">입력</span><span class="sxs-lookup"><span data-stu-id="8984d-144">INPUTS</span></span>

### <span data-ttu-id="8984d-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="8984d-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="8984d-146">출력</span><span class="sxs-lookup"><span data-stu-id="8984d-146">OUTPUTS</span></span>

### <span data-ttu-id="8984d-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8984d-147">System.Boolean</span></span>

## <span data-ttu-id="8984d-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8984d-148">NOTES</span></span>

## <span data-ttu-id="8984d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8984d-149">RELATED LINKS</span></span>

[<span data-ttu-id="8984d-150">Azure SQL 데이터베이스 데이터 검색 및 분류에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="8984d-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)