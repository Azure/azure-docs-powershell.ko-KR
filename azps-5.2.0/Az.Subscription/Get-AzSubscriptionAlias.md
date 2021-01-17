---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370560"
---
# <span data-ttu-id="788ef-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="788ef-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="788ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="788ef-102">SYNOPSIS</span></span>
<span data-ttu-id="788ef-103">구독 별칭 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="788ef-103">Gets subscription alias details</span></span>

## <span data-ttu-id="788ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="788ef-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="788ef-105">설명</span><span class="sxs-lookup"><span data-stu-id="788ef-105">DESCRIPTION</span></span>
<span data-ttu-id="788ef-106">**Get-AzSubscriptionAlias** cmdlet은 구독 별칭 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="788ef-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="788ef-107">예제</span><span class="sxs-lookup"><span data-stu-id="788ef-107">EXAMPLES</span></span>

### <span data-ttu-id="788ef-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="788ef-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="788ef-109">구독 별칭 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="788ef-109">Gets subscription alias details</span></span>

## <span data-ttu-id="788ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="788ef-110">PARAMETERS</span></span>

### <span data-ttu-id="788ef-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="788ef-111">-AliasName</span></span>
<span data-ttu-id="788ef-112">구독에 대한 별칭</span><span class="sxs-lookup"><span data-stu-id="788ef-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788ef-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="788ef-113">-AsJob</span></span>
<span data-ttu-id="788ef-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="788ef-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="788ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788ef-115">-DefaultProfile</span></span>
<span data-ttu-id="788ef-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="788ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="788ef-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="788ef-117">-Confirm</span></span>
<span data-ttu-id="788ef-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="788ef-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="788ef-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="788ef-119">-WhatIf</span></span>
<span data-ttu-id="788ef-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="788ef-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="788ef-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="788ef-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="788ef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788ef-122">CommonParameters</span></span>
<span data-ttu-id="788ef-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="788ef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788ef-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="788ef-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788ef-125">입력</span><span class="sxs-lookup"><span data-stu-id="788ef-125">INPUTS</span></span>

### <span data-ttu-id="788ef-126">없음</span><span class="sxs-lookup"><span data-stu-id="788ef-126">None</span></span>

## <span data-ttu-id="788ef-127">출력</span><span class="sxs-lookup"><span data-stu-id="788ef-127">OUTPUTS</span></span>

### <span data-ttu-id="788ef-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="788ef-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="788ef-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="788ef-129">NOTES</span></span>

## <span data-ttu-id="788ef-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="788ef-130">RELATED LINKS</span></span>
