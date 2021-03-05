---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 2de3856a51ce8b55d6db7a82f6e50027b60d9d87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013515"
---
# <span data-ttu-id="e149f-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="e149f-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="e149f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e149f-102">SYNOPSIS</span></span>
<span data-ttu-id="e149f-103">저장소 대상을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="e149f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e149f-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e149f-105">설명</span><span class="sxs-lookup"><span data-stu-id="e149f-105">DESCRIPTION</span></span>
<span data-ttu-id="e149f-106">**Remove-AzHpcCacheStorageTarget** cmdlet은 Azure HPC Cache에서 저장소 대상을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="e149f-107">예제</span><span class="sxs-lookup"><span data-stu-id="e149f-107">EXAMPLES</span></span>

### <span data-ttu-id="e149f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e149f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="e149f-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e149f-109">PARAMETERS</span></span>

### <span data-ttu-id="e149f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e149f-110">-AsJob</span></span>
<span data-ttu-id="e149f-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e149f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e149f-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="e149f-112">-CacheName</span></span>
<span data-ttu-id="e149f-113">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-113">Name of cache.</span></span>

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

### <span data-ttu-id="e149f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e149f-114">-DefaultProfile</span></span>
<span data-ttu-id="e149f-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e149f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e149f-116">-Force</span></span>
<span data-ttu-id="e149f-117">cmdlet에서 확인을 묻는 메시지가 표시되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e149f-118">기본적으로 이 cmdlet은 저장소 대상을 제거하려는지 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="e149f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e149f-119">-Name</span></span>
<span data-ttu-id="e149f-120">저장소 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-120">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e149f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e149f-121">-PassThru</span></span>
<span data-ttu-id="e149f-122">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e149f-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e149f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e149f-124">-ResourceGroupName</span></span>
<span data-ttu-id="e149f-125">캐시에서 저장소 대상을 제거하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="e149f-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e149f-126">-Confirm</span></span>
<span data-ttu-id="e149f-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e149f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e149f-128">-WhatIf</span></span>
<span data-ttu-id="e149f-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e149f-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e149f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e149f-131">CommonParameters</span></span>
<span data-ttu-id="e149f-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e149f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e149f-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e149f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e149f-134">입력</span><span class="sxs-lookup"><span data-stu-id="e149f-134">INPUTS</span></span>

### <span data-ttu-id="e149f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e149f-135">System.String</span></span>

## <span data-ttu-id="e149f-136">출력</span><span class="sxs-lookup"><span data-stu-id="e149f-136">OUTPUTS</span></span>

## <span data-ttu-id="e149f-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e149f-137">NOTES</span></span>

## <span data-ttu-id="e149f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e149f-138">RELATED LINKS</span></span>
