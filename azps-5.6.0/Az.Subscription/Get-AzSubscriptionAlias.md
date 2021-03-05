---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: 0cce48f38b669c713f0d3a193deec64cfce649e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988680"
---
# <span data-ttu-id="2594a-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="2594a-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="2594a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2594a-102">SYNOPSIS</span></span>
<span data-ttu-id="2594a-103">구독 별칭 세부 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2594a-103">Gets subscription alias details</span></span>

## <span data-ttu-id="2594a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2594a-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2594a-105">설명</span><span class="sxs-lookup"><span data-stu-id="2594a-105">DESCRIPTION</span></span>
<span data-ttu-id="2594a-106">**Get-AzSubscriptionAlias** cmdlet은 구독 별칭 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2594a-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="2594a-107">예제</span><span class="sxs-lookup"><span data-stu-id="2594a-107">EXAMPLES</span></span>

### <span data-ttu-id="2594a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2594a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="2594a-109">구독 별칭 세부 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2594a-109">Gets subscription alias details</span></span>

## <span data-ttu-id="2594a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2594a-110">PARAMETERS</span></span>

### <span data-ttu-id="2594a-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="2594a-111">-AliasName</span></span>
<span data-ttu-id="2594a-112">구독의 별칭</span><span class="sxs-lookup"><span data-stu-id="2594a-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="2594a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2594a-113">-AsJob</span></span>
<span data-ttu-id="2594a-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2594a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2594a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2594a-115">-DefaultProfile</span></span>
<span data-ttu-id="2594a-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2594a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2594a-117">-확인</span><span class="sxs-lookup"><span data-stu-id="2594a-117">-Confirm</span></span>
<span data-ttu-id="2594a-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2594a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2594a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2594a-119">-WhatIf</span></span>
<span data-ttu-id="2594a-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2594a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2594a-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2594a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2594a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2594a-122">CommonParameters</span></span>
<span data-ttu-id="2594a-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2594a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2594a-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2594a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2594a-125">입력</span><span class="sxs-lookup"><span data-stu-id="2594a-125">INPUTS</span></span>

### <span data-ttu-id="2594a-126">없음</span><span class="sxs-lookup"><span data-stu-id="2594a-126">None</span></span>

## <span data-ttu-id="2594a-127">출력</span><span class="sxs-lookup"><span data-stu-id="2594a-127">OUTPUTS</span></span>

### <span data-ttu-id="2594a-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="2594a-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="2594a-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2594a-129">NOTES</span></span>

## <span data-ttu-id="2594a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2594a-130">RELATED LINKS</span></span>
