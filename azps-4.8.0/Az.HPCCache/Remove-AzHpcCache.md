---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211755"
---
# <span data-ttu-id="272d1-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="272d1-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="272d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="272d1-102">SYNOPSIS</span></span>
<span data-ttu-id="272d1-103">HPC 캐시를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="272d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="272d1-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="272d1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="272d1-105">DESCRIPTION</span></span>
<span data-ttu-id="272d1-106">**AzHpcCache** Cmdlet은 Azure HPC 캐시를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="272d1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="272d1-107">EXAMPLES</span></span>

### <span data-ttu-id="272d1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="272d1-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="272d1-109">변수</span><span class="sxs-lookup"><span data-stu-id="272d1-109">PARAMETERS</span></span>

### <span data-ttu-id="272d1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="272d1-110">-AsJob</span></span>
<span data-ttu-id="272d1-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="272d1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="272d1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272d1-112">-DefaultProfile</span></span>
<span data-ttu-id="272d1-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="272d1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="272d1-114">-Force</span></span>
<span data-ttu-id="272d1-115">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="272d1-116">기본적으로이 cmdlet은 캐시 제거 여부를 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="272d1-117">-이름</span><span class="sxs-lookup"><span data-stu-id="272d1-117">-Name</span></span>
<span data-ttu-id="272d1-118">캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-118">Name of cache.</span></span>

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

### <span data-ttu-id="272d1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="272d1-119">-PassThru</span></span>
<span data-ttu-id="272d1-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="272d1-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="272d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="272d1-123">캐시를 제거 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="272d1-124">-확인</span><span class="sxs-lookup"><span data-stu-id="272d1-124">-Confirm</span></span>
<span data-ttu-id="272d1-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="272d1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="272d1-126">-WhatIf</span></span>
<span data-ttu-id="272d1-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="272d1-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="272d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272d1-129">CommonParameters</span></span>
<span data-ttu-id="272d1-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="272d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272d1-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="272d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272d1-132">입력</span><span class="sxs-lookup"><span data-stu-id="272d1-132">INPUTS</span></span>

### <span data-ttu-id="272d1-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="272d1-133">System.String</span></span>

## <span data-ttu-id="272d1-134">출력</span><span class="sxs-lookup"><span data-stu-id="272d1-134">OUTPUTS</span></span>

## <span data-ttu-id="272d1-135">상속자</span><span class="sxs-lookup"><span data-stu-id="272d1-135">NOTES</span></span>

## <span data-ttu-id="272d1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="272d1-136">RELATED LINKS</span></span>
