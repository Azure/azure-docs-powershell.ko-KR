---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489563"
---
# <span data-ttu-id="59959-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="59959-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="59959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59959-102">SYNOPSIS</span></span>
<span data-ttu-id="59959-103">HPC 캐시에서 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="59959-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="59959-104">구문</span><span class="sxs-lookup"><span data-stu-id="59959-104">SYNTAX</span></span>

### <span data-ttu-id="59959-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="59959-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59959-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59959-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59959-107">설명</span><span class="sxs-lookup"><span data-stu-id="59959-107">DESCRIPTION</span></span>
<span data-ttu-id="59959-108">**Set-AzHpcCache** cmdlet은 Azure HPC 캐시 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="59959-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="59959-109">예제</span><span class="sxs-lookup"><span data-stu-id="59959-109">EXAMPLES</span></span>

### <span data-ttu-id="59959-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="59959-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="59959-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59959-111">PARAMETERS</span></span>

### <span data-ttu-id="59959-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59959-112">-AsJob</span></span>
<span data-ttu-id="59959-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="59959-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59959-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59959-114">-DefaultProfile</span></span>
<span data-ttu-id="59959-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59959-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59959-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59959-116">-InputObject</span></span>
<span data-ttu-id="59959-117">업데이트할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="59959-117">The cache object to update.</span></span>

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

### <span data-ttu-id="59959-118">-Name</span><span class="sxs-lookup"><span data-stu-id="59959-118">-Name</span></span>
<span data-ttu-id="59959-119">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59959-119">Name of cache.</span></span>

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

### <span data-ttu-id="59959-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59959-120">-ResourceGroupName</span></span>
<span data-ttu-id="59959-121">캐시를 업데이트하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59959-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="59959-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="59959-122">-Tag</span></span>
<span data-ttu-id="59959-123">HPC 캐시와 연결하기 위해 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="59959-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59959-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59959-124">-Confirm</span></span>
<span data-ttu-id="59959-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="59959-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59959-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59959-126">-WhatIf</span></span>
<span data-ttu-id="59959-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="59959-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59959-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59959-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59959-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59959-129">CommonParameters</span></span>
<span data-ttu-id="59959-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59959-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59959-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="59959-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59959-132">입력</span><span class="sxs-lookup"><span data-stu-id="59959-132">INPUTS</span></span>

### <span data-ttu-id="59959-133">System.String</span><span class="sxs-lookup"><span data-stu-id="59959-133">System.String</span></span>

### <span data-ttu-id="59959-134">System.Int32</span><span class="sxs-lookup"><span data-stu-id="59959-134">System.Int32</span></span>

## <span data-ttu-id="59959-135">출력</span><span class="sxs-lookup"><span data-stu-id="59959-135">OUTPUTS</span></span>

### <span data-ttu-id="59959-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="59959-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="59959-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59959-137">NOTES</span></span>

## <span data-ttu-id="59959-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59959-138">RELATED LINKS</span></span>
