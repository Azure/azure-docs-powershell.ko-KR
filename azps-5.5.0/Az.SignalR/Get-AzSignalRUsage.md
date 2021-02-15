---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189036"
---
# <span data-ttu-id="c4f7b-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="c4f7b-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="c4f7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f7b-103">구독의 사용 할당량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c4f7b-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="c4f7b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4f7b-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4f7b-105">설명</span><span class="sxs-lookup"><span data-stu-id="c4f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="c4f7b-106">구독의 사용 할당량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c4f7b-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="c4f7b-107">예제</span><span class="sxs-lookup"><span data-stu-id="c4f7b-107">EXAMPLES</span></span>

### <span data-ttu-id="c4f7b-108">위치를 입력하여 사용 할당량 얻음</span><span class="sxs-lookup"><span data-stu-id="c4f7b-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="c4f7b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4f7b-109">PARAMETERS</span></span>

### <span data-ttu-id="c4f7b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f7b-110">-DefaultProfile</span></span>
<span data-ttu-id="c4f7b-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4f7b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4f7b-112">-Location</span><span class="sxs-lookup"><span data-stu-id="c4f7b-112">-Location</span></span>
<span data-ttu-id="c4f7b-113">SignalR 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c4f7b-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="c4f7b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f7b-114">CommonParameters</span></span>
<span data-ttu-id="c4f7b-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4f7b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f7b-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4f7b-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f7b-117">입력</span><span class="sxs-lookup"><span data-stu-id="c4f7b-117">INPUTS</span></span>

### <span data-ttu-id="c4f7b-118">없음</span><span class="sxs-lookup"><span data-stu-id="c4f7b-118">None</span></span>

## <span data-ttu-id="c4f7b-119">출력</span><span class="sxs-lookup"><span data-stu-id="c4f7b-119">OUTPUTS</span></span>

### <span data-ttu-id="c4f7b-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="c4f7b-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="c4f7b-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4f7b-121">NOTES</span></span>

## <span data-ttu-id="c4f7b-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4f7b-122">RELATED LINKS</span></span>
