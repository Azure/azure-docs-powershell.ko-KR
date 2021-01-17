---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 260cb8b605415137e9a9e667634ff02b8d4b3de7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368089"
---
# <span data-ttu-id="053b4-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="053b4-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="053b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="053b4-102">SYNOPSIS</span></span>
<span data-ttu-id="053b4-103">지정된 WcfRelay에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="053b4-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="053b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="053b4-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="053b4-105">설명</span><span class="sxs-lookup"><span data-stu-id="053b4-105">DESCRIPTION</span></span>
<span data-ttu-id="053b4-106">**Get-AzWcfRelay** cmdlet은 지정된 WcfRelay에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="053b4-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="053b4-107">예제</span><span class="sxs-lookup"><span data-stu-id="053b4-107">EXAMPLES</span></span>

### <span data-ttu-id="053b4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="053b4-108">Example 1</span></span>
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="053b4-109">WcfRelay에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="053b4-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="053b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="053b4-110">PARAMETERS</span></span>

### <span data-ttu-id="053b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="053b4-111">-DefaultProfile</span></span>
<span data-ttu-id="053b4-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="053b4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="053b4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="053b4-113">-Name</span></span>
<span data-ttu-id="053b4-114">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="053b4-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="053b4-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="053b4-115">-Namespace</span></span>
<span data-ttu-id="053b4-116">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="053b4-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="053b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="053b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="053b4-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="053b4-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="053b4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="053b4-119">CommonParameters</span></span>
<span data-ttu-id="053b4-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="053b4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="053b4-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="053b4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="053b4-122">입력</span><span class="sxs-lookup"><span data-stu-id="053b4-122">INPUTS</span></span>

### <span data-ttu-id="053b4-123">System.String</span><span class="sxs-lookup"><span data-stu-id="053b4-123">System.String</span></span>

## <span data-ttu-id="053b4-124">출력</span><span class="sxs-lookup"><span data-stu-id="053b4-124">OUTPUTS</span></span>

### <span data-ttu-id="053b4-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="053b4-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="053b4-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="053b4-126">NOTES</span></span>

## <span data-ttu-id="053b4-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="053b4-127">RELATED LINKS</span></span>
