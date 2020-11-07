---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: fd87311c59c0889a57cb22eb08aba855e5c3b49c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699210"
---
# <span data-ttu-id="bb633-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb633-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="bb633-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb633-102">SYNOPSIS</span></span>
<span data-ttu-id="bb633-103">Primary 또는 secondary 네임 스페이스에 대 한 별칭 (재해 복구 구성)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb633-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="bb633-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb633-104">SYNTAX</span></span>

### <span data-ttu-id="bb633-105">Geodr속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bb633-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb633-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb633-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb633-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb633-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb633-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bb633-108">DESCRIPTION</span></span>
<span data-ttu-id="bb633-109">**AzServiceBusGeoDRConfiguration** 에서 primary 또는 secondary 네임 스페이스에 대 한 별칭 (재해 복구 구성)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb633-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="bb633-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bb633-110">EXAMPLES</span></span>

### <span data-ttu-id="bb633-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb633-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="bb633-112">기본 네임 스페이스 "SampleNamespace_Primary"에 대 한 별칭 "Sampledrcon.gif 이름" 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb633-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="bb633-113">변수</span><span class="sxs-lookup"><span data-stu-id="bb633-113">PARAMETERS</span></span>

### <span data-ttu-id="bb633-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb633-114">-DefaultProfile</span></span>
<span data-ttu-id="bb633-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb633-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb633-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb633-116">-InputObject</span></span>
<span data-ttu-id="bb633-117">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="bb633-117">Namespace Object</span></span>

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

### <span data-ttu-id="bb633-118">-이름</span><span class="sxs-lookup"><span data-stu-id="bb633-118">-Name</span></span>
<span data-ttu-id="bb633-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="bb633-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="bb633-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bb633-120">-Namespace</span></span>
<span data-ttu-id="bb633-121">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="bb633-121">Namespace Name</span></span>

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

### <span data-ttu-id="bb633-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb633-122">-ResourceGroupName</span></span>
<span data-ttu-id="bb633-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bb633-123">Resource Group Name</span></span>

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

### <span data-ttu-id="bb633-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb633-124">-ResourceId</span></span>
<span data-ttu-id="bb633-125">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="bb633-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="bb633-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb633-126">CommonParameters</span></span>
<span data-ttu-id="bb633-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb633-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb633-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb633-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb633-129">입력</span><span class="sxs-lookup"><span data-stu-id="bb633-129">INPUTS</span></span>

### <span data-ttu-id="bb633-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb633-130">System.String</span></span>

### <span data-ttu-id="bb633-131">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="bb633-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="bb633-132">출력</span><span class="sxs-lookup"><span data-stu-id="bb633-132">OUTPUTS</span></span>

### <span data-ttu-id="bb633-133">ServiceBus. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="bb633-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="bb633-134">상속자</span><span class="sxs-lookup"><span data-stu-id="bb633-134">NOTES</span></span>

## <span data-ttu-id="bb633-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb633-135">RELATED LINKS</span></span>
