---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 260cb8b605415137e9a9e667634ff02b8d4b3de7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048775"
---
# <span data-ttu-id="6e68f-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="6e68f-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="6e68f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e68f-102">SYNOPSIS</span></span>
<span data-ttu-id="6e68f-103">지정 된 WcfRelay에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="6e68f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e68f-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e68f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6e68f-105">DESCRIPTION</span></span>
<span data-ttu-id="6e68f-106">**AzWcfRelay** cmdlet은 지정 된 WcfRelay에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="6e68f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6e68f-107">EXAMPLES</span></span>

### <span data-ttu-id="6e68f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e68f-108">Example 1</span></span>
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

<span data-ttu-id="6e68f-109">WcfRelay의 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="6e68f-110">변수</span><span class="sxs-lookup"><span data-stu-id="6e68f-110">PARAMETERS</span></span>

### <span data-ttu-id="6e68f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e68f-111">-DefaultProfile</span></span>
<span data-ttu-id="6e68f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e68f-113">-이름</span><span class="sxs-lookup"><span data-stu-id="6e68f-113">-Name</span></span>
<span data-ttu-id="6e68f-114">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="6e68f-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e68f-115">-Namespace</span></span>
<span data-ttu-id="6e68f-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-116">Namespace Name.</span></span>

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

### <span data-ttu-id="6e68f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e68f-117">-ResourceGroupName</span></span>
<span data-ttu-id="6e68f-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="6e68f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e68f-119">CommonParameters</span></span>
<span data-ttu-id="6e68f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e68f-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e68f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e68f-122">입력</span><span class="sxs-lookup"><span data-stu-id="6e68f-122">INPUTS</span></span>

### <span data-ttu-id="6e68f-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6e68f-123">System.String</span></span>

## <span data-ttu-id="6e68f-124">출력</span><span class="sxs-lookup"><span data-stu-id="6e68f-124">OUTPUTS</span></span>

### <span data-ttu-id="6e68f-125">PSWcfRelayAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="6e68f-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="6e68f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="6e68f-126">NOTES</span></span>

## <span data-ttu-id="6e68f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e68f-127">RELATED LINKS</span></span>
