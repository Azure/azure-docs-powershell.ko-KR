---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c594a9bf247355201bc08e438af1d9dff8cd3f7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204776"
---
# <span data-ttu-id="a2e6f-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="a2e6f-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="a2e6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e6f-103">Azure SQL 관리 인스턴스 데이터베이스에서 열의 정보 유형 및 민감도 레이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a2e6f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2e6f-104">SYNTAX</span></span>

### <span data-ttu-id="a2e6f-105">ClassificationObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a2e6f-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2e6f-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2e6f-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2e6f-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2e6f-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2e6f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a2e6f-108">DESCRIPTION</span></span>
<span data-ttu-id="a2e6f-109">Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet은 Azure SQL 관리 인스턴스 데이터베이스의 열에 대 한 정보 유형 및 민감도 레이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a2e6f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a2e6f-110">EXAMPLES</span></span>

### <span data-ttu-id="a2e6f-111">예제 1: Azure SQL 관리 인스턴스 데이터베이스에서 열의 정보 유형 및 민감도 레이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="a2e6f-112">예제 2: 파이핑을 사용 하는 Azure SQL 관리 인스턴스 데이터베이스에서 열의 현재 정보 유형 및 민감도 레이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="a2e6f-113">예제 3: 파이프를 사용 하는 Azure SQL 관리 인스턴스 데이터베이스에서 열의 정보 형식 및 민감도 레이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="a2e6f-114">변수</span><span class="sxs-lookup"><span data-stu-id="a2e6f-114">PARAMETERS</span></span>

### <span data-ttu-id="a2e6f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2e6f-115">-AsJob</span></span>
<span data-ttu-id="a2e6f-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a2e6f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2e6f-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="a2e6f-117">-ClassificationObject</span></span>
<span data-ttu-id="a2e6f-118">SQL 관리 되는 인스턴스 데이터베이스 민감도 분류를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="a2e6f-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a2e6f-119">-ColumnName</span></span>
<span data-ttu-id="a2e6f-120">열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-120">Name of column.</span></span>

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

### <span data-ttu-id="a2e6f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2e6f-121">-DatabaseName</span></span>
<span data-ttu-id="a2e6f-122">Azure SQL 관리 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="a2e6f-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a2e6f-123">-DatabaseObject</span></span>
<span data-ttu-id="a2e6f-124">Azure SQL 관리 되는 인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="a2e6f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e6f-125">-DefaultProfile</span></span>
<span data-ttu-id="a2e6f-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2e6f-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a2e6f-127">-InstanceName</span></span>
<span data-ttu-id="a2e6f-128">Azure SQL 관리 되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="a2e6f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2e6f-129">-PassThru</span></span>
<span data-ttu-id="a2e6f-130">Cmdlet 실행 종료 시 민감도 분류 모델을 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="a2e6f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e6f-131">-ResourceGroupName</span></span>
<span data-ttu-id="a2e6f-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2e6f-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a2e6f-133">-SchemaName</span></span>
<span data-ttu-id="a2e6f-134">스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-134">Name of schema.</span></span>

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

### <span data-ttu-id="a2e6f-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="a2e6f-135">-TableName</span></span>
<span data-ttu-id="a2e6f-136">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-136">Name of table.</span></span>

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

### <span data-ttu-id="a2e6f-137">-확인</span><span class="sxs-lookup"><span data-stu-id="a2e6f-137">-Confirm</span></span>
<span data-ttu-id="a2e6f-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2e6f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2e6f-139">-WhatIf</span></span>
<span data-ttu-id="a2e6f-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2e6f-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2e6f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e6f-142">CommonParameters</span></span>
<span data-ttu-id="a2e6f-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e6f-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a2e6f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e6f-145">입력</span><span class="sxs-lookup"><span data-stu-id="a2e6f-145">INPUTS</span></span>

### <span data-ttu-id="a2e6f-146">DataClassification. ManagedDatabaseSensitivityClassificationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="a2e6f-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="a2e6f-147">출력</span><span class="sxs-lookup"><span data-stu-id="a2e6f-147">OUTPUTS</span></span>

### <span data-ttu-id="a2e6f-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a2e6f-148">System.Boolean</span></span>

## <span data-ttu-id="a2e6f-149">상속자</span><span class="sxs-lookup"><span data-stu-id="a2e6f-149">NOTES</span></span>

## <span data-ttu-id="a2e6f-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2e6f-150">RELATED LINKS</span></span>

[<span data-ttu-id="a2e6f-151">Azure SQL 데이터베이스 데이터 검색 및 분류에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="a2e6f-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
