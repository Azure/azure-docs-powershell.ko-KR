---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 118fce3e75ee7ba66fa30e6e07cfce16e5dadcff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009307"
---
# <span data-ttu-id="6a1d9-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="6a1d9-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="6a1d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="6a1d9-103">매개 변수에 의해 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a1d9-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="6a1d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a1d9-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6a1d9-105">설명</span><span class="sxs-lookup"><span data-stu-id="6a1d9-105">DESCRIPTION</span></span>
<span data-ttu-id="6a1d9-106">매개 변수에 의해 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a1d9-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="6a1d9-107">예제</span><span class="sxs-lookup"><span data-stu-id="6a1d9-107">EXAMPLES</span></span>

### <span data-ttu-id="6a1d9-108">예제 1: Project FileFolder 초기화</span><span class="sxs-lookup"><span data-stu-id="6a1d9-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="6a1d9-109">사용할 리소스 준비 초기화 및 기본 상태로 설정</span><span class="sxs-lookup"><span data-stu-id="6a1d9-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="6a1d9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6a1d9-110">PARAMETERS</span></span>

### <span data-ttu-id="6a1d9-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="6a1d9-111">-CodeDir</span></span>
<span data-ttu-id="6a1d9-112">사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a1d9-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="6a1d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a1d9-113">-DefaultProfile</span></span>
<span data-ttu-id="6a1d9-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a1d9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a1d9-115">-Language</span><span class="sxs-lookup"><span data-stu-id="6a1d9-115">-Language</span></span>


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

### <span data-ttu-id="6a1d9-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="6a1d9-116">-ProjFileName</span></span>


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

### <span data-ttu-id="6a1d9-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a1d9-117">-SubscriptionId</span></span>
<span data-ttu-id="6a1d9-118">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6a1d9-118">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a1d9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a1d9-119">CommonParameters</span></span>
<span data-ttu-id="6a1d9-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a1d9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a1d9-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a1d9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a1d9-122">입력</span><span class="sxs-lookup"><span data-stu-id="6a1d9-122">INPUTS</span></span>

## <span data-ttu-id="6a1d9-123">출력</span><span class="sxs-lookup"><span data-stu-id="6a1d9-123">OUTPUTS</span></span>

### <span data-ttu-id="6a1d9-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="6a1d9-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="6a1d9-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a1d9-125">NOTES</span></span>

<span data-ttu-id="6a1d9-126">별칭</span><span class="sxs-lookup"><span data-stu-id="6a1d9-126">ALIASES</span></span>

## <span data-ttu-id="6a1d9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a1d9-127">RELATED LINKS</span></span>

