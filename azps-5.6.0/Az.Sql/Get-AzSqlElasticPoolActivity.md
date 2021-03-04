---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 013a7c40a5acfb4306d53e0ff5b8da1b54f86e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999563"
---
# <span data-ttu-id="95a53-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="95a53-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="95a53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95a53-102">SYNOPSIS</span></span>
<span data-ttu-id="95a53-103">탄력적 풀에서 작업 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="95a53-104">구문</span><span class="sxs-lookup"><span data-stu-id="95a53-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95a53-105">설명</span><span class="sxs-lookup"><span data-stu-id="95a53-105">DESCRIPTION</span></span>
<span data-ttu-id="95a53-106">**Get-AzSqlElasticPoolActivity** cmdlet은 Azure SQL 탄력적 풀에서 작업 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="95a53-107">풀 만들기 및 구성 업데이트의 상태를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="95a53-108">예제</span><span class="sxs-lookup"><span data-stu-id="95a53-108">EXAMPLES</span></span>

### <span data-ttu-id="95a53-109">예제 1: 탄력적 풀에 대한 작업 상태 확인</span><span class="sxs-lookup"><span data-stu-id="95a53-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="95a53-110">이 명령은 ElasticPool01이라는 탄력적 풀에 대한 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="95a53-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="95a53-111">PARAMETERS</span></span>

### <span data-ttu-id="95a53-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a53-112">-DefaultProfile</span></span>
<span data-ttu-id="95a53-113">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="95a53-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95a53-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="95a53-114">-ElasticPoolName</span></span>
<span data-ttu-id="95a53-115">탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="95a53-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="95a53-116">-OperationId</span></span>
<span data-ttu-id="95a53-117">검색할 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="95a53-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95a53-118">-ResourceGroupName</span></span>
<span data-ttu-id="95a53-119">탄력적 풀이 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="95a53-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="95a53-120">-ServerName</span></span>
<span data-ttu-id="95a53-121">탄력적 풀을 포함하는 서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="95a53-122">-확인</span><span class="sxs-lookup"><span data-stu-id="95a53-122">-Confirm</span></span>
<span data-ttu-id="95a53-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a53-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95a53-124">-WhatIf</span></span>
<span data-ttu-id="95a53-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95a53-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a53-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a53-127">CommonParameters</span></span>
<span data-ttu-id="95a53-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95a53-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a53-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95a53-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a53-130">입력</span><span class="sxs-lookup"><span data-stu-id="95a53-130">INPUTS</span></span>

### <span data-ttu-id="95a53-131">System.String</span><span class="sxs-lookup"><span data-stu-id="95a53-131">System.String</span></span>

### <span data-ttu-id="95a53-132">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="95a53-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="95a53-133">출력</span><span class="sxs-lookup"><span data-stu-id="95a53-133">OUTPUTS</span></span>

### <span data-ttu-id="95a53-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="95a53-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="95a53-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95a53-135">NOTES</span></span>

## <span data-ttu-id="95a53-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95a53-136">RELATED LINKS</span></span>

[<span data-ttu-id="95a53-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95a53-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="95a53-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="95a53-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="95a53-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95a53-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="95a53-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95a53-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="95a53-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95a53-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


