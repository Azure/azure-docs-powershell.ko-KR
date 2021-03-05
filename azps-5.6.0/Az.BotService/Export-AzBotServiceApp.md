---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: 79ef8a92997790f547847e05eae6ca101016bc42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960875"
---
# <span data-ttu-id="1f5f7-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="1f5f7-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="1f5f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="1f5f7-103">매개 변수에 의해 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f7-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="1f5f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f5f7-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1f5f7-105">설명</span><span class="sxs-lookup"><span data-stu-id="1f5f7-105">DESCRIPTION</span></span>
<span data-ttu-id="1f5f7-106">매개 변수에 의해 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f7-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="1f5f7-107">예제</span><span class="sxs-lookup"><span data-stu-id="1f5f7-107">EXAMPLES</span></span>

### <span data-ttu-id="1f5f7-108">예제 1: BotService 앱 폴더 다운로드</span><span class="sxs-lookup"><span data-stu-id="1f5f7-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="1f5f7-109">BotService 앱 폴더 다운로드</span><span class="sxs-lookup"><span data-stu-id="1f5f7-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="1f5f7-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1f5f7-110">PARAMETERS</span></span>

### <span data-ttu-id="1f5f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f5f7-111">-DefaultProfile</span></span>
<span data-ttu-id="1f5f7-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f5f7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1f5f7-113">-Name</span></span>
<span data-ttu-id="1f5f7-114">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f7-114">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f5f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f5f7-115">-ResourceGroupName</span></span>
<span data-ttu-id="1f5f7-116">사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f7-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="1f5f7-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="1f5f7-117">-SavePath</span></span>


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

### <span data-ttu-id="1f5f7-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f5f7-118">-SubscriptionId</span></span>
<span data-ttu-id="1f5f7-119">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f7-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1f5f7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f5f7-120">CommonParameters</span></span>
<span data-ttu-id="1f5f7-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f5f7-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f5f7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f5f7-123">입력</span><span class="sxs-lookup"><span data-stu-id="1f5f7-123">INPUTS</span></span>

## <span data-ttu-id="1f5f7-124">출력</span><span class="sxs-lookup"><span data-stu-id="1f5f7-124">OUTPUTS</span></span>

### <span data-ttu-id="1f5f7-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="1f5f7-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="1f5f7-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f5f7-126">NOTES</span></span>

<span data-ttu-id="1f5f7-127">별칭</span><span class="sxs-lookup"><span data-stu-id="1f5f7-127">ALIASES</span></span>

## <span data-ttu-id="1f5f7-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f5f7-128">RELATED LINKS</span></span>

