---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: dd922730f03b715924a69219c0b1f1ccb11534de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200857"
---
# <span data-ttu-id="14747-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="14747-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="14747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14747-102">SYNOPSIS</span></span>
<span data-ttu-id="14747-103">매개 변수로 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="14747-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="14747-104">구문</span><span class="sxs-lookup"><span data-stu-id="14747-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="14747-105">설명</span><span class="sxs-lookup"><span data-stu-id="14747-105">DESCRIPTION</span></span>
<span data-ttu-id="14747-106">매개 변수로 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="14747-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="14747-107">예제</span><span class="sxs-lookup"><span data-stu-id="14747-107">EXAMPLES</span></span>

### <span data-ttu-id="14747-108">예제 1: BotService 앱 폴더 다운로드</span><span class="sxs-lookup"><span data-stu-id="14747-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="14747-109">BotService 앱 폴더 다운로드</span><span class="sxs-lookup"><span data-stu-id="14747-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="14747-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14747-110">PARAMETERS</span></span>

### <span data-ttu-id="14747-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14747-111">-DefaultProfile</span></span>
<span data-ttu-id="14747-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14747-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14747-113">-Name</span><span class="sxs-lookup"><span data-stu-id="14747-113">-Name</span></span>
<span data-ttu-id="14747-114">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14747-114">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="14747-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14747-115">-ResourceGroupName</span></span>
<span data-ttu-id="14747-116">사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14747-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="14747-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="14747-117">-SavePath</span></span>


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

### <span data-ttu-id="14747-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14747-118">-SubscriptionId</span></span>
<span data-ttu-id="14747-119">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="14747-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="14747-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14747-120">CommonParameters</span></span>
<span data-ttu-id="14747-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14747-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14747-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14747-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14747-123">입력</span><span class="sxs-lookup"><span data-stu-id="14747-123">INPUTS</span></span>

## <span data-ttu-id="14747-124">출력</span><span class="sxs-lookup"><span data-stu-id="14747-124">OUTPUTS</span></span>

### <span data-ttu-id="14747-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="14747-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="14747-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14747-126">NOTES</span></span>

<span data-ttu-id="14747-127">별칭</span><span class="sxs-lookup"><span data-stu-id="14747-127">ALIASES</span></span>

## <span data-ttu-id="14747-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14747-128">RELATED LINKS</span></span>

