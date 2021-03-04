---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 01fc755564fdfd702773c31a52e13d8a95c40ede
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955360"
---
# <span data-ttu-id="7b1ef-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="7b1ef-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="7b1ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1ef-103">이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1ef-103">Check the availability of a name.</span></span> <span data-ttu-id="7b1ef-104">별칭: Test-AzSignal입니다.</span><span class="sxs-lookup"><span data-stu-id="7b1ef-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="7b1ef-105">구문</span><span class="sxs-lookup"><span data-stu-id="7b1ef-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b1ef-106">설명</span><span class="sxs-lookup"><span data-stu-id="7b1ef-106">DESCRIPTION</span></span>
<span data-ttu-id="7b1ef-107">이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1ef-107">Check the availability of a name.</span></span> <span data-ttu-id="7b1ef-108">별칭: Test-AzSignal입니다.</span><span class="sxs-lookup"><span data-stu-id="7b1ef-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="7b1ef-109">예제</span><span class="sxs-lookup"><span data-stu-id="7b1ef-109">EXAMPLES</span></span>

### <span data-ttu-id="7b1ef-110">존재하는 이름을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1ef-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="7b1ef-111">없는 이름을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1ef-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="7b1ef-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7b1ef-112">PARAMETERS</span></span>

### <span data-ttu-id="7b1ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1ef-113">-DefaultProfile</span></span>
<span data-ttu-id="7b1ef-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b1ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b1ef-115">-Location</span><span class="sxs-lookup"><span data-stu-id="7b1ef-115">-Location</span></span>
<span data-ttu-id="7b1ef-116">SignalR 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7b1ef-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b1ef-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7b1ef-117">-Name</span></span>
<span data-ttu-id="7b1ef-118">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b1ef-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="7b1ef-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1ef-119">CommonParameters</span></span>
<span data-ttu-id="7b1ef-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b1ef-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1ef-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b1ef-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1ef-122">입력</span><span class="sxs-lookup"><span data-stu-id="7b1ef-122">INPUTS</span></span>

### <span data-ttu-id="7b1ef-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7b1ef-123">System.String</span></span>

## <span data-ttu-id="7b1ef-124">출력</span><span class="sxs-lookup"><span data-stu-id="7b1ef-124">OUTPUTS</span></span>

### <span data-ttu-id="7b1ef-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b1ef-125">System.Boolean</span></span>

## <span data-ttu-id="7b1ef-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b1ef-126">NOTES</span></span>

## <span data-ttu-id="7b1ef-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b1ef-127">RELATED LINKS</span></span>
