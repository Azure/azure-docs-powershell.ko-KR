---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203997"
---
# <span data-ttu-id="9ffe5-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="9ffe5-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="9ffe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ffe5-102">SYNOPSIS</span></span>
<span data-ttu-id="9ffe5-103">HPC 캐시를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="9ffe5-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ffe5-104">SYNTAX</span></span>

### <span data-ttu-id="9ffe5-105">FlushParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9ffe5-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ffe5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ffe5-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ffe5-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ffe5-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ffe5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ffe5-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ffe5-109">설명</span><span class="sxs-lookup"><span data-stu-id="9ffe5-109">DESCRIPTION</span></span>
<span data-ttu-id="9ffe5-110">**Update-AzHpcCache** cmdlet은 Azure HPC 캐시를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="9ffe5-111">예제</span><span class="sxs-lookup"><span data-stu-id="9ffe5-111">EXAMPLES</span></span>

### <span data-ttu-id="9ffe5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ffe5-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="9ffe5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ffe5-113">PARAMETERS</span></span>

### <span data-ttu-id="9ffe5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ffe5-114">-AsJob</span></span>
<span data-ttu-id="9ffe5-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9ffe5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ffe5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ffe5-116">-DefaultProfile</span></span>
<span data-ttu-id="9ffe5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ffe5-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="9ffe5-118">-Flush</span></span>
<span data-ttu-id="9ffe5-119">HPC 캐시를 플러시합니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ffe5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9ffe5-120">-Force</span></span>
<span data-ttu-id="9ffe5-121">cmdlet이 확인 메시지를 표시하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="9ffe5-122">기본적으로 이 cmdlet은 캐시를 업데이트할지 확인하라는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="9ffe5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ffe5-123">-InputObject</span></span>
<span data-ttu-id="9ffe5-124">업데이트할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-124">The cache object to update.</span></span>

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

### <span data-ttu-id="9ffe5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9ffe5-125">-Name</span></span>
<span data-ttu-id="9ffe5-126">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-126">Name of cache.</span></span>

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

### <span data-ttu-id="9ffe5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ffe5-127">-PassThru</span></span>
<span data-ttu-id="9ffe5-128">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9ffe5-129">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9ffe5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ffe5-130">-ResourceGroupName</span></span>
<span data-ttu-id="9ffe5-131">캐시를 업데이트하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="9ffe5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ffe5-132">-ResourceId</span></span>
<span data-ttu-id="9ffe5-133">캐시의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9ffe5-133">The resource id of the Cache</span></span>

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

### <span data-ttu-id="9ffe5-134">-Upgrade</span><span class="sxs-lookup"><span data-stu-id="9ffe5-134">-Upgrade</span></span>
<span data-ttu-id="9ffe5-135">HpcCache를 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ffe5-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ffe5-136">-Confirm</span></span>
<span data-ttu-id="9ffe5-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ffe5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ffe5-138">-WhatIf</span></span>
<span data-ttu-id="9ffe5-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9ffe5-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ffe5-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ffe5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ffe5-141">CommonParameters</span></span>
<span data-ttu-id="9ffe5-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ffe5-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ffe5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ffe5-144">입력</span><span class="sxs-lookup"><span data-stu-id="9ffe5-144">INPUTS</span></span>

### <span data-ttu-id="9ffe5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9ffe5-145">System.String</span></span>

## <span data-ttu-id="9ffe5-146">출력</span><span class="sxs-lookup"><span data-stu-id="9ffe5-146">OUTPUTS</span></span>

## <span data-ttu-id="9ffe5-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ffe5-147">NOTES</span></span>

## <span data-ttu-id="9ffe5-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ffe5-148">RELATED LINKS</span></span>
