---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 97f13dc7c9a74fef3775d0aed0db9d7acfa4da43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496189"
---
# <span data-ttu-id="48be7-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="48be7-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="48be7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48be7-102">SYNOPSIS</span></span>
<span data-ttu-id="48be7-103">매개 변수로 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="48be7-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="48be7-104">구문</span><span class="sxs-lookup"><span data-stu-id="48be7-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="48be7-105">설명</span><span class="sxs-lookup"><span data-stu-id="48be7-105">DESCRIPTION</span></span>
<span data-ttu-id="48be7-106">매개 변수로 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="48be7-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="48be7-107">예제</span><span class="sxs-lookup"><span data-stu-id="48be7-107">EXAMPLES</span></span>

### <span data-ttu-id="48be7-108">예제 1: Project FileFolder 초기화</span><span class="sxs-lookup"><span data-stu-id="48be7-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="48be7-109">사용할 리소스 준비 초기화 및 기본 상태로 설정</span><span class="sxs-lookup"><span data-stu-id="48be7-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="48be7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48be7-110">PARAMETERS</span></span>

### <span data-ttu-id="48be7-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="48be7-111">-CodeDir</span></span>
<span data-ttu-id="48be7-112">사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48be7-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="48be7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48be7-113">-DefaultProfile</span></span>
<span data-ttu-id="48be7-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48be7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48be7-115">-Language</span><span class="sxs-lookup"><span data-stu-id="48be7-115">-Language</span></span>


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

### <span data-ttu-id="48be7-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="48be7-116">-ProjFileName</span></span>


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

### <span data-ttu-id="48be7-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48be7-117">-SubscriptionId</span></span>
<span data-ttu-id="48be7-118">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="48be7-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="48be7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48be7-119">CommonParameters</span></span>
<span data-ttu-id="48be7-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48be7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48be7-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48be7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48be7-122">입력</span><span class="sxs-lookup"><span data-stu-id="48be7-122">INPUTS</span></span>

## <span data-ttu-id="48be7-123">출력</span><span class="sxs-lookup"><span data-stu-id="48be7-123">OUTPUTS</span></span>

### <span data-ttu-id="48be7-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="48be7-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="48be7-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48be7-125">NOTES</span></span>

<span data-ttu-id="48be7-126">별칭</span><span class="sxs-lookup"><span data-stu-id="48be7-126">ALIASES</span></span>

## <span data-ttu-id="48be7-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48be7-127">RELATED LINKS</span></span>

