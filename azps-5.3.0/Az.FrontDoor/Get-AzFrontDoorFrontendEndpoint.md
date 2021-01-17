---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489748"
---
# <span data-ttu-id="f79f5-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="f79f5-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="f79f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f79f5-102">SYNOPSIS</span></span>
<span data-ttu-id="f79f5-103">프런트 도어 프런트 엔드 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="f79f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="f79f5-104">SYNTAX</span></span>

### <span data-ttu-id="f79f5-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f79f5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f79f5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f79f5-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f79f5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f79f5-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f79f5-108">설명</span><span class="sxs-lookup"><span data-stu-id="f79f5-108">DESCRIPTION</span></span>
<span data-ttu-id="f79f5-109">**Get-AzFrontDoorFrontendEndpoint** cmdlet은 제공된 정보와 일치하는 현재 Front Door 리소스의 모든 기존 프런트 엔드 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="f79f5-110">예제</span><span class="sxs-lookup"><span data-stu-id="f79f5-110">EXAMPLES</span></span>

### <span data-ttu-id="f79f5-111">예제 1: 리소스 그룹 "rg1"의 일부인 Front Door "frontdoor1"에서 모든 프런트 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
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

<span data-ttu-id="f79f5-112">리소스 그룹 "rg1"의 일부인 Front Door "frontdoor1"에서 모든 프런트 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="f79f5-113">예제 2: 리소스 그룹 "rg1"의 일부인 Front Door "frontdoor1"에서 이름이 "frontdoor1-azurefd-net"인 프런트 엔드 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
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

<span data-ttu-id="f79f5-114">리소스 그룹 "rg1"의 일부인 Front Door "frontdoor1"에서 이름이 "frontdoor1-azurefd-net"인 프런트 엔드 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="f79f5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f79f5-115">PARAMETERS</span></span>

### <span data-ttu-id="f79f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79f5-116">-DefaultProfile</span></span>
<span data-ttu-id="f79f5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f79f5-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="f79f5-118">-FrontDoorName</span></span>
<span data-ttu-id="f79f5-119">Front Door 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-119">Front Door name.</span></span>

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

### <span data-ttu-id="f79f5-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="f79f5-120">-FrontDoorObject</span></span>
<span data-ttu-id="f79f5-121">FrontDoor 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-121">The FrontDoor object.</span></span>

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

### <span data-ttu-id="f79f5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f79f5-122">-Name</span></span>
<span data-ttu-id="f79f5-123">프런트 엔드 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="f79f5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f79f5-124">-ResourceGroupName</span></span>
<span data-ttu-id="f79f5-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-125">The resource group name.</span></span>

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

### <span data-ttu-id="f79f5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f79f5-126">-ResourceId</span></span>
<span data-ttu-id="f79f5-127">Front Door의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f79f5-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="f79f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79f5-128">CommonParameters</span></span>
<span data-ttu-id="f79f5-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f79f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79f5-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f79f5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79f5-131">입력</span><span class="sxs-lookup"><span data-stu-id="f79f5-131">INPUTS</span></span>

### <span data-ttu-id="f79f5-132">없음</span><span class="sxs-lookup"><span data-stu-id="f79f5-132">None</span></span>

## <span data-ttu-id="f79f5-133">출력</span><span class="sxs-lookup"><span data-stu-id="f79f5-133">OUTPUTS</span></span>

### <span data-ttu-id="f79f5-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="f79f5-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="f79f5-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f79f5-135">NOTES</span></span>

## <span data-ttu-id="f79f5-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f79f5-136">RELATED LINKS</span></span>
