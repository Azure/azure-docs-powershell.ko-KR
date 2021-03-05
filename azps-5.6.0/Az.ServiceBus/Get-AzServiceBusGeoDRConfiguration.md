---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 21ccb8a16ff3622e6661bd5548721d6d1227e7e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997332"
---
# <span data-ttu-id="ba217-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba217-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="ba217-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba217-102">SYNOPSIS</span></span>
<span data-ttu-id="ba217-103">기본 또는 보조 네임스페이스에 대한 별칭(재해 복구 구성)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ba217-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="ba217-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba217-104">SYNTAX</span></span>

### <span data-ttu-id="ba217-105">GeoDRPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ba217-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba217-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ba217-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba217-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba217-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba217-108">설명</span><span class="sxs-lookup"><span data-stu-id="ba217-108">DESCRIPTION</span></span>
<span data-ttu-id="ba217-109">기본 또는 보조 네임스페이스에 대한 **Get-AzServiceBusGeoDRConfiguration에서** 별칭(재해 복구 구성)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ba217-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="ba217-110">예제</span><span class="sxs-lookup"><span data-stu-id="ba217-110">EXAMPLES</span></span>

### <span data-ttu-id="ba217-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba217-111">Example 1</span></span>
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

<span data-ttu-id="ba217-112">기본 네임스페이스 "샘플DRConfigName" 구성 "SampleNamespace_Primary" 검색</span><span class="sxs-lookup"><span data-stu-id="ba217-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="ba217-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ba217-113">PARAMETERS</span></span>

### <span data-ttu-id="ba217-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba217-114">-DefaultProfile</span></span>
<span data-ttu-id="ba217-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba217-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba217-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba217-116">-InputObject</span></span>
<span data-ttu-id="ba217-117">네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="ba217-117">Namespace Object</span></span>

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

### <span data-ttu-id="ba217-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ba217-118">-Name</span></span>
<span data-ttu-id="ba217-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="ba217-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="ba217-120">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="ba217-120">-Namespace</span></span>
<span data-ttu-id="ba217-121">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="ba217-121">Namespace Name</span></span>

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

### <span data-ttu-id="ba217-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba217-122">-ResourceGroupName</span></span>
<span data-ttu-id="ba217-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ba217-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ba217-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba217-124">-ResourceId</span></span>
<span data-ttu-id="ba217-125">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ba217-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="ba217-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba217-126">CommonParameters</span></span>
<span data-ttu-id="ba217-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba217-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba217-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ba217-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba217-129">입력</span><span class="sxs-lookup"><span data-stu-id="ba217-129">INPUTS</span></span>

### <span data-ttu-id="ba217-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ba217-130">System.String</span></span>

### <span data-ttu-id="ba217-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ba217-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ba217-132">출력</span><span class="sxs-lookup"><span data-stu-id="ba217-132">OUTPUTS</span></span>

### <span data-ttu-id="ba217-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ba217-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="ba217-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba217-134">NOTES</span></span>

## <span data-ttu-id="ba217-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba217-135">RELATED LINKS</span></span>
