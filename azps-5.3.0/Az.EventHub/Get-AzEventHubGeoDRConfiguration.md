---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2e324524319a2eacd24bc08aa727892ef08928c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387045"
---
# <span data-ttu-id="6d5eb-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5eb-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="6d5eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5eb-103">기본 또는 보조 네임스페이스에 대한 별칭(재해 복구 구성)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5eb-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="6d5eb-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d5eb-104">SYNTAX</span></span>

### <span data-ttu-id="6d5eb-105">GeoDRParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6d5eb-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d5eb-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6d5eb-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d5eb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d5eb-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d5eb-108">설명</span><span class="sxs-lookup"><span data-stu-id="6d5eb-108">DESCRIPTION</span></span>
<span data-ttu-id="6d5eb-109">**Get-AzEventHubGeoDRConfiguration은** 기본 또는 보조 네임스페이스에 대한 별칭(재해 복구 구성)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5eb-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="6d5eb-110">예제</span><span class="sxs-lookup"><span data-stu-id="6d5eb-110">EXAMPLES</span></span>

### <span data-ttu-id="6d5eb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d5eb-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="6d5eb-112">기본 네임스페이스 "SampleNamespace_Primary"에 대한 별칭 "SampleDRConfigName" 구성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5eb-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="6d5eb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d5eb-113">PARAMETERS</span></span>

### <span data-ttu-id="6d5eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5eb-114">-DefaultProfile</span></span>
<span data-ttu-id="6d5eb-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5eb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d5eb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5eb-116">-InputObject</span></span>
<span data-ttu-id="6d5eb-117">네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="6d5eb-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5eb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6d5eb-118">-Name</span></span>
<span data-ttu-id="6d5eb-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="6d5eb-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="6d5eb-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6d5eb-120">-Namespace</span></span>
<span data-ttu-id="6d5eb-121">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="6d5eb-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5eb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5eb-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d5eb-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6d5eb-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5eb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5eb-124">-ResourceId</span></span>
<span data-ttu-id="6d5eb-125">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6d5eb-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5eb-126">CommonParameters</span></span>
<span data-ttu-id="6d5eb-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5eb-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6d5eb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5eb-129">입력</span><span class="sxs-lookup"><span data-stu-id="6d5eb-129">INPUTS</span></span>

### <span data-ttu-id="6d5eb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6d5eb-130">System.String</span></span>

### <span data-ttu-id="6d5eb-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="6d5eb-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="6d5eb-132">출력</span><span class="sxs-lookup"><span data-stu-id="6d5eb-132">OUTPUTS</span></span>

### <span data-ttu-id="6d5eb-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6d5eb-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="6d5eb-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6d5eb-134">NOTES</span></span>

## <span data-ttu-id="6d5eb-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d5eb-135">RELATED LINKS</span></span>
