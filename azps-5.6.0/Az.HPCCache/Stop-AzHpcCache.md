---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 2d3fd9d44a06c8538233b1f130010e905055912e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013424"
---
# <span data-ttu-id="58e80-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="58e80-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="58e80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e80-102">SYNOPSIS</span></span>
<span data-ttu-id="58e80-103">HPC 캐시를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-103">Stops HPC cache.</span></span>

## <span data-ttu-id="58e80-104">구문</span><span class="sxs-lookup"><span data-stu-id="58e80-104">SYNTAX</span></span>

### <span data-ttu-id="58e80-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="58e80-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58e80-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58e80-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58e80-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58e80-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58e80-108">설명</span><span class="sxs-lookup"><span data-stu-id="58e80-108">DESCRIPTION</span></span>
<span data-ttu-id="58e80-109">**Stop-AzHpcCache** cmdlet은 Azure HPC 캐시를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="58e80-110">예제</span><span class="sxs-lookup"><span data-stu-id="58e80-110">EXAMPLES</span></span>

### <span data-ttu-id="58e80-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="58e80-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="58e80-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="58e80-112">PARAMETERS</span></span>

### <span data-ttu-id="58e80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e80-113">-DefaultProfile</span></span>
<span data-ttu-id="58e80-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58e80-115">-Force</span><span class="sxs-lookup"><span data-stu-id="58e80-115">-Force</span></span>
<span data-ttu-id="58e80-116">cmdlet에서 확인을 묻는 메시지가 표시되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="58e80-117">기본적으로 이 cmdlet은 캐시를 중지할지 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="58e80-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58e80-118">-InputObject</span></span>
<span data-ttu-id="58e80-119">중지할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-119">The cache object to stop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58e80-120">-Name</span><span class="sxs-lookup"><span data-stu-id="58e80-120">-Name</span></span>
<span data-ttu-id="58e80-121">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-121">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e80-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58e80-122">-PassThru</span></span>
<span data-ttu-id="58e80-123">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="58e80-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e80-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e80-125">-ResourceGroupName</span></span>
<span data-ttu-id="58e80-126">캐시를 중지하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-126">Name of resource group under which you want to stop cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e80-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58e80-127">-ResourceId</span></span>
<span data-ttu-id="58e80-128">캐시의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="58e80-128">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e80-129">-확인</span><span class="sxs-lookup"><span data-stu-id="58e80-129">-Confirm</span></span>
<span data-ttu-id="58e80-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58e80-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58e80-131">-WhatIf</span></span>
<span data-ttu-id="58e80-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58e80-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58e80-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e80-134">CommonParameters</span></span>
<span data-ttu-id="58e80-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="58e80-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e80-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58e80-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e80-137">입력</span><span class="sxs-lookup"><span data-stu-id="58e80-137">INPUTS</span></span>

### <span data-ttu-id="58e80-138">System.String</span><span class="sxs-lookup"><span data-stu-id="58e80-138">System.String</span></span>

## <span data-ttu-id="58e80-139">출력</span><span class="sxs-lookup"><span data-stu-id="58e80-139">OUTPUTS</span></span>

## <span data-ttu-id="58e80-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="58e80-140">NOTES</span></span>

## <span data-ttu-id="58e80-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58e80-141">RELATED LINKS</span></span>
