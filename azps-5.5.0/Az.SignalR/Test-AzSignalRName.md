---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198641"
---
# <span data-ttu-id="b9931-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="b9931-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="b9931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9931-102">SYNOPSIS</span></span>
<span data-ttu-id="b9931-103">이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="b9931-103">Check the availability of a name.</span></span> <span data-ttu-id="b9931-104">별칭: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="b9931-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="b9931-105">구문</span><span class="sxs-lookup"><span data-stu-id="b9931-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9931-106">설명</span><span class="sxs-lookup"><span data-stu-id="b9931-106">DESCRIPTION</span></span>
<span data-ttu-id="b9931-107">이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="b9931-107">Check the availability of a name.</span></span> <span data-ttu-id="b9931-108">별칭: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="b9931-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="b9931-109">예제</span><span class="sxs-lookup"><span data-stu-id="b9931-109">EXAMPLES</span></span>

### <span data-ttu-id="b9931-110">존재하는 이름을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="b9931-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="b9931-111">없는 이름을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="b9931-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="b9931-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9931-112">PARAMETERS</span></span>

### <span data-ttu-id="b9931-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9931-113">-DefaultProfile</span></span>
<span data-ttu-id="b9931-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9931-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9931-115">-Location</span><span class="sxs-lookup"><span data-stu-id="b9931-115">-Location</span></span>
<span data-ttu-id="b9931-116">SignalR 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b9931-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="b9931-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b9931-117">-Name</span></span>
<span data-ttu-id="b9931-118">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9931-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="b9931-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9931-119">CommonParameters</span></span>
<span data-ttu-id="b9931-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9931-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9931-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b9931-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9931-122">입력</span><span class="sxs-lookup"><span data-stu-id="b9931-122">INPUTS</span></span>

### <span data-ttu-id="b9931-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b9931-123">System.String</span></span>

## <span data-ttu-id="b9931-124">출력</span><span class="sxs-lookup"><span data-stu-id="b9931-124">OUTPUTS</span></span>

### <span data-ttu-id="b9931-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9931-125">System.Boolean</span></span>

## <span data-ttu-id="b9931-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9931-126">NOTES</span></span>

## <span data-ttu-id="b9931-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9931-127">RELATED LINKS</span></span>
