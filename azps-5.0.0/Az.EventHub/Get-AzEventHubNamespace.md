---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: ba2209f7b58951bdc52976fb3cbab10fa15da98a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218684"
---
# <span data-ttu-id="7de63-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7de63-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="7de63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7de63-102">SYNOPSIS</span></span>
<span data-ttu-id="7de63-103">이벤트 허브 네임 스페이스의 세부 정보를 가져오거나 현재 Azure 구독에 있는 모든 이벤트 허브 네임 스페이스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7de63-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="7de63-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7de63-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7de63-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7de63-105">DESCRIPTION</span></span>
<span data-ttu-id="7de63-106">Get-AzEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스에 대 한 세부 정보 또는 현재 Azure 구독에서 모든 이벤트 허브 네임 스페이스의 목록 중 하나를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7de63-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="7de63-107">네임 스페이스 이름을 제공 하는 경우 단일 이벤트 허브 네임 스페이스에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7de63-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="7de63-108">네임 스페이스 이름을 제공 하지 않으면 네임 스페이스 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7de63-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="7de63-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7de63-109">EXAMPLES</span></span>

### <span data-ttu-id="7de63-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7de63-110">Example 1</span></span>
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

<span data-ttu-id="7de63-111">\` \` 리소스 그룹 MyResourceGroupName에서 네임 스페이스 MyNamespaceName의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="7de63-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7de63-112">변수</span><span class="sxs-lookup"><span data-stu-id="7de63-112">PARAMETERS</span></span>

### <span data-ttu-id="7de63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de63-113">-DefaultProfile</span></span>
<span data-ttu-id="7de63-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7de63-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7de63-115">-이름</span><span class="sxs-lookup"><span data-stu-id="7de63-115">-Name</span></span>
<span data-ttu-id="7de63-116">EventHub 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="7de63-116">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="7de63-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de63-117">-ResourceGroupName</span></span>
<span data-ttu-id="7de63-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7de63-118">Resource Group Name</span></span>

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

### <span data-ttu-id="7de63-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de63-119">CommonParameters</span></span>
<span data-ttu-id="7de63-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de63-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de63-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de63-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de63-122">입력</span><span class="sxs-lookup"><span data-stu-id="7de63-122">INPUTS</span></span>

### <span data-ttu-id="7de63-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7de63-123">System.String</span></span>

## <span data-ttu-id="7de63-124">출력</span><span class="sxs-lookup"><span data-stu-id="7de63-124">OUTPUTS</span></span>

### <span data-ttu-id="7de63-125">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="7de63-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="7de63-126">상속자</span><span class="sxs-lookup"><span data-stu-id="7de63-126">NOTES</span></span>

## <span data-ttu-id="7de63-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7de63-127">RELATED LINKS</span></span>
