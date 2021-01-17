---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: ba2209f7b58951bdc52976fb3cbab10fa15da98a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387038"
---
# <span data-ttu-id="bfc2d-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="bfc2d-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="bfc2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc2d-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc2d-103">Event Hubs 네임스페이스의 세부 정보를 얻거나 현재 Azure 구독의 모든 Event Hubs 네임스페이스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="bfc2d-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfc2d-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfc2d-105">설명</span><span class="sxs-lookup"><span data-stu-id="bfc2d-105">DESCRIPTION</span></span>
<span data-ttu-id="bfc2d-106">Get-AzEventHubNamespace cmdlet은 지정된 Event Hubs 네임스페이스의 세부 정보 또는 현재 Azure 구독의 모든 Event Hubs 네임스페이스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="bfc2d-107">네임스페이스 이름이 제공된 경우 단일 Event Hubs 네임스페이스의 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="bfc2d-108">네임스페이스 이름이 제공되지 않은 경우 네임스페이스 목록이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="bfc2d-109">예제</span><span class="sxs-lookup"><span data-stu-id="bfc2d-109">EXAMPLES</span></span>

### <span data-ttu-id="bfc2d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bfc2d-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="bfc2d-111">리소스 그룹 \` \` \` MyResourceGroupName에서 MyNamespaceName 네임스페이스의 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="bfc2d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfc2d-112">PARAMETERS</span></span>

### <span data-ttu-id="bfc2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc2d-113">-DefaultProfile</span></span>
<span data-ttu-id="bfc2d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfc2d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bfc2d-115">-Name</span></span>
<span data-ttu-id="bfc2d-116">EventHub 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="bfc2d-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc2d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc2d-117">-ResourceGroupName</span></span>
<span data-ttu-id="bfc2d-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bfc2d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="bfc2d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc2d-119">CommonParameters</span></span>
<span data-ttu-id="bfc2d-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc2d-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc2d-122">입력</span><span class="sxs-lookup"><span data-stu-id="bfc2d-122">INPUTS</span></span>

### <span data-ttu-id="bfc2d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="bfc2d-123">System.String</span></span>

## <span data-ttu-id="bfc2d-124">출력</span><span class="sxs-lookup"><span data-stu-id="bfc2d-124">OUTPUTS</span></span>

### <span data-ttu-id="bfc2d-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bfc2d-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="bfc2d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfc2d-126">NOTES</span></span>

## <span data-ttu-id="bfc2d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfc2d-127">RELATED LINKS</span></span>
