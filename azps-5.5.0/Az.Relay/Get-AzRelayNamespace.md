---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: ddbc0631b6ba6a3cb55d6e91ab951d44d644e85d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206080"
---
# <span data-ttu-id="1dbac-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="1dbac-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="1dbac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbac-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbac-103">리소스 그룹 내에서 지정된 Relay 네임스페이스에 대한 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1dbac-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="1dbac-104">구문</span><span class="sxs-lookup"><span data-stu-id="1dbac-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dbac-105">설명</span><span class="sxs-lookup"><span data-stu-id="1dbac-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbac-106">**Get-AzRelayNamespace** cmdlet은 리소스 그룹 내에서 지정된 Relay 네임스페이스에 대한 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1dbac-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="1dbac-107">예제</span><span class="sxs-lookup"><span data-stu-id="1dbac-107">EXAMPLES</span></span>

### <span data-ttu-id="1dbac-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1dbac-108">Example 1</span></span>
```
PS C:\> Get-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="1dbac-109">지정된 Relay 네임스페이스에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1dbac-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="1dbac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dbac-110">PARAMETERS</span></span>

### <span data-ttu-id="1dbac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbac-111">-DefaultProfile</span></span>
<span data-ttu-id="1dbac-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dbac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbac-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1dbac-113">-Name</span></span>
<span data-ttu-id="1dbac-114">릴레이 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dbac-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbac-115">-ResourceGroupName</span></span>
<span data-ttu-id="1dbac-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dbac-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbac-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbac-117">CommonParameters</span></span>
<span data-ttu-id="1dbac-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1dbac-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbac-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1dbac-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbac-120">입력</span><span class="sxs-lookup"><span data-stu-id="1dbac-120">INPUTS</span></span>

### <span data-ttu-id="1dbac-121">System.String</span><span class="sxs-lookup"><span data-stu-id="1dbac-121">System.String</span></span>

## <span data-ttu-id="1dbac-122">출력</span><span class="sxs-lookup"><span data-stu-id="1dbac-122">OUTPUTS</span></span>

### <span data-ttu-id="1dbac-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1dbac-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="1dbac-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1dbac-124">NOTES</span></span>

## <span data-ttu-id="1dbac-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dbac-125">RELATED LINKS</span></span>
