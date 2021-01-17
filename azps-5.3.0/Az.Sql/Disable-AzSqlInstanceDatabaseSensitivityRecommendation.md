---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375320"
---
# <span data-ttu-id="7fe63-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="7fe63-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="7fe63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fe63-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe63-103">Azure 관리되는 인스턴스 데이터베이스의 열에 대한 민감도 권장 사항을 SQL(해제)</span><span class="sxs-lookup"><span data-stu-id="7fe63-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="7fe63-104">구문</span><span class="sxs-lookup"><span data-stu-id="7fe63-104">SYNTAX</span></span>

### <span data-ttu-id="7fe63-105">InputObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7fe63-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fe63-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fe63-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fe63-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fe63-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fe63-108">설명</span><span class="sxs-lookup"><span data-stu-id="7fe63-108">DESCRIPTION</span></span>
<span data-ttu-id="7fe63-109">이 Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet은 Azure SQL 관리되는 인스턴스 데이터베이스의 열에 대한 민감도 권장 사항을 사용하지 않도록 설정(해제)합니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="7fe63-110">예제</span><span class="sxs-lookup"><span data-stu-id="7fe63-110">EXAMPLES</span></span>

### <span data-ttu-id="7fe63-111">예제 1: 관리되는 인스턴스 데이터베이스에서 Azure SQL 열에 대한 민감도 권장 사항을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="7fe63-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="7fe63-112">예제 2: Piping을 사용하여 Azure SQL 관리되는 인스턴스 데이터베이스에서 민감도 권장 사항이 있는 열에 대한 민감도 권장 사항을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="7fe63-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="7fe63-113">예제 3: Piping을 사용하여 Azure SQL 관리되는 인스턴스 데이터베이스의 주어진 열에 대한 민감도 권장 사항을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="7fe63-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="7fe63-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fe63-114">PARAMETERS</span></span>

### <span data-ttu-id="7fe63-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fe63-115">-AsJob</span></span>
<span data-ttu-id="7fe63-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7fe63-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fe63-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7fe63-117">-ColumnName</span></span>
<span data-ttu-id="7fe63-118">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-118">Name of column.</span></span>

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

### <span data-ttu-id="7fe63-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7fe63-119">-DatabaseName</span></span>
<span data-ttu-id="7fe63-120">Azure SQL 관리되는 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="7fe63-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7fe63-121">-DatabaseObject</span></span>
<span data-ttu-id="7fe63-122">Azure SQL 관리되는 인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-122">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe63-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe63-123">-DefaultProfile</span></span>
<span data-ttu-id="7fe63-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fe63-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fe63-125">-InputObject</span></span>
<span data-ttu-id="7fe63-126">Managed Instance 데이터베이스 SQL 분류를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe63-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7fe63-127">-InstanceName</span></span>
<span data-ttu-id="7fe63-128">Azure SQL 관리되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="7fe63-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fe63-129">-PassThru</span></span>
<span data-ttu-id="7fe63-130">cmdlet 실행의 끝에서 민감도 분류 모델을 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7fe63-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fe63-131">-ResourceGroupName</span></span>
<span data-ttu-id="7fe63-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="7fe63-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7fe63-133">-SchemaName</span></span>
<span data-ttu-id="7fe63-134">schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-134">Name of schema.</span></span>

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

### <span data-ttu-id="7fe63-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="7fe63-135">-TableName</span></span>
<span data-ttu-id="7fe63-136">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-136">Name of table.</span></span>

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

### <span data-ttu-id="7fe63-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fe63-137">-Confirm</span></span>
<span data-ttu-id="7fe63-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fe63-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fe63-139">-WhatIf</span></span>
<span data-ttu-id="7fe63-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7fe63-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fe63-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fe63-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe63-142">CommonParameters</span></span>
<span data-ttu-id="7fe63-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fe63-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe63-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7fe63-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe63-145">입력</span><span class="sxs-lookup"><span data-stu-id="7fe63-145">INPUTS</span></span>

### <span data-ttu-id="7fe63-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7fe63-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="7fe63-147">출력</span><span class="sxs-lookup"><span data-stu-id="7fe63-147">OUTPUTS</span></span>

### <span data-ttu-id="7fe63-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7fe63-148">System.Boolean</span></span>

## <span data-ttu-id="7fe63-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7fe63-149">NOTES</span></span>

## <span data-ttu-id="7fe63-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fe63-150">RELATED LINKS</span></span>

[<span data-ttu-id="7fe63-151">Azure SQL 데이터베이스 데이터 검색 및 분류에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="7fe63-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)