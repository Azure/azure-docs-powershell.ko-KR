---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: df4ad0ea9f0e1990fa3c71915b1882baf1d3a762
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361894"
---
# <span data-ttu-id="f95ed-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="f95ed-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="f95ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f95ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f95ed-103">데이터베이스 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="f95ed-104">구문</span><span class="sxs-lookup"><span data-stu-id="f95ed-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f95ed-105">설명</span><span class="sxs-lookup"><span data-stu-id="f95ed-105">DESCRIPTION</span></span>
<span data-ttu-id="f95ed-106">**Get-AzSqlDatabaseActivity** cmdlet은 Azure SQL Database에서 데이터베이스 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="f95ed-107">예제</span><span class="sxs-lookup"><span data-stu-id="f95ed-107">EXAMPLES</span></span>

### <span data-ttu-id="f95ed-108">예제 1: 모든 SQL 데이터베이스 인스턴스에 대한 상태 확인</span><span class="sxs-lookup"><span data-stu-id="f95ed-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f95ed-109">이 명령은 ElasticPool01이라는 탄력적 SQL 모든 데이터베이스 인스턴스의 작업 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="f95ed-110">예제 2: 모든 데이터베이스 작업의 SQL</span><span class="sxs-lookup"><span data-stu-id="f95ed-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f95ed-111">이 명령은 데이터베이스의 모든 SQL 데이터베이스 작업의 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="f95ed-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f95ed-112">PARAMETERS</span></span>

### <span data-ttu-id="f95ed-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f95ed-113">-DatabaseName</span></span>
<span data-ttu-id="f95ed-114">이 cmdlet이 상태를 얻을 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95ed-115">-DefaultProfile</span></span>
<span data-ttu-id="f95ed-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f95ed-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f95ed-117">-ElasticPoolName</span></span>
<span data-ttu-id="f95ed-118">이 cmdlet이 상태를 얻을 탄력적 데이터베이스 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f95ed-119">-OperationId</span></span>
<span data-ttu-id="f95ed-120">이 cmdlet에서 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="f95ed-122">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-122">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f95ed-123">-ServerName</span></span>
<span data-ttu-id="f95ed-124">데이터베이스를 호스트하는 Microsoft SQL Server 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f95ed-125">-Confirm</span></span>
<span data-ttu-id="f95ed-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f95ed-127">-WhatIf</span></span>
<span data-ttu-id="f95ed-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f95ed-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f95ed-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95ed-130">CommonParameters</span></span>
<span data-ttu-id="f95ed-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f95ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95ed-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f95ed-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95ed-133">입력</span><span class="sxs-lookup"><span data-stu-id="f95ed-133">INPUTS</span></span>

### <span data-ttu-id="f95ed-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f95ed-134">System.String</span></span>

### <span data-ttu-id="f95ed-135">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f95ed-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f95ed-136">출력</span><span class="sxs-lookup"><span data-stu-id="f95ed-136">OUTPUTS</span></span>

### <span data-ttu-id="f95ed-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="f95ed-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="f95ed-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f95ed-138">NOTES</span></span>

## <span data-ttu-id="f95ed-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f95ed-139">RELATED LINKS</span></span>
