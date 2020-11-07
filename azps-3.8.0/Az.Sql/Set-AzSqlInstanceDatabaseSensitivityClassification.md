---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: f524c8b30f609cb2fef3fb3f59550078b26b11b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878805"
---
# <span data-ttu-id="1b93d-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="1b93d-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="1b93d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b93d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b93d-103">Azure SQL 관리 인스턴스 데이터베이스의 열에 대 한 정보 유형 및 민감도 레이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="1b93d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1b93d-104">SYNTAX</span></span>

### <span data-ttu-id="1b93d-105">ClassificationObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1b93d-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b93d-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b93d-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b93d-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b93d-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b93d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1b93d-108">DESCRIPTION</span></span>
<span data-ttu-id="1b93d-109">Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet은 Azure SQL 관리 인스턴스 데이터베이스의 열에 대 한 정보 유형 및 민감도 레이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="1b93d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1b93d-110">EXAMPLES</span></span>

### <span data-ttu-id="1b93d-111">예제 1: Azure SQL 관리 인스턴스 데이터베이스에서 열의 정보 유형 및 민감도 레이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="1b93d-112">예제 2: Azure SQL 관리 인스턴스 데이터베이스에서 열에 대 한 권장 정보 유형 및 민감도 레이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="1b93d-113">예제 3: 파이프를 사용 하 여 Azure SQL 관리 인스턴스 데이터베이스의 열에 대 한 정보 유형 및 민감도 레이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="1b93d-114">변수</span><span class="sxs-lookup"><span data-stu-id="1b93d-114">PARAMETERS</span></span>

### <span data-ttu-id="1b93d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b93d-115">-AsJob</span></span>
<span data-ttu-id="1b93d-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1b93d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b93d-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="1b93d-117">-ClassificationObject</span></span>
<span data-ttu-id="1b93d-118">SQL 관리 되는 인스턴스 데이터베이스 민감도 분류를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="1b93d-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="1b93d-119">-ColumnName</span></span>
<span data-ttu-id="1b93d-120">열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-120">Name of column.</span></span>

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

### <span data-ttu-id="1b93d-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b93d-121">-DatabaseName</span></span>
<span data-ttu-id="1b93d-122">Azure SQL 관리 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="1b93d-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="1b93d-123">-DatabaseObject</span></span>
<span data-ttu-id="1b93d-124">Azure SQL 관리 되는 인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="1b93d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b93d-125">-DefaultProfile</span></span>
<span data-ttu-id="1b93d-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b93d-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="1b93d-127">-InformationType</span></span>
<span data-ttu-id="1b93d-128">열에 저장 된 데이터의 정보 유형을 설명 하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="1b93d-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1b93d-129">-InstanceName</span></span>
<span data-ttu-id="1b93d-130">Azure SQL 관리 되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="1b93d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b93d-131">-PassThru</span></span>
<span data-ttu-id="1b93d-132">Cmdlet 실행 종료 시 민감도 분류 모델을 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="1b93d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b93d-133">-ResourceGroupName</span></span>
<span data-ttu-id="1b93d-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="1b93d-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="1b93d-135">-SchemaName</span></span>
<span data-ttu-id="1b93d-136">스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-136">Name of schema.</span></span>

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

### <span data-ttu-id="1b93d-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="1b93d-137">-SensitivityLabel</span></span>
<span data-ttu-id="1b93d-138">열에 저장 된 데이터의 민감도를 설명 하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="1b93d-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="1b93d-139">-TableName</span></span>
<span data-ttu-id="1b93d-140">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-140">Name of table.</span></span>

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

### <span data-ttu-id="1b93d-141">-확인</span><span class="sxs-lookup"><span data-stu-id="1b93d-141">-Confirm</span></span>
<span data-ttu-id="1b93d-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b93d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b93d-143">-WhatIf</span></span>
<span data-ttu-id="1b93d-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b93d-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b93d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b93d-146">CommonParameters</span></span>
<span data-ttu-id="1b93d-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b93d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b93d-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1b93d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b93d-149">입력</span><span class="sxs-lookup"><span data-stu-id="1b93d-149">INPUTS</span></span>

### <span data-ttu-id="1b93d-150">DataClassification. ManagedDatabaseSensitivityClassificationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="1b93d-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="1b93d-151">출력</span><span class="sxs-lookup"><span data-stu-id="1b93d-151">OUTPUTS</span></span>

### <span data-ttu-id="1b93d-152">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1b93d-152">System.Boolean</span></span>

## <span data-ttu-id="1b93d-153">상속자</span><span class="sxs-lookup"><span data-stu-id="1b93d-153">NOTES</span></span>

## <span data-ttu-id="1b93d-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b93d-154">RELATED LINKS</span></span>

[<span data-ttu-id="1b93d-155">Azure SQL 데이터베이스 데이터 검색 및 분류에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="1b93d-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
