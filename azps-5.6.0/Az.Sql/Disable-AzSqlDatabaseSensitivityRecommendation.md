---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 2f7d9421ada70946f18322828c138eca186df5c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011515"
---
# <span data-ttu-id="48681-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="48681-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="48681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48681-102">SYNOPSIS</span></span>
<span data-ttu-id="48681-103">데이터베이스의 열에 대한 민감도 권장 사항을 사용하지 않도록 설정(해제)합니다.</span><span class="sxs-lookup"><span data-stu-id="48681-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="48681-104">구문</span><span class="sxs-lookup"><span data-stu-id="48681-104">SYNTAX</span></span>

### <span data-ttu-id="48681-105">InputObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="48681-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48681-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="48681-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48681-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="48681-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48681-108">설명</span><span class="sxs-lookup"><span data-stu-id="48681-108">DESCRIPTION</span></span>
<span data-ttu-id="48681-109">Disable-AzSqlDatabaseSensitivityRecommendation cmdlet은 데이터베이스의 열에 대한 민감도 권장 사항을 사용하지 않도록 설정(해제)합니다.</span><span class="sxs-lookup"><span data-stu-id="48681-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="48681-110">예제</span><span class="sxs-lookup"><span data-stu-id="48681-110">EXAMPLES</span></span>

### <span data-ttu-id="48681-111">예제 1: Azure SQL 열에서 민감도 권장 사항을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="48681-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="48681-112">예제 2: Piping을 사용하여 Azure SQL 권장 사항이 있는 열에 대한 민감도 권장 사항을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="48681-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="48681-113">예제 3: Piping을 사용하여 Azure SQL 열에 대한 민감도 권장 사항을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="48681-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="48681-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="48681-114">PARAMETERS</span></span>

### <span data-ttu-id="48681-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48681-115">-AsJob</span></span>
<span data-ttu-id="48681-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="48681-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48681-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="48681-117">-ColumnName</span></span>
<span data-ttu-id="48681-118">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48681-118">Name of column.</span></span>

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

### <span data-ttu-id="48681-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="48681-119">-DatabaseName</span></span>
<span data-ttu-id="48681-120">Azure 데이터베이스의 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="48681-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="48681-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="48681-121">-DatabaseObject</span></span>
<span data-ttu-id="48681-122">데이터베이스 SQL 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="48681-122">The SQL database object.</span></span>

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

### <span data-ttu-id="48681-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48681-123">-DefaultProfile</span></span>
<span data-ttu-id="48681-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48681-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48681-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48681-125">-InputObject</span></span>
<span data-ttu-id="48681-126">데이터베이스 민감도 분류를 SQL 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="48681-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="48681-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48681-127">-PassThru</span></span>
<span data-ttu-id="48681-128">cmdlet 실행의 끝에 민감도 분류 모델을 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48681-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="48681-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48681-129">-ResourceGroupName</span></span>
<span data-ttu-id="48681-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48681-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="48681-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="48681-131">-SchemaName</span></span>
<span data-ttu-id="48681-132">Schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48681-132">Name of schema.</span></span>

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

### <span data-ttu-id="48681-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="48681-133">-ServerName</span></span>
<span data-ttu-id="48681-134">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48681-134">SQL server name.</span></span>

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

### <span data-ttu-id="48681-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="48681-135">-TableName</span></span>
<span data-ttu-id="48681-136">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48681-136">Name of table.</span></span>

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

### <span data-ttu-id="48681-137">-확인</span><span class="sxs-lookup"><span data-stu-id="48681-137">-Confirm</span></span>
<span data-ttu-id="48681-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="48681-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48681-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48681-139">-WhatIf</span></span>
<span data-ttu-id="48681-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="48681-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48681-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48681-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48681-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48681-142">CommonParameters</span></span>
<span data-ttu-id="48681-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48681-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48681-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48681-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48681-145">입력</span><span class="sxs-lookup"><span data-stu-id="48681-145">INPUTS</span></span>

### <span data-ttu-id="48681-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="48681-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="48681-147">출력</span><span class="sxs-lookup"><span data-stu-id="48681-147">OUTPUTS</span></span>

### <span data-ttu-id="48681-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48681-148">System.Boolean</span></span>

## <span data-ttu-id="48681-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48681-149">NOTES</span></span>

## <span data-ttu-id="48681-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48681-150">RELATED LINKS</span></span>

[<span data-ttu-id="48681-151">Azure SQL 데이터베이스 데이터 검색 및 분류에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="48681-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)