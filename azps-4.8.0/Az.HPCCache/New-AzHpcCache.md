---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212220"
---
# <span data-ttu-id="fd7f0-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="fd7f0-101">New-AzHpcCache</span></span>

## <span data-ttu-id="fd7f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7f0-103">HPC 캐시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="fd7f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd7f0-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd7f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fd7f0-105">DESCRIPTION</span></span>
<span data-ttu-id="fd7f0-106">**AzHpcCache** Cmdlet은 Azure HPC 캐시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="fd7f0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fd7f0-107">EXAMPLES</span></span>

### <span data-ttu-id="fd7f0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd7f0-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="fd7f0-109">변수</span><span class="sxs-lookup"><span data-stu-id="fd7f0-109">PARAMETERS</span></span>

### <span data-ttu-id="fd7f0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd7f0-110">-AsJob</span></span>
<span data-ttu-id="fd7f0-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fd7f0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd7f0-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="fd7f0-112">-CacheSize</span></span>
<span data-ttu-id="fd7f0-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-113">CacheSize.</span></span>

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

### <span data-ttu-id="fd7f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7f0-114">-DefaultProfile</span></span>
<span data-ttu-id="fd7f0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd7f0-116">-위치</span><span class="sxs-lookup"><span data-stu-id="fd7f0-116">-Location</span></span>
<span data-ttu-id="fd7f0-117">Location.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-117">Location.</span></span>

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

### <span data-ttu-id="fd7f0-118">-이름</span><span class="sxs-lookup"><span data-stu-id="fd7f0-118">-Name</span></span>
<span data-ttu-id="fd7f0-119">캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-119">Name of cache.</span></span>

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

### <span data-ttu-id="fd7f0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7f0-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd7f0-121">캐시를 만들려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-121">Name of resource group under which you want to create cache.</span></span>

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

### <span data-ttu-id="fd7f0-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="fd7f0-122">-Sku</span></span>
<span data-ttu-id="fd7f0-123">제품.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-123">Sku.</span></span>

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

### <span data-ttu-id="fd7f0-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="fd7f0-124">-SubnetUri</span></span>
<span data-ttu-id="fd7f0-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-125">SubnetURI.</span></span>

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

### <span data-ttu-id="fd7f0-126">태그</span><span class="sxs-lookup"><span data-stu-id="fd7f0-126">-Tag</span></span>
<span data-ttu-id="fd7f0-127">HPC 캐시와 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-127">The tags to associate with HPC Cache.</span></span>

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

### <span data-ttu-id="fd7f0-128">-확인</span><span class="sxs-lookup"><span data-stu-id="fd7f0-128">-Confirm</span></span>
<span data-ttu-id="fd7f0-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd7f0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd7f0-130">-WhatIf</span></span>
<span data-ttu-id="fd7f0-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd7f0-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd7f0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7f0-133">CommonParameters</span></span>
<span data-ttu-id="fd7f0-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7f0-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7f0-136">입력</span><span class="sxs-lookup"><span data-stu-id="fd7f0-136">INPUTS</span></span>

### <span data-ttu-id="fd7f0-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd7f0-137">System.String</span></span>

### <span data-ttu-id="fd7f0-138">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="fd7f0-138">System.Int32</span></span>

## <span data-ttu-id="fd7f0-139">출력</span><span class="sxs-lookup"><span data-stu-id="fd7f0-139">OUTPUTS</span></span>

### <span data-ttu-id="fd7f0-140">Microsoft. PowerShell. a i m/PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="fd7f0-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="fd7f0-141">상속자</span><span class="sxs-lookup"><span data-stu-id="fd7f0-141">NOTES</span></span>

## <span data-ttu-id="fd7f0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd7f0-142">RELATED LINKS</span></span>
