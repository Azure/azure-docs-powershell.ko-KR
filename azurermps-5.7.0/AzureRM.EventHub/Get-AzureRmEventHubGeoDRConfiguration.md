---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 8c48e6dc8fb095258953a57498b76219dec4ef42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534819"
---
# <span data-ttu-id="abf68-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="abf68-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="abf68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf68-102">SYNOPSIS</span></span>
<span data-ttu-id="abf68-103">Primary 또는 secondary 네임 스페이스에 대 한 별칭 (재해 복구 구성)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf68-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abf68-104">구문과</span><span class="sxs-lookup"><span data-stu-id="abf68-104">SYNTAX</span></span>

### <span data-ttu-id="abf68-105">GeoDRParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="abf68-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abf68-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="abf68-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abf68-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abf68-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abf68-108">설명은</span><span class="sxs-lookup"><span data-stu-id="abf68-108">DESCRIPTION</span></span>
<span data-ttu-id="abf68-109">**AzureRmEventHubGeoDRConfiguration** 에서 primary 또는 secondary 네임 스페이스에 대 한 별칭 (재해 복구 구성)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf68-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="abf68-110">예제의</span><span class="sxs-lookup"><span data-stu-id="abf68-110">EXAMPLES</span></span>

### <span data-ttu-id="abf68-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="abf68-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="abf68-112">기본 네임 스페이스 "SampleNamespace_Primary"에 대 한 별칭 "Sampledrcon.gif 이름" 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf68-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="abf68-113">변수</span><span class="sxs-lookup"><span data-stu-id="abf68-113">PARAMETERS</span></span>

### <span data-ttu-id="abf68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf68-114">-DefaultProfile</span></span>
<span data-ttu-id="abf68-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="abf68-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abf68-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abf68-116">-InputObject</span></span>
<span data-ttu-id="abf68-117">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="abf68-117">Namespace Object</span></span>

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

### <span data-ttu-id="abf68-118">-이름</span><span class="sxs-lookup"><span data-stu-id="abf68-118">-Name</span></span>
<span data-ttu-id="abf68-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="abf68-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf68-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="abf68-120">-Namespace</span></span>
<span data-ttu-id="abf68-121">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="abf68-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf68-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf68-122">-ResourceGroupName</span></span>
<span data-ttu-id="abf68-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="abf68-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf68-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abf68-124">-ResourceId</span></span>
<span data-ttu-id="abf68-125">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="abf68-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="abf68-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf68-126">CommonParameters</span></span>
<span data-ttu-id="abf68-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf68-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf68-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf68-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf68-129">입력</span><span class="sxs-lookup"><span data-stu-id="abf68-129">INPUTS</span></span>

### <span data-ttu-id="abf68-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="abf68-130">System.String</span></span>
<span data-ttu-id="abf68-131">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="abf68-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="abf68-132">출력</span><span class="sxs-lookup"><span data-stu-id="abf68-132">OUTPUTS</span></span>

### <span data-ttu-id="abf68-133">System.webserver. List ' 1 [[Microsoft PSEventHubDRConfigurationAttributes, Microsoft Azure. 0.5.0.0, Version =, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="abf68-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="abf68-134">상속자</span><span class="sxs-lookup"><span data-stu-id="abf68-134">NOTES</span></span>

## <span data-ttu-id="abf68-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abf68-135">RELATED LINKS</span></span>
