---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: ddbc0631b6ba6a3cb55d6e91ab951d44d644e85d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310034"
---
# <span data-ttu-id="d43a2-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="d43a2-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="d43a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d43a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d43a2-103">리소스 그룹 내에서 지정 된 릴레이 네임 스페이스에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d43a2-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="d43a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d43a2-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d43a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d43a2-105">DESCRIPTION</span></span>
<span data-ttu-id="d43a2-106">**AzRelayNamespace** cmdlet은 리소스 그룹 내의 지정 된 릴레이 네임 스페이스에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d43a2-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="d43a2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d43a2-107">EXAMPLES</span></span>

### <span data-ttu-id="d43a2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d43a2-108">Example 1</span></span>
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

<span data-ttu-id="d43a2-109">지정 된 릴레이 네임 스페이스에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d43a2-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="d43a2-110">변수</span><span class="sxs-lookup"><span data-stu-id="d43a2-110">PARAMETERS</span></span>

### <span data-ttu-id="d43a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43a2-111">-DefaultProfile</span></span>
<span data-ttu-id="d43a2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d43a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d43a2-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d43a2-113">-Name</span></span>
<span data-ttu-id="d43a2-114">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d43a2-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="d43a2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d43a2-115">-ResourceGroupName</span></span>
<span data-ttu-id="d43a2-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d43a2-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="d43a2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43a2-117">CommonParameters</span></span>
<span data-ttu-id="d43a2-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d43a2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43a2-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d43a2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43a2-120">입력</span><span class="sxs-lookup"><span data-stu-id="d43a2-120">INPUTS</span></span>

### <span data-ttu-id="d43a2-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d43a2-121">System.String</span></span>

## <span data-ttu-id="d43a2-122">출력</span><span class="sxs-lookup"><span data-stu-id="d43a2-122">OUTPUTS</span></span>

### <span data-ttu-id="d43a2-123">PSRelayNamespaceAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="d43a2-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="d43a2-124">상속자</span><span class="sxs-lookup"><span data-stu-id="d43a2-124">NOTES</span></span>

## <span data-ttu-id="d43a2-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d43a2-125">RELATED LINKS</span></span>
