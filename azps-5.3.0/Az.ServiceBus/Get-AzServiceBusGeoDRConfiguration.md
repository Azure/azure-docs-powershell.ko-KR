---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494896"
---
# <span data-ttu-id="00bc4-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="00bc4-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="00bc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="00bc4-103">기본 또는 보조 네임스페이스에 대한 별칭(재해 복구 구성)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="00bc4-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="00bc4-104">구문</span><span class="sxs-lookup"><span data-stu-id="00bc4-104">SYNTAX</span></span>

### <span data-ttu-id="00bc4-105">GeoDRPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="00bc4-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00bc4-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="00bc4-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00bc4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00bc4-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00bc4-108">설명</span><span class="sxs-lookup"><span data-stu-id="00bc4-108">DESCRIPTION</span></span>
<span data-ttu-id="00bc4-109">**Get-AzServiceBusGeoDRConfiguration은** 기본 또는 보조 네임스페이스에 대한 별칭(재해 복구 구성)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="00bc4-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="00bc4-110">예제</span><span class="sxs-lookup"><span data-stu-id="00bc4-110">EXAMPLES</span></span>

### <span data-ttu-id="00bc4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="00bc4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="00bc4-112">기본 네임스페이스 "SampleNamespace_Primary"에 대한 별칭 "SampleDRConfigName" 구성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="00bc4-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="00bc4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00bc4-113">PARAMETERS</span></span>

### <span data-ttu-id="00bc4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00bc4-114">-DefaultProfile</span></span>
<span data-ttu-id="00bc4-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00bc4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00bc4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00bc4-116">-InputObject</span></span>
<span data-ttu-id="00bc4-117">네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="00bc4-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="00bc4-118">-Name</span></span>
<span data-ttu-id="00bc4-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="00bc4-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="00bc4-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="00bc4-120">-Namespace</span></span>
<span data-ttu-id="00bc4-121">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="00bc4-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00bc4-122">-ResourceGroupName</span></span>
<span data-ttu-id="00bc4-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="00bc4-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00bc4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00bc4-124">-ResourceId</span></span>
<span data-ttu-id="00bc4-125">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="00bc4-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="00bc4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bc4-126">CommonParameters</span></span>
<span data-ttu-id="00bc4-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00bc4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bc4-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="00bc4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bc4-129">입력</span><span class="sxs-lookup"><span data-stu-id="00bc4-129">INPUTS</span></span>

### <span data-ttu-id="00bc4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="00bc4-130">System.String</span></span>

### <span data-ttu-id="00bc4-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="00bc4-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="00bc4-132">출력</span><span class="sxs-lookup"><span data-stu-id="00bc4-132">OUTPUTS</span></span>

### <span data-ttu-id="00bc4-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="00bc4-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="00bc4-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00bc4-134">NOTES</span></span>

## <span data-ttu-id="00bc4-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00bc4-135">RELATED LINKS</span></span>
