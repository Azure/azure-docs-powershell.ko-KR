---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: e0df378cb50d7d308d5d6a9f0acf8a15466b8a11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013536"
---
# <span data-ttu-id="902e8-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="902e8-101">New-AzHpcCache</span></span>

## <span data-ttu-id="902e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="902e8-102">SYNOPSIS</span></span>
<span data-ttu-id="902e8-103">HPC 캐시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="902e8-104">구문</span><span class="sxs-lookup"><span data-stu-id="902e8-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="902e8-105">설명</span><span class="sxs-lookup"><span data-stu-id="902e8-105">DESCRIPTION</span></span>
<span data-ttu-id="902e8-106">**New-AzHpcCache** cmdlet은 Azure HPC 캐시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="902e8-107">예제</span><span class="sxs-lookup"><span data-stu-id="902e8-107">EXAMPLES</span></span>

### <span data-ttu-id="902e8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="902e8-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="902e8-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="902e8-109">PARAMETERS</span></span>

### <span data-ttu-id="902e8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="902e8-110">-AsJob</span></span>
<span data-ttu-id="902e8-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="902e8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="902e8-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="902e8-112">-CacheSize</span></span>
<span data-ttu-id="902e8-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="902e8-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="902e8-114">-DefaultProfile</span></span>
<span data-ttu-id="902e8-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="902e8-116">-Location</span><span class="sxs-lookup"><span data-stu-id="902e8-116">-Location</span></span>
<span data-ttu-id="902e8-117">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-117">Location.</span></span>

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

### <span data-ttu-id="902e8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="902e8-118">-Name</span></span>
<span data-ttu-id="902e8-119">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="902e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="902e8-121">캐시를 만들 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-121">Name of resource group under which you want to create cache.</span></span>

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

### <span data-ttu-id="902e8-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="902e8-122">-Sku</span></span>
<span data-ttu-id="902e8-123">Sku입니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-123">Sku.</span></span>

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

### <span data-ttu-id="902e8-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="902e8-124">-SubnetUri</span></span>
<span data-ttu-id="902e8-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="902e8-125">SubnetURI.</span></span>

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

### <span data-ttu-id="902e8-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="902e8-126">-Tag</span></span>
<span data-ttu-id="902e8-127">HPC Cache와 연결되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-127">The tags to associate with HPC Cache.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="902e8-128">-확인</span><span class="sxs-lookup"><span data-stu-id="902e8-128">-Confirm</span></span>
<span data-ttu-id="902e8-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="902e8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="902e8-130">-WhatIf</span></span>
<span data-ttu-id="902e8-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="902e8-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="902e8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="902e8-133">CommonParameters</span></span>
<span data-ttu-id="902e8-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="902e8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="902e8-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="902e8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="902e8-136">입력</span><span class="sxs-lookup"><span data-stu-id="902e8-136">INPUTS</span></span>

### <span data-ttu-id="902e8-137">System.String</span><span class="sxs-lookup"><span data-stu-id="902e8-137">System.String</span></span>

### <span data-ttu-id="902e8-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="902e8-138">System.Int32</span></span>

## <span data-ttu-id="902e8-139">출력</span><span class="sxs-lookup"><span data-stu-id="902e8-139">OUTPUTS</span></span>

### <span data-ttu-id="902e8-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="902e8-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="902e8-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="902e8-141">NOTES</span></span>

## <span data-ttu-id="902e8-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="902e8-142">RELATED LINKS</span></span>
