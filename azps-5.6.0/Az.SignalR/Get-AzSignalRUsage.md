---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 16d528497532f026961941963049c61a470ad188
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955488"
---
# <span data-ttu-id="c5118-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="c5118-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="c5118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5118-102">SYNOPSIS</span></span>
<span data-ttu-id="c5118-103">구독의 사용량 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5118-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="c5118-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5118-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5118-105">설명</span><span class="sxs-lookup"><span data-stu-id="c5118-105">DESCRIPTION</span></span>
<span data-ttu-id="c5118-106">구독의 사용량 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5118-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="c5118-107">예제</span><span class="sxs-lookup"><span data-stu-id="c5118-107">EXAMPLES</span></span>

### <span data-ttu-id="c5118-108">위치를 입력하여 사용량 할당량 얻음</span><span class="sxs-lookup"><span data-stu-id="c5118-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="c5118-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c5118-109">PARAMETERS</span></span>

### <span data-ttu-id="c5118-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5118-110">-DefaultProfile</span></span>
<span data-ttu-id="c5118-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5118-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5118-112">-Location</span><span class="sxs-lookup"><span data-stu-id="c5118-112">-Location</span></span>
<span data-ttu-id="c5118-113">SignalR 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c5118-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="c5118-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5118-114">CommonParameters</span></span>
<span data-ttu-id="c5118-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5118-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5118-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5118-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5118-117">입력</span><span class="sxs-lookup"><span data-stu-id="c5118-117">INPUTS</span></span>

### <span data-ttu-id="c5118-118">없음</span><span class="sxs-lookup"><span data-stu-id="c5118-118">None</span></span>

## <span data-ttu-id="c5118-119">출력</span><span class="sxs-lookup"><span data-stu-id="c5118-119">OUTPUTS</span></span>

### <span data-ttu-id="c5118-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="c5118-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="c5118-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5118-121">NOTES</span></span>

## <span data-ttu-id="c5118-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5118-122">RELATED LINKS</span></span>
