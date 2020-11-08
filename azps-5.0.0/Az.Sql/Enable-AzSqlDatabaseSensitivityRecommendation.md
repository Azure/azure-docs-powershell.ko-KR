---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216988"
---
# <span data-ttu-id="1a414-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="1a414-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="1a414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a414-102">SYNOPSIS</span></span>
<span data-ttu-id="1a414-103">데이터베이스에서 열에 대해 우편물 종류 추천을 사용 하도록 설정 합니다 (권장 사항은 모든 열에 기본적으로 사용 하도록 설정 되어 있음).</span><span class="sxs-lookup"><span data-stu-id="1a414-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="1a414-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a414-104">SYNTAX</span></span>

### <span data-ttu-id="1a414-105">InputObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1a414-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a414-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a414-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a414-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a414-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a414-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1a414-108">DESCRIPTION</span></span>
<span data-ttu-id="1a414-109">Enable-AzSqlDatabaseSensitivityRecommendation cmdlet은 데이터베이스의 열에 대 한 민감도 추천을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="1a414-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1a414-110">EXAMPLES</span></span>

### <span data-ttu-id="1a414-111">예제 1: Azure SQL 데이터베이스에서 지정 된 열에 대해 민감도 추천을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="1a414-112">예제 2: 파이핑을 사용 하 여 지정 된 열 Azure SQL 데이터베이스에 대해 민감도 추천을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="1a414-113">변수</span><span class="sxs-lookup"><span data-stu-id="1a414-113">PARAMETERS</span></span>

### <span data-ttu-id="1a414-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a414-114">-AsJob</span></span>
<span data-ttu-id="1a414-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1a414-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a414-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="1a414-116">-ColumnName</span></span>
<span data-ttu-id="1a414-117">열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-117">Name of column.</span></span>

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

### <span data-ttu-id="1a414-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1a414-118">-DatabaseName</span></span>
<span data-ttu-id="1a414-119">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="1a414-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="1a414-120">-DatabaseObject</span></span>
<span data-ttu-id="1a414-121">SQL 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-121">The SQL database object.</span></span>

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

### <span data-ttu-id="1a414-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a414-122">-DefaultProfile</span></span>
<span data-ttu-id="1a414-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a414-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a414-124">-InputObject</span></span>
<span data-ttu-id="1a414-125">SQL 데이터베이스 민감도 분류를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-125">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="1a414-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a414-126">-PassThru</span></span>
<span data-ttu-id="1a414-127">Cmdlet 실행 종료 시 민감도 분류 모델을 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="1a414-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a414-128">-ResourceGroupName</span></span>
<span data-ttu-id="1a414-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="1a414-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="1a414-130">-SchemaName</span></span>
<span data-ttu-id="1a414-131">스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-131">Name of schema.</span></span>

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

### <span data-ttu-id="1a414-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1a414-132">-ServerName</span></span>
<span data-ttu-id="1a414-133">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-133">SQL server name.</span></span>

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

### <span data-ttu-id="1a414-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="1a414-134">-TableName</span></span>
<span data-ttu-id="1a414-135">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-135">Name of table.</span></span>

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

### <span data-ttu-id="1a414-136">-확인</span><span class="sxs-lookup"><span data-stu-id="1a414-136">-Confirm</span></span>
<span data-ttu-id="1a414-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a414-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a414-138">-WhatIf</span></span>
<span data-ttu-id="1a414-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a414-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a414-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a414-141">CommonParameters</span></span>
<span data-ttu-id="1a414-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a414-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a414-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1a414-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a414-144">입력</span><span class="sxs-lookup"><span data-stu-id="1a414-144">INPUTS</span></span>

### <span data-ttu-id="1a414-145">DataClassification. SqlDatabaseSensitivityClassificationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="1a414-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="1a414-146">출력</span><span class="sxs-lookup"><span data-stu-id="1a414-146">OUTPUTS</span></span>

### <span data-ttu-id="1a414-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1a414-147">System.Boolean</span></span>

## <span data-ttu-id="1a414-148">상속자</span><span class="sxs-lookup"><span data-stu-id="1a414-148">NOTES</span></span>

## <span data-ttu-id="1a414-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a414-149">RELATED LINKS</span></span>

[<span data-ttu-id="1a414-150">Azure SQL 데이터베이스 데이터 검색 및 분류에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="1a414-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)