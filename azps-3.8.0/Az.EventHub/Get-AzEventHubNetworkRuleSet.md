---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041872"
---
# <span data-ttu-id="206b4-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="206b4-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="206b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="206b4-102">SYNOPSIS</span></span>
<span data-ttu-id="206b4-103">현재 Azure 구독에서 네임 스페이스의 이벤트 허브 네트워크 규칙 집합에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="206b4-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="206b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="206b4-104">SYNTAX</span></span>

### <span data-ttu-id="206b4-105">Networkruleset속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="206b4-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="206b4-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="206b4-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="206b4-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="206b4-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="206b4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="206b4-108">DESCRIPTION</span></span>
<span data-ttu-id="206b4-109">현재 Azure 구독에서 네임 스페이스의 이벤트 허브 네트워크 규칙 집합에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="206b4-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="206b4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="206b4-110">EXAMPLES</span></span>

### <span data-ttu-id="206b4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="206b4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="206b4-112">ResourceGroup 및 Namespace 매개 변수를 사용 하 여 네임 스페이스의 이벤트 허브 네트워크 규칙 집합에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="206b4-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="206b4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="206b4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="206b4-114">현재 구독에 있는 네임 스페이스를 사용 하 여 네임 스페이스의 이벤트 허브 네트워크 규칙 집합에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="206b4-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="206b4-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="206b4-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="206b4-116">다른 네임 스페이스의 리소스 Id를 사용 하 여 네임 스페이스의 이벤트 허브 네트워크 규칙 집합에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="206b4-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="206b4-117">변수</span><span class="sxs-lookup"><span data-stu-id="206b4-117">PARAMETERS</span></span>

### <span data-ttu-id="206b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="206b4-118">-DefaultProfile</span></span>
<span data-ttu-id="206b4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="206b4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="206b4-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="206b4-120">-Namespace</span></span>
<span data-ttu-id="206b4-121">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="206b4-121">Namespace Name</span></span>

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

### <span data-ttu-id="206b4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="206b4-122">-ResourceGroupName</span></span>
<span data-ttu-id="206b4-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="206b4-123">Resource Group Name</span></span>

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

### <span data-ttu-id="206b4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="206b4-124">-ResourceId</span></span>
<span data-ttu-id="206b4-125">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="206b4-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="206b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="206b4-126">CommonParameters</span></span>
<span data-ttu-id="206b4-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="206b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="206b4-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="206b4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="206b4-129">입력</span><span class="sxs-lookup"><span data-stu-id="206b4-129">INPUTS</span></span>

### <span data-ttu-id="206b4-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="206b4-130">System.String</span></span>

## <span data-ttu-id="206b4-131">출력</span><span class="sxs-lookup"><span data-stu-id="206b4-131">OUTPUTS</span></span>

### <span data-ttu-id="206b4-132">Microsoft. \*. a. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="206b4-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="206b4-133">상속자</span><span class="sxs-lookup"><span data-stu-id="206b4-133">NOTES</span></span>

## <span data-ttu-id="206b4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="206b4-134">RELATED LINKS</span></span>