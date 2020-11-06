---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e5623ed840b9b1d2a7f75150fa686d6f488dc2ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528808"
---
# <span data-ttu-id="ba2a9-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba2a9-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="ba2a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ba2a9-103">Primary 또는 secondary 네임 스페이스에 대 한 별칭 (재해 복구 구성)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2a9-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba2a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba2a9-104">SYNTAX</span></span>

### <span data-ttu-id="ba2a9-105">Geodr속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ba2a9-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba2a9-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ba2a9-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba2a9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba2a9-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba2a9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ba2a9-108">DESCRIPTION</span></span>
<span data-ttu-id="ba2a9-109">**AzureRmServiceBusGeoDRConfiguration** 에서 primary 또는 secondary 네임 스페이스에 대 한 별칭 (재해 복구 구성)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2a9-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="ba2a9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ba2a9-110">EXAMPLES</span></span>

### <span data-ttu-id="ba2a9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba2a9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="ba2a9-112">기본 네임 스페이스 "SampleNamespace_Primary"에 대 한 별칭 "Sampledrcon.gif 이름" 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2a9-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="ba2a9-113">변수</span><span class="sxs-lookup"><span data-stu-id="ba2a9-113">PARAMETERS</span></span>

### <span data-ttu-id="ba2a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba2a9-114">-DefaultProfile</span></span>
<span data-ttu-id="ba2a9-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba2a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba2a9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba2a9-116">-InputObject</span></span>
<span data-ttu-id="ba2a9-117">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="ba2a9-117">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba2a9-118">-이름</span><span class="sxs-lookup"><span data-stu-id="ba2a9-118">-Name</span></span>
<span data-ttu-id="ba2a9-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="ba2a9-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba2a9-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ba2a9-120">-Namespace</span></span>
<span data-ttu-id="ba2a9-121">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="ba2a9-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba2a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba2a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="ba2a9-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ba2a9-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba2a9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba2a9-124">-ResourceId</span></span>
<span data-ttu-id="ba2a9-125">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ba2a9-125">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba2a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba2a9-126">CommonParameters</span></span>
<span data-ttu-id="ba2a9-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ba2a9-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba2a9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba2a9-129">입력</span><span class="sxs-lookup"><span data-stu-id="ba2a9-129">INPUTS</span></span>

### <span data-ttu-id="ba2a9-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba2a9-130">System.String</span></span>
<span data-ttu-id="ba2a9-131">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="ba2a9-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="ba2a9-132">출력</span><span class="sxs-lookup"><span data-stu-id="ba2a9-132">OUTPUTS</span></span>

### <span data-ttu-id="ba2a9-133">System.webserver. List ' 1 [[ServiceBus. ServiceBus, Version = 0.5.0.0, Culture = 중립, PublicKeyToken = null]). 목록 ' ' [[Microsoft Azure.]</span><span class="sxs-lookup"><span data-stu-id="ba2a9-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="ba2a9-134">상속자</span><span class="sxs-lookup"><span data-stu-id="ba2a9-134">NOTES</span></span>

## <span data-ttu-id="ba2a9-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba2a9-135">RELATED LINKS</span></span>
