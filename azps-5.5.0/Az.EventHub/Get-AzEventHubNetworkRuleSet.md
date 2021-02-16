---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185932"
---
# <span data-ttu-id="d06cc-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d06cc-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="d06cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d06cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d06cc-103">현재 Azure 구독에서 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d06cc-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d06cc-104">구문</span><span class="sxs-lookup"><span data-stu-id="d06cc-104">SYNTAX</span></span>

### <span data-ttu-id="d06cc-105">NetworkRuleSetPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d06cc-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d06cc-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d06cc-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d06cc-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d06cc-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d06cc-108">설명</span><span class="sxs-lookup"><span data-stu-id="d06cc-108">DESCRIPTION</span></span>
<span data-ttu-id="d06cc-109">현재 Azure 구독에서 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d06cc-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d06cc-110">예제</span><span class="sxs-lookup"><span data-stu-id="d06cc-110">EXAMPLES</span></span>

### <span data-ttu-id="d06cc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d06cc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="d06cc-112">ResourceGroup 및 네임스페이스 매개 변수를 사용하여 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d06cc-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="d06cc-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d06cc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="d06cc-114">현재 구독에 있는 네임스페이스를 사용하여 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d06cc-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="d06cc-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="d06cc-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="d06cc-116">다른 네임스페이스의 리소스 ID를 사용하여 네임스페이스의 Event Hubs NetworkruleSet 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d06cc-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="d06cc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d06cc-117">PARAMETERS</span></span>

### <span data-ttu-id="d06cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06cc-118">-DefaultProfile</span></span>
<span data-ttu-id="d06cc-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d06cc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d06cc-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d06cc-120">-Namespace</span></span>
<span data-ttu-id="d06cc-121">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="d06cc-121">Namespace Name</span></span>

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

### <span data-ttu-id="d06cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d06cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="d06cc-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d06cc-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d06cc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d06cc-124">-ResourceId</span></span>
<span data-ttu-id="d06cc-125">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d06cc-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="d06cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06cc-126">CommonParameters</span></span>
<span data-ttu-id="d06cc-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d06cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d06cc-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d06cc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06cc-129">입력</span><span class="sxs-lookup"><span data-stu-id="d06cc-129">INPUTS</span></span>

### <span data-ttu-id="d06cc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d06cc-130">System.String</span></span>

## <span data-ttu-id="d06cc-131">출력</span><span class="sxs-lookup"><span data-stu-id="d06cc-131">OUTPUTS</span></span>

### <span data-ttu-id="d06cc-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d06cc-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d06cc-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d06cc-133">NOTES</span></span>

## <span data-ttu-id="d06cc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d06cc-134">RELATED LINKS</span></span>