---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 4c9d4d1a4ec79da0677bc44d53a3843aa9a6d102
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696494"
---
# <span data-ttu-id="4342c-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="4342c-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="4342c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4342c-102">SYNOPSIS</span></span>
<span data-ttu-id="4342c-103">Primary 또는 secondary 네임 스페이스에 대 한 별칭 (재해 복구 구성)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4342c-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="4342c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4342c-104">SYNTAX</span></span>

### <span data-ttu-id="4342c-105">GeoDRParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4342c-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4342c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4342c-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4342c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4342c-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4342c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4342c-108">DESCRIPTION</span></span>
<span data-ttu-id="4342c-109">**AzEventHubGeoDRConfiguration** 에서 primary 또는 secondary 네임 스페이스에 대 한 별칭 (재해 복구 구성)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4342c-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="4342c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4342c-110">EXAMPLES</span></span>

### <span data-ttu-id="4342c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4342c-111">Example 1</span></span>
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

<span data-ttu-id="4342c-112">기본 네임 스페이스 "SampleNamespace_Primary"에 대 한 별칭 "SampleDRConfigName" 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4342c-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="4342c-113">변수</span><span class="sxs-lookup"><span data-stu-id="4342c-113">PARAMETERS</span></span>

### <span data-ttu-id="4342c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4342c-114">-DefaultProfile</span></span>
<span data-ttu-id="4342c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4342c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4342c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4342c-116">-InputObject</span></span>
<span data-ttu-id="4342c-117">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="4342c-117">Namespace Object</span></span>

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

### <span data-ttu-id="4342c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4342c-118">-Name</span></span>
<span data-ttu-id="4342c-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="4342c-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="4342c-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4342c-120">-Namespace</span></span>
<span data-ttu-id="4342c-121">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="4342c-121">Namespace Name</span></span>

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

### <span data-ttu-id="4342c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4342c-122">-ResourceGroupName</span></span>
<span data-ttu-id="4342c-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4342c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4342c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4342c-124">-ResourceId</span></span>
<span data-ttu-id="4342c-125">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="4342c-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="4342c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4342c-126">CommonParameters</span></span>
<span data-ttu-id="4342c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4342c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4342c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4342c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4342c-129">입력</span><span class="sxs-lookup"><span data-stu-id="4342c-129">INPUTS</span></span>

### <span data-ttu-id="4342c-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4342c-130">System.String</span></span>

### <span data-ttu-id="4342c-131">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="4342c-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="4342c-132">출력</span><span class="sxs-lookup"><span data-stu-id="4342c-132">OUTPUTS</span></span>

### <span data-ttu-id="4342c-133">PSEventHubDRConfigurationAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="4342c-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="4342c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4342c-134">NOTES</span></span>

## <span data-ttu-id="4342c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4342c-135">RELATED LINKS</span></span>
