---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 15da7969c5e47376e04bb78a02ff611c9326b947
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226312"
---
# <span data-ttu-id="3e877-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="3e877-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="3e877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e877-102">SYNOPSIS</span></span>
<span data-ttu-id="3e877-103">데이터베이스의 열에 대 한 정보 유형 및 민감도 레이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="3e877-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e877-104">SYNTAX</span></span>

### <span data-ttu-id="3e877-105">ClassificationObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3e877-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e877-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e877-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e877-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e877-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e877-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3e877-108">DESCRIPTION</span></span>
<span data-ttu-id="3e877-109">Remove-AzSqlDatabaseSensitivityClassification cmdlet은 데이터베이스의 열에 대 한 정보 형식 및 민감도 레이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="3e877-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3e877-110">EXAMPLES</span></span>

### <span data-ttu-id="3e877-111">예제 1: Azure SQL 데이터베이스에서 열의 정보 유형 및 민감도 레이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="3e877-112">예제 2: 파이핑을 사용 하 여 Azure SQL 데이터베이스에서 열의 현재 정보 유형 및 민감도 레이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="3e877-113">예제 3: 파이핑을 사용 하 여 Azure SQL 데이터베이스에서 열의 정보 유형 및 민감도 레이블 제거</span><span class="sxs-lookup"><span data-stu-id="3e877-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="3e877-114">변수</span><span class="sxs-lookup"><span data-stu-id="3e877-114">PARAMETERS</span></span>

### <span data-ttu-id="3e877-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e877-115">-AsJob</span></span>
<span data-ttu-id="3e877-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3e877-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e877-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="3e877-117">-ClassificationObject</span></span>
<span data-ttu-id="3e877-118">SQL 데이터베이스 민감도 분류를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="3e877-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3e877-119">-ColumnName</span></span>
<span data-ttu-id="3e877-120">열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-120">Name of column.</span></span>

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

### <span data-ttu-id="3e877-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e877-121">-DatabaseName</span></span>
<span data-ttu-id="3e877-122">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="3e877-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="3e877-123">-DatabaseObject</span></span>
<span data-ttu-id="3e877-124">SQL 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-124">The SQL database object.</span></span>

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

### <span data-ttu-id="3e877-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e877-125">-DefaultProfile</span></span>
<span data-ttu-id="3e877-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e877-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e877-127">-PassThru</span></span>
<span data-ttu-id="3e877-128">Cmdlet 실행 종료 시 민감도 분류 모델을 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="3e877-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e877-129">-ResourceGroupName</span></span>
<span data-ttu-id="3e877-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e877-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3e877-131">-SchemaName</span></span>
<span data-ttu-id="3e877-132">스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-132">Name of schema.</span></span>

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

### <span data-ttu-id="3e877-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3e877-133">-ServerName</span></span>
<span data-ttu-id="3e877-134">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-134">SQL server name.</span></span>

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

### <span data-ttu-id="3e877-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="3e877-135">-TableName</span></span>
<span data-ttu-id="3e877-136">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-136">Name of table.</span></span>

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

### <span data-ttu-id="3e877-137">-확인</span><span class="sxs-lookup"><span data-stu-id="3e877-137">-Confirm</span></span>
<span data-ttu-id="3e877-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e877-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e877-139">-WhatIf</span></span>
<span data-ttu-id="3e877-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e877-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e877-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e877-142">CommonParameters</span></span>
<span data-ttu-id="3e877-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e877-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e877-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3e877-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e877-145">입력</span><span class="sxs-lookup"><span data-stu-id="3e877-145">INPUTS</span></span>

### <span data-ttu-id="3e877-146">DataClassification. SqlDatabaseSensitivityClassificationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="3e877-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="3e877-147">출력</span><span class="sxs-lookup"><span data-stu-id="3e877-147">OUTPUTS</span></span>

### <span data-ttu-id="3e877-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3e877-148">System.Boolean</span></span>

## <span data-ttu-id="3e877-149">상속자</span><span class="sxs-lookup"><span data-stu-id="3e877-149">NOTES</span></span>

## <span data-ttu-id="3e877-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e877-150">RELATED LINKS</span></span>

[<span data-ttu-id="3e877-151">Azure SQL 데이터베이스 데이터 검색 및 분류에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="3e877-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
