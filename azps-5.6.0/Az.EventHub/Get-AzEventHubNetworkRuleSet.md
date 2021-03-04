---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 7fa9cb54a6790a473be419dd934927ed26783d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957211"
---
# <span data-ttu-id="867be-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="867be-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="867be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="867be-102">SYNOPSIS</span></span>
<span data-ttu-id="867be-103">현재 Azure 구독에서 네임스페이스의 Event Hubs NetworkruleSet의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="867be-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="867be-104">구문</span><span class="sxs-lookup"><span data-stu-id="867be-104">SYNTAX</span></span>

### <span data-ttu-id="867be-105">NetworkRuleSetPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="867be-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="867be-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="867be-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="867be-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="867be-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="867be-108">설명</span><span class="sxs-lookup"><span data-stu-id="867be-108">DESCRIPTION</span></span>
<span data-ttu-id="867be-109">현재 Azure 구독에서 네임스페이스의 Event Hubs NetworkruleSet의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="867be-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="867be-110">예제</span><span class="sxs-lookup"><span data-stu-id="867be-110">EXAMPLES</span></span>

### <span data-ttu-id="867be-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="867be-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="867be-112">ResourceGroup 및 네임스페이스 매개 변수를 사용하여 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="867be-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="867be-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="867be-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="867be-114">현재 구독에 있는 네임스페이스를 사용하여 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="867be-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="867be-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="867be-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="867be-116">다른 네임스페이스의 리소스 ID를 사용하여 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="867be-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="867be-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="867be-117">PARAMETERS</span></span>

### <span data-ttu-id="867be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867be-118">-DefaultProfile</span></span>
<span data-ttu-id="867be-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="867be-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="867be-120">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="867be-120">-Namespace</span></span>
<span data-ttu-id="867be-121">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="867be-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867be-122">-ResourceGroupName</span></span>
<span data-ttu-id="867be-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="867be-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867be-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="867be-124">-ResourceId</span></span>
<span data-ttu-id="867be-125">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="867be-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="867be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867be-126">CommonParameters</span></span>
<span data-ttu-id="867be-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="867be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="867be-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="867be-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867be-129">입력</span><span class="sxs-lookup"><span data-stu-id="867be-129">INPUTS</span></span>

### <span data-ttu-id="867be-130">System.String</span><span class="sxs-lookup"><span data-stu-id="867be-130">System.String</span></span>

## <span data-ttu-id="867be-131">출력</span><span class="sxs-lookup"><span data-stu-id="867be-131">OUTPUTS</span></span>

### <span data-ttu-id="867be-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="867be-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="867be-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="867be-133">NOTES</span></span>

## <span data-ttu-id="867be-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="867be-134">RELATED LINKS</span></span>