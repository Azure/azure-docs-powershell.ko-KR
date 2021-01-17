---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367935"
---
# <span data-ttu-id="4dc44-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="4dc44-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="4dc44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc44-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc44-103">구독 별칭을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc44-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="4dc44-104">구문</span><span class="sxs-lookup"><span data-stu-id="4dc44-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dc44-105">설명</span><span class="sxs-lookup"><span data-stu-id="4dc44-105">DESCRIPTION</span></span>
<span data-ttu-id="4dc44-106">**Remove-AzSubscriptionAlias** cmdlet은 구독 별칭을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc44-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="4dc44-107">예제</span><span class="sxs-lookup"><span data-stu-id="4dc44-107">EXAMPLES</span></span>

### <span data-ttu-id="4dc44-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4dc44-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="4dc44-109">구독 별칭을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc44-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="4dc44-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dc44-110">PARAMETERS</span></span>

### <span data-ttu-id="4dc44-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="4dc44-111">-AliasName</span></span>
<span data-ttu-id="4dc44-112">구독에 대한 별칭</span><span class="sxs-lookup"><span data-stu-id="4dc44-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="4dc44-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dc44-113">-AsJob</span></span>
<span data-ttu-id="4dc44-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4dc44-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4dc44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc44-115">-DefaultProfile</span></span>
<span data-ttu-id="4dc44-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dc44-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dc44-117">-Confirm</span></span>
<span data-ttu-id="4dc44-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dc44-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc44-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc44-119">-WhatIf</span></span>
<span data-ttu-id="4dc44-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4dc44-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dc44-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dc44-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc44-122">CommonParameters</span></span>
<span data-ttu-id="4dc44-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc44-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4dc44-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc44-125">입력</span><span class="sxs-lookup"><span data-stu-id="4dc44-125">INPUTS</span></span>

### <span data-ttu-id="4dc44-126">없음</span><span class="sxs-lookup"><span data-stu-id="4dc44-126">None</span></span>

## <span data-ttu-id="4dc44-127">출력</span><span class="sxs-lookup"><span data-stu-id="4dc44-127">OUTPUTS</span></span>

### <span data-ttu-id="4dc44-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="4dc44-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="4dc44-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4dc44-129">NOTES</span></span>

## <span data-ttu-id="4dc44-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dc44-130">RELATED LINKS</span></span>
