---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363063"
---
# <span data-ttu-id="858f7-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="858f7-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="858f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858f7-102">SYNOPSIS</span></span>
<span data-ttu-id="858f7-103">저장소 대상을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="858f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="858f7-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="858f7-105">설명</span><span class="sxs-lookup"><span data-stu-id="858f7-105">DESCRIPTION</span></span>
<span data-ttu-id="858f7-106">**Remove-AzHpcCacheStorageTarget** cmdlet은 Azure HPC 캐시에서 저장소 대상을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="858f7-107">예제</span><span class="sxs-lookup"><span data-stu-id="858f7-107">EXAMPLES</span></span>

### <span data-ttu-id="858f7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="858f7-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="858f7-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="858f7-109">PARAMETERS</span></span>

### <span data-ttu-id="858f7-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="858f7-110">-AsJob</span></span>
<span data-ttu-id="858f7-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="858f7-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="858f7-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="858f7-112">-CacheName</span></span>
<span data-ttu-id="858f7-113">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-113">Name of cache.</span></span>

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

### <span data-ttu-id="858f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858f7-114">-DefaultProfile</span></span>
<span data-ttu-id="858f7-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="858f7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="858f7-116">-Force</span></span>
<span data-ttu-id="858f7-117">cmdlet이 확인 메시지를 표시하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="858f7-118">기본적으로 이 cmdlet은 저장소 대상을 제거할지 묻는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="858f7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="858f7-119">-Name</span></span>
<span data-ttu-id="858f7-120">저장소 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-120">Name of storage target.</span></span>

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

### <span data-ttu-id="858f7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="858f7-121">-PassThru</span></span>
<span data-ttu-id="858f7-122">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="858f7-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="858f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="858f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="858f7-125">캐시에서 저장소 대상을 제거하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="858f7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="858f7-126">-Confirm</span></span>
<span data-ttu-id="858f7-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="858f7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="858f7-128">-WhatIf</span></span>
<span data-ttu-id="858f7-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="858f7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="858f7-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="858f7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858f7-131">CommonParameters</span></span>
<span data-ttu-id="858f7-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="858f7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858f7-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="858f7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858f7-134">입력</span><span class="sxs-lookup"><span data-stu-id="858f7-134">INPUTS</span></span>

### <span data-ttu-id="858f7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="858f7-135">System.String</span></span>

## <span data-ttu-id="858f7-136">출력</span><span class="sxs-lookup"><span data-stu-id="858f7-136">OUTPUTS</span></span>

## <span data-ttu-id="858f7-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="858f7-137">NOTES</span></span>

## <span data-ttu-id="858f7-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="858f7-138">RELATED LINKS</span></span>
