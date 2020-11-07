---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 1e844ecfbcbbbef32471c4aafe9091b1cc6dab0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699522"
---
# <span data-ttu-id="dc570-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="dc570-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="dc570-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc570-102">SYNOPSIS</span></span>
<span data-ttu-id="dc570-103">릴레이 네임 스페이스 내에서 지정 된 HybridConnection에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc570-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="dc570-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc570-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc570-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dc570-105">DESCRIPTION</span></span>
<span data-ttu-id="dc570-106">**AzRelayHybridConnection** Cmdlet은 Relay 네임 스페이스 내에서 지정 된 HybridConnection에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc570-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="dc570-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dc570-107">EXAMPLES</span></span>

### <span data-ttu-id="dc570-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc570-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="dc570-109">HybridConnection의 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc570-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="dc570-110">변수</span><span class="sxs-lookup"><span data-stu-id="dc570-110">PARAMETERS</span></span>

### <span data-ttu-id="dc570-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc570-111">-DefaultProfile</span></span>
<span data-ttu-id="dc570-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc570-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc570-113">-이름</span><span class="sxs-lookup"><span data-stu-id="dc570-113">-Name</span></span>
<span data-ttu-id="dc570-114">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc570-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc570-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dc570-115">-Namespace</span></span>
<span data-ttu-id="dc570-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc570-116">Namespace Name.</span></span>

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

### <span data-ttu-id="dc570-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc570-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc570-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc570-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc570-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc570-119">CommonParameters</span></span>
<span data-ttu-id="dc570-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc570-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc570-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc570-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc570-122">입력</span><span class="sxs-lookup"><span data-stu-id="dc570-122">INPUTS</span></span>

### <span data-ttu-id="dc570-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc570-123">System.String</span></span>

## <span data-ttu-id="dc570-124">출력</span><span class="sxs-lookup"><span data-stu-id="dc570-124">OUTPUTS</span></span>

### <span data-ttu-id="dc570-125">PSHybridConnectionAttibutes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="dc570-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>

## <span data-ttu-id="dc570-126">상속자</span><span class="sxs-lookup"><span data-stu-id="dc570-126">NOTES</span></span>

## <span data-ttu-id="dc570-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc570-127">RELATED LINKS</span></span>
