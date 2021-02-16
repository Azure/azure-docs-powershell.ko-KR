---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209368"
---
# <span data-ttu-id="0d257-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="0d257-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="0d257-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d257-102">SYNOPSIS</span></span>
<span data-ttu-id="0d257-103">HPC 캐시를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="0d257-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d257-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d257-105">설명</span><span class="sxs-lookup"><span data-stu-id="0d257-105">DESCRIPTION</span></span>
<span data-ttu-id="0d257-106">**Remove-AzHpcCache** cmdlet은 Azure HPC 캐시를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="0d257-107">예제</span><span class="sxs-lookup"><span data-stu-id="0d257-107">EXAMPLES</span></span>

### <span data-ttu-id="0d257-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d257-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="0d257-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d257-109">PARAMETERS</span></span>

### <span data-ttu-id="0d257-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d257-110">-AsJob</span></span>
<span data-ttu-id="0d257-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0d257-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d257-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d257-112">-DefaultProfile</span></span>
<span data-ttu-id="0d257-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d257-114">-Force</span><span class="sxs-lookup"><span data-stu-id="0d257-114">-Force</span></span>
<span data-ttu-id="0d257-115">cmdlet이 확인 메시지를 표시하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="0d257-116">기본적으로 이 cmdlet은 캐시를 제거할지 묻는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="0d257-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0d257-117">-Name</span></span>
<span data-ttu-id="0d257-118">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-118">Name of cache.</span></span>

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

### <span data-ttu-id="0d257-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d257-119">-PassThru</span></span>
<span data-ttu-id="0d257-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d257-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d257-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d257-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d257-123">캐시를 제거하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="0d257-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d257-124">-Confirm</span></span>
<span data-ttu-id="0d257-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d257-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d257-126">-WhatIf</span></span>
<span data-ttu-id="0d257-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0d257-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d257-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d257-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d257-129">CommonParameters</span></span>
<span data-ttu-id="0d257-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d257-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d257-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0d257-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d257-132">입력</span><span class="sxs-lookup"><span data-stu-id="0d257-132">INPUTS</span></span>

### <span data-ttu-id="0d257-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0d257-133">System.String</span></span>

## <span data-ttu-id="0d257-134">출력</span><span class="sxs-lookup"><span data-stu-id="0d257-134">OUTPUTS</span></span>

## <span data-ttu-id="0d257-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d257-135">NOTES</span></span>

## <span data-ttu-id="0d257-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d257-136">RELATED LINKS</span></span>
