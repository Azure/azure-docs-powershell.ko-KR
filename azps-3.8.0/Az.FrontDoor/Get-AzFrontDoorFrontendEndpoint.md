---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877770"
---
# <span data-ttu-id="ad61a-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad61a-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="ad61a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad61a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad61a-103">앞 도어 프런트 엔드 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad61a-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="ad61a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad61a-104">SYNTAX</span></span>

### <span data-ttu-id="ad61a-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad61a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad61a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad61a-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad61a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad61a-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad61a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ad61a-108">DESCRIPTION</span></span>
<span data-ttu-id="ad61a-109">**AzFrontDoorFrontendEndpoint** cmdlet은 제공 된 정보와 일치 하는 현재 프론트 도어 리소스의 기존 프런트 엔드 끝점을 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad61a-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="ad61a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ad61a-110">EXAMPLES</span></span>

### <span data-ttu-id="ad61a-111">예제 1: "rg1" 리소스 그룹의 일부인 앞 도어 "frontdoor1"의 모든 프론트 엔드 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad61a-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="ad61a-112">"Rg1" 리소스 그룹의 일부인 앞 도어 "frontdoor1"의 모든 프런트 엔드 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad61a-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="ad61a-113">예제 2: 이름 "frontdoor1-azurefd-net"이 리소스 그룹 "rg1"의 일부인 프론트 도어 "frontdoor1"에 있는 프런트 엔드 끝점 가져오기</span><span class="sxs-lookup"><span data-stu-id="ad61a-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1" -Name "frontdoor1-azurefd-net"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="ad61a-114">"Frontdoor1-azurefd"이 리소스 그룹 "rg1"의 일부인 프론트 도어 "frontdoor1" 인 프런트 엔드 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad61a-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="ad61a-115">변수</span><span class="sxs-lookup"><span data-stu-id="ad61a-115">PARAMETERS</span></span>

### <span data-ttu-id="ad61a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad61a-116">-DefaultProfile</span></span>
<span data-ttu-id="ad61a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad61a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad61a-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ad61a-118">-FrontDoorName</span></span>
<span data-ttu-id="ad61a-119">전방 문 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad61a-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad61a-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="ad61a-120">-FrontDoorObject</span></span>
<span data-ttu-id="ad61a-121">FrontDoor 개체</span><span class="sxs-lookup"><span data-stu-id="ad61a-121">The FrontDoor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad61a-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ad61a-122">-Name</span></span>
<span data-ttu-id="ad61a-123">프런트 엔드 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad61a-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad61a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad61a-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad61a-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad61a-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad61a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad61a-126">-ResourceId</span></span>
<span data-ttu-id="ad61a-127">앞면 도어의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ad61a-127">Resource Id of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad61a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad61a-128">CommonParameters</span></span>
<span data-ttu-id="ad61a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad61a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad61a-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad61a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad61a-131">입력</span><span class="sxs-lookup"><span data-stu-id="ad61a-131">INPUTS</span></span>

### <span data-ttu-id="ad61a-132">않아야</span><span class="sxs-lookup"><span data-stu-id="ad61a-132">None</span></span>

## <span data-ttu-id="ad61a-133">출력</span><span class="sxs-lookup"><span data-stu-id="ad61a-133">OUTPUTS</span></span>

### <span data-ttu-id="ad61a-134">FrontDoor. PSFrontendEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="ad61a-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="ad61a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ad61a-135">NOTES</span></span>

## <span data-ttu-id="ad61a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad61a-136">RELATED LINKS</span></span>
