---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 4409825b758d34e656b18a198aefd0da32824fcd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216964"
---
# <span data-ttu-id="e3e74-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="e3e74-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="e3e74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3e74-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e74-103">데이터베이스의 열에 대 한 정보 유형 및 민감도 레이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="e3e74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3e74-104">SYNTAX</span></span>

### <span data-ttu-id="e3e74-105">ClassificationObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e3e74-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e74-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3e74-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e74-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3e74-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3e74-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e3e74-108">DESCRIPTION</span></span>
<span data-ttu-id="e3e74-109">Set-AzSqlDatabaseSensitivityClassification cmdlet은 데이터베이스의 열에 대 한 정보 유형 및 민감도 레이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="e3e74-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e3e74-110">EXAMPLES</span></span>

### <span data-ttu-id="e3e74-111">예제 1: Azure SQL 데이터베이스에서 열의 정보 유형 및 민감도 레이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="e3e74-112">예제 2: Azure SQL 데이터베이스에서 열의 권장 정보 유형 및 민감도 레이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="e3e74-113">예제 3: 파이프를 사용 하 여 Azure SQL 데이터베이스의 열에 대 한 정보 유형 및 민감도 레이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="e3e74-114">변수</span><span class="sxs-lookup"><span data-stu-id="e3e74-114">PARAMETERS</span></span>

### <span data-ttu-id="e3e74-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3e74-115">-AsJob</span></span>
<span data-ttu-id="e3e74-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e3e74-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3e74-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="e3e74-117">-ClassificationObject</span></span>
<span data-ttu-id="e3e74-118">SQL 데이터베이스 민감도 분류를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="e3e74-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e3e74-119">-ColumnName</span></span>
<span data-ttu-id="e3e74-120">열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-120">Name of column.</span></span>

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

### <span data-ttu-id="e3e74-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3e74-121">-DatabaseName</span></span>
<span data-ttu-id="e3e74-122">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="e3e74-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e3e74-123">-DatabaseObject</span></span>
<span data-ttu-id="e3e74-124">SQL 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-124">The SQL database object.</span></span>

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

### <span data-ttu-id="e3e74-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e74-125">-DefaultProfile</span></span>
<span data-ttu-id="e3e74-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3e74-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="e3e74-127">-InformationType</span></span>
<span data-ttu-id="e3e74-128">열에 저장 된 데이터의 정보 유형을 설명 하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="e3e74-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3e74-129">-PassThru</span></span>
<span data-ttu-id="e3e74-130">Cmdlet 실행 종료 시 민감도 분류 모델을 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="e3e74-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e74-131">-ResourceGroupName</span></span>
<span data-ttu-id="e3e74-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="e3e74-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e3e74-133">-SchemaName</span></span>
<span data-ttu-id="e3e74-134">스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-134">Name of schema.</span></span>

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

### <span data-ttu-id="e3e74-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="e3e74-135">-SensitivityLabel</span></span>
<span data-ttu-id="e3e74-136">열에 저장 된 데이터의 민감도를 설명 하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-136">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="e3e74-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e3e74-137">-ServerName</span></span>
<span data-ttu-id="e3e74-138">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-138">SQL server name.</span></span>

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

### <span data-ttu-id="e3e74-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="e3e74-139">-TableName</span></span>
<span data-ttu-id="e3e74-140">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-140">Name of table.</span></span>

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

### <span data-ttu-id="e3e74-141">-확인</span><span class="sxs-lookup"><span data-stu-id="e3e74-141">-Confirm</span></span>
<span data-ttu-id="e3e74-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3e74-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e74-143">-WhatIf</span></span>
<span data-ttu-id="e3e74-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3e74-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3e74-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e74-146">CommonParameters</span></span>
<span data-ttu-id="e3e74-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e74-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e74-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3e74-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e74-149">입력</span><span class="sxs-lookup"><span data-stu-id="e3e74-149">INPUTS</span></span>

### <span data-ttu-id="e3e74-150">DataClassification. SqlDatabaseSensitivityClassificationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="e3e74-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="e3e74-151">출력</span><span class="sxs-lookup"><span data-stu-id="e3e74-151">OUTPUTS</span></span>

### <span data-ttu-id="e3e74-152">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e3e74-152">System.Boolean</span></span>

## <span data-ttu-id="e3e74-153">상속자</span><span class="sxs-lookup"><span data-stu-id="e3e74-153">NOTES</span></span>

## <span data-ttu-id="e3e74-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3e74-154">RELATED LINKS</span></span>

[<span data-ttu-id="e3e74-155">Azure SQL 데이터베이스 데이터 검색 및 분류에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="e3e74-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
