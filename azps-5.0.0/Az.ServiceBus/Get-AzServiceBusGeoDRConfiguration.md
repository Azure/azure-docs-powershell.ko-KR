---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226663"
---
# <span data-ttu-id="2397e-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2397e-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="2397e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2397e-102">SYNOPSIS</span></span>
<span data-ttu-id="2397e-103">Primary 또는 secondary 네임 스페이스에 대 한 별칭 (재해 복구 구성)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2397e-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="2397e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2397e-104">SYNTAX</span></span>

### <span data-ttu-id="2397e-105">Geodr속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2397e-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2397e-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2397e-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2397e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2397e-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2397e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2397e-108">DESCRIPTION</span></span>
<span data-ttu-id="2397e-109">**AzServiceBusGeoDRConfiguration** 에서 primary 또는 secondary 네임 스페이스에 대 한 별칭 (재해 복구 구성)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2397e-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="2397e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2397e-110">EXAMPLES</span></span>

### <span data-ttu-id="2397e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2397e-111">Example 1</span></span>
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

<span data-ttu-id="2397e-112">기본 네임 스페이스 "SampleNamespace_Primary"에 대 한 별칭 "SampleDRConfigName" 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2397e-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="2397e-113">변수</span><span class="sxs-lookup"><span data-stu-id="2397e-113">PARAMETERS</span></span>

### <span data-ttu-id="2397e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2397e-114">-DefaultProfile</span></span>
<span data-ttu-id="2397e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2397e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2397e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2397e-116">-InputObject</span></span>
<span data-ttu-id="2397e-117">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="2397e-117">Namespace Object</span></span>

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

### <span data-ttu-id="2397e-118">-이름</span><span class="sxs-lookup"><span data-stu-id="2397e-118">-Name</span></span>
<span data-ttu-id="2397e-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="2397e-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="2397e-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2397e-120">-Namespace</span></span>
<span data-ttu-id="2397e-121">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="2397e-121">Namespace Name</span></span>

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

### <span data-ttu-id="2397e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2397e-122">-ResourceGroupName</span></span>
<span data-ttu-id="2397e-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2397e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2397e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2397e-124">-ResourceId</span></span>
<span data-ttu-id="2397e-125">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="2397e-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2397e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2397e-126">CommonParameters</span></span>
<span data-ttu-id="2397e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2397e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2397e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2397e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2397e-129">입력</span><span class="sxs-lookup"><span data-stu-id="2397e-129">INPUTS</span></span>

### <span data-ttu-id="2397e-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2397e-130">System.String</span></span>

### <span data-ttu-id="2397e-131">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="2397e-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="2397e-132">출력</span><span class="sxs-lookup"><span data-stu-id="2397e-132">OUTPUTS</span></span>

### <span data-ttu-id="2397e-133">ServiceBus. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2397e-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="2397e-134">상속자</span><span class="sxs-lookup"><span data-stu-id="2397e-134">NOTES</span></span>

## <span data-ttu-id="2397e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2397e-135">RELATED LINKS</span></span>
