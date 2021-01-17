---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: f524c8b30f609cb2fef3fb3f59550078b26b11b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492141"
---
# <span data-ttu-id="0b9a6-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="0b9a6-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="0b9a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="0b9a6-103">Azure SQL 관리되는 인스턴스 데이터베이스에서 열의 정보 유형 및 민감도 레이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="0b9a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b9a6-104">SYNTAX</span></span>

### <span data-ttu-id="0b9a6-105">ClassificationObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0b9a6-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b9a6-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b9a6-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b9a6-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b9a6-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b9a6-108">설명</span><span class="sxs-lookup"><span data-stu-id="0b9a6-108">DESCRIPTION</span></span>
<span data-ttu-id="0b9a6-109">이 Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet은 Azure SQL 관리되는 인스턴스 데이터베이스에서 열의 정보 형식 및 민감도 레이블을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="0b9a6-110">예제</span><span class="sxs-lookup"><span data-stu-id="0b9a6-110">EXAMPLES</span></span>

### <span data-ttu-id="0b9a6-111">예제 1: Azure SQL 관리되는 인스턴스 데이터베이스에서 열의 정보 유형 및 민감도 레이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="0b9a6-112">예제 2: Azure 관리되는 인스턴스 데이터베이스에서 권장되는 정보 유형 및 민감도 레이블을 Azure SQL 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="0b9a6-113">예제 3: Azure SQL 관리되는 인스턴스 데이터베이스에서 파이핑을 사용하여 열의 정보 유형 및 민감도 레이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="0b9a6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b9a6-114">PARAMETERS</span></span>

### <span data-ttu-id="0b9a6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b9a6-115">-AsJob</span></span>
<span data-ttu-id="0b9a6-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0b9a6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b9a6-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="0b9a6-117">-ClassificationObject</span></span>
<span data-ttu-id="0b9a6-118">Managed Instance 데이터베이스 SQL 분류를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b9a6-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0b9a6-119">-ColumnName</span></span>
<span data-ttu-id="0b9a6-120">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-120">Name of column.</span></span>

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

### <span data-ttu-id="0b9a6-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b9a6-121">-DatabaseName</span></span>
<span data-ttu-id="0b9a6-122">Azure SQL 관리되는 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="0b9a6-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="0b9a6-123">-DatabaseObject</span></span>
<span data-ttu-id="0b9a6-124">Azure SQL 관리되는 인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="0b9a6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b9a6-125">-DefaultProfile</span></span>
<span data-ttu-id="0b9a6-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b9a6-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="0b9a6-127">-InformationType</span></span>
<span data-ttu-id="0b9a6-128">열에 저장된 데이터의 정보 형식을 설명하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="0b9a6-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0b9a6-129">-InstanceName</span></span>
<span data-ttu-id="0b9a6-130">Azure SQL 관리되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="0b9a6-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b9a6-131">-PassThru</span></span>
<span data-ttu-id="0b9a6-132">cmdlet 실행의 끝에서 민감도 분류 모델을 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="0b9a6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b9a6-133">-ResourceGroupName</span></span>
<span data-ttu-id="0b9a6-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="0b9a6-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0b9a6-135">-SchemaName</span></span>
<span data-ttu-id="0b9a6-136">schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-136">Name of schema.</span></span>

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

### <span data-ttu-id="0b9a6-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="0b9a6-137">-SensitivityLabel</span></span>
<span data-ttu-id="0b9a6-138">열에 저장된 데이터의 민감도를 설명하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="0b9a6-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="0b9a6-139">-TableName</span></span>
<span data-ttu-id="0b9a6-140">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-140">Name of table.</span></span>

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

### <span data-ttu-id="0b9a6-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b9a6-141">-Confirm</span></span>
<span data-ttu-id="0b9a6-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b9a6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b9a6-143">-WhatIf</span></span>
<span data-ttu-id="0b9a6-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0b9a6-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b9a6-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b9a6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b9a6-146">CommonParameters</span></span>
<span data-ttu-id="0b9a6-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b9a6-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b9a6-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b9a6-149">입력</span><span class="sxs-lookup"><span data-stu-id="0b9a6-149">INPUTS</span></span>

### <span data-ttu-id="0b9a6-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="0b9a6-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="0b9a6-151">출력</span><span class="sxs-lookup"><span data-stu-id="0b9a6-151">OUTPUTS</span></span>

### <span data-ttu-id="0b9a6-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0b9a6-152">System.Boolean</span></span>

## <span data-ttu-id="0b9a6-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b9a6-153">NOTES</span></span>

## <span data-ttu-id="0b9a6-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b9a6-154">RELATED LINKS</span></span>

[<span data-ttu-id="0b9a6-155">Azure SQL 데이터베이스 데이터 검색 및 분류에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="0b9a6-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
