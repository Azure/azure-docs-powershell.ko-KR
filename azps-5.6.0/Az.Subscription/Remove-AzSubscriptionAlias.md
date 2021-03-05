---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 2acca5ede1d6ef7e4a3767b87053fb356555993d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971648"
---
# <span data-ttu-id="95860-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="95860-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="95860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95860-102">SYNOPSIS</span></span>
<span data-ttu-id="95860-103">구독 별칭 삭제</span><span class="sxs-lookup"><span data-stu-id="95860-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="95860-104">구문</span><span class="sxs-lookup"><span data-stu-id="95860-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95860-105">설명</span><span class="sxs-lookup"><span data-stu-id="95860-105">DESCRIPTION</span></span>
<span data-ttu-id="95860-106">**Remove-AzSubscriptionAlias** cmdlet은 구독 별칭을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="95860-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="95860-107">예제</span><span class="sxs-lookup"><span data-stu-id="95860-107">EXAMPLES</span></span>

### <span data-ttu-id="95860-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="95860-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="95860-109">구독 별칭 삭제</span><span class="sxs-lookup"><span data-stu-id="95860-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="95860-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="95860-110">PARAMETERS</span></span>

### <span data-ttu-id="95860-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="95860-111">-AliasName</span></span>
<span data-ttu-id="95860-112">구독의 별칭</span><span class="sxs-lookup"><span data-stu-id="95860-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95860-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95860-113">-AsJob</span></span>
<span data-ttu-id="95860-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="95860-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95860-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95860-115">-DefaultProfile</span></span>
<span data-ttu-id="95860-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95860-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95860-117">-확인</span><span class="sxs-lookup"><span data-stu-id="95860-117">-Confirm</span></span>
<span data-ttu-id="95860-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95860-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95860-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95860-119">-WhatIf</span></span>
<span data-ttu-id="95860-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="95860-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95860-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95860-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95860-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95860-122">CommonParameters</span></span>
<span data-ttu-id="95860-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95860-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95860-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95860-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95860-125">입력</span><span class="sxs-lookup"><span data-stu-id="95860-125">INPUTS</span></span>

### <span data-ttu-id="95860-126">없음</span><span class="sxs-lookup"><span data-stu-id="95860-126">None</span></span>

## <span data-ttu-id="95860-127">출력</span><span class="sxs-lookup"><span data-stu-id="95860-127">OUTPUTS</span></span>

### <span data-ttu-id="95860-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="95860-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="95860-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95860-129">NOTES</span></span>

## <span data-ttu-id="95860-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95860-130">RELATED LINKS</span></span>
