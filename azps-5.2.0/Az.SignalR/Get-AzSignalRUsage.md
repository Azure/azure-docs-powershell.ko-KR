---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356361"
---
# <span data-ttu-id="46654-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="46654-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="46654-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46654-102">SYNOPSIS</span></span>
<span data-ttu-id="46654-103">구독의 사용 할당량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="46654-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="46654-104">구문</span><span class="sxs-lookup"><span data-stu-id="46654-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46654-105">설명</span><span class="sxs-lookup"><span data-stu-id="46654-105">DESCRIPTION</span></span>
<span data-ttu-id="46654-106">구독의 사용 할당량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="46654-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="46654-107">예제</span><span class="sxs-lookup"><span data-stu-id="46654-107">EXAMPLES</span></span>

### <span data-ttu-id="46654-108">위치를 입력하여 사용 할당량 얻음</span><span class="sxs-lookup"><span data-stu-id="46654-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="46654-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46654-109">PARAMETERS</span></span>

### <span data-ttu-id="46654-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46654-110">-DefaultProfile</span></span>
<span data-ttu-id="46654-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46654-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46654-112">-Location</span><span class="sxs-lookup"><span data-stu-id="46654-112">-Location</span></span>
<span data-ttu-id="46654-113">SignalR 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="46654-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46654-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46654-114">CommonParameters</span></span>
<span data-ttu-id="46654-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46654-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46654-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46654-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46654-117">입력</span><span class="sxs-lookup"><span data-stu-id="46654-117">INPUTS</span></span>

### <span data-ttu-id="46654-118">없음</span><span class="sxs-lookup"><span data-stu-id="46654-118">None</span></span>

## <span data-ttu-id="46654-119">출력</span><span class="sxs-lookup"><span data-stu-id="46654-119">OUTPUTS</span></span>

### <span data-ttu-id="46654-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="46654-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="46654-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46654-121">NOTES</span></span>

## <span data-ttu-id="46654-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46654-122">RELATED LINKS</span></span>
