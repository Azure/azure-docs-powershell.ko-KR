---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 9e7edf3a7aa076d7bb5ad4b1a36aecdedfd89b92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000635"
---
# <span data-ttu-id="9494d-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="9494d-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="9494d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9494d-102">SYNOPSIS</span></span>
<span data-ttu-id="9494d-103">릴레이 네임스페이스 내에서 지정된 HybridConnection에 대한 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9494d-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="9494d-104">구문</span><span class="sxs-lookup"><span data-stu-id="9494d-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9494d-105">설명</span><span class="sxs-lookup"><span data-stu-id="9494d-105">DESCRIPTION</span></span>
<span data-ttu-id="9494d-106">**Get-AzRelayHybridConnection** cmdlet은 릴레이 네임스페이스 내에서 지정된 HybridConnection에 대한 설명을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9494d-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="9494d-107">예제</span><span class="sxs-lookup"><span data-stu-id="9494d-107">EXAMPLES</span></span>

### <span data-ttu-id="9494d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9494d-108">Example 1</span></span>
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

<span data-ttu-id="9494d-109">HybridConnection에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9494d-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="9494d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9494d-110">PARAMETERS</span></span>

### <span data-ttu-id="9494d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9494d-111">-DefaultProfile</span></span>
<span data-ttu-id="9494d-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9494d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9494d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9494d-113">-Name</span></span>
<span data-ttu-id="9494d-114">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9494d-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="9494d-115">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="9494d-115">-Namespace</span></span>
<span data-ttu-id="9494d-116">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9494d-116">Namespace Name.</span></span>

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

### <span data-ttu-id="9494d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9494d-117">-ResourceGroupName</span></span>
<span data-ttu-id="9494d-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9494d-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="9494d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9494d-119">CommonParameters</span></span>
<span data-ttu-id="9494d-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9494d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9494d-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9494d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9494d-122">입력</span><span class="sxs-lookup"><span data-stu-id="9494d-122">INPUTS</span></span>

### <span data-ttu-id="9494d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9494d-123">System.String</span></span>

## <span data-ttu-id="9494d-124">출력</span><span class="sxs-lookup"><span data-stu-id="9494d-124">OUTPUTS</span></span>

### <span data-ttu-id="9494d-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="9494d-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="9494d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9494d-126">NOTES</span></span>

## <span data-ttu-id="9494d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9494d-127">RELATED LINKS</span></span>
