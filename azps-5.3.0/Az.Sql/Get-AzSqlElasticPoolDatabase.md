---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 2e24dc80b93d72722d05a7dced05cbea02751a05
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374802"
---
# <span data-ttu-id="577bd-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="577bd-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="577bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="577bd-102">SYNOPSIS</span></span>
<span data-ttu-id="577bd-103">탄력적 풀의 탄력적 데이터베이스 및 해당 속성 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="577bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="577bd-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="577bd-105">설명</span><span class="sxs-lookup"><span data-stu-id="577bd-105">DESCRIPTION</span></span>
<span data-ttu-id="577bd-106">**Get-AzSqlElasticPoolDatabase** cmdlet은 탄력적 풀의 탄력적 데이터베이스 및 해당 속성 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="577bd-107">Azure SQL Database에서 탄력적 데이터베이스의 이름을 지정하여 해당 데이터베이스에 대한 속성 값을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="577bd-108">예제</span><span class="sxs-lookup"><span data-stu-id="577bd-108">EXAMPLES</span></span>

### <span data-ttu-id="577bd-109">예제 1: 탄력적 풀의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="577bd-110">이 명령은 ElasticPool01이라는 탄력적 풀의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="577bd-111">예제 2: 필터링을 사용하여 탄력적 풀의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="577bd-112">이 명령은 "Database"로 시작하는 ElasticPool01이라는 탄력적 풀의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="577bd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="577bd-113">PARAMETERS</span></span>

### <span data-ttu-id="577bd-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="577bd-114">-DatabaseName</span></span>
<span data-ttu-id="577bd-115">이 cmdlet이 SQL 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="577bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577bd-116">-DefaultProfile</span></span>
<span data-ttu-id="577bd-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="577bd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="577bd-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="577bd-118">-ElasticPoolName</span></span>
<span data-ttu-id="577bd-119">탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-119">Specifies the name of an elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577bd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="577bd-120">-ResourceGroupName</span></span>
<span data-ttu-id="577bd-121">탄력적 풀이 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="577bd-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="577bd-122">-ServerName</span></span>
<span data-ttu-id="577bd-123">탄력적 풀을 포함하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="577bd-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="577bd-124">-Confirm</span></span>
<span data-ttu-id="577bd-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577bd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="577bd-126">-WhatIf</span></span>
<span data-ttu-id="577bd-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="577bd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577bd-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577bd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577bd-129">CommonParameters</span></span>
<span data-ttu-id="577bd-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="577bd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577bd-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="577bd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577bd-132">입력</span><span class="sxs-lookup"><span data-stu-id="577bd-132">INPUTS</span></span>

### <span data-ttu-id="577bd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="577bd-133">System.String</span></span>

## <span data-ttu-id="577bd-134">출력</span><span class="sxs-lookup"><span data-stu-id="577bd-134">OUTPUTS</span></span>

### <span data-ttu-id="577bd-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="577bd-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="577bd-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="577bd-136">NOTES</span></span>

## <span data-ttu-id="577bd-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="577bd-137">RELATED LINKS</span></span>

[<span data-ttu-id="577bd-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="577bd-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="577bd-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="577bd-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="577bd-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="577bd-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="577bd-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="577bd-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="577bd-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="577bd-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

