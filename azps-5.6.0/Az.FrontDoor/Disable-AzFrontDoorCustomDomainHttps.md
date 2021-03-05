---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: e76d4f0da95e8cc315cbbf4218a68f340b2a5e7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991167"
---
# <span data-ttu-id="d292b-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="d292b-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="d292b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d292b-102">SYNOPSIS</span></span>
<span data-ttu-id="d292b-103">사용자 지정 도메인에 대한 HTTPS 사용 안</span><span class="sxs-lookup"><span data-stu-id="d292b-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="d292b-104">구문</span><span class="sxs-lookup"><span data-stu-id="d292b-104">SYNTAX</span></span>

### <span data-ttu-id="d292b-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d292b-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d292b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d292b-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d292b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d292b-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d292b-108">설명</span><span class="sxs-lookup"><span data-stu-id="d292b-108">DESCRIPTION</span></span>
<span data-ttu-id="d292b-109">**Disable-AzFrontDoorCustomDomainHttps는** 사용자 지정 도메인에 대해 HTTPS를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="d292b-110">예제</span><span class="sxs-lookup"><span data-stu-id="d292b-110">EXAMPLES</span></span>

### <span data-ttu-id="d292b-111">예제 1: FrontDoorName 및 ResourceGroupName을 사용하여 사용자 지정 도메인에 대해 HTTPS를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="d292b-112">FrontDoorName을 "frontdoor1"로, ResourceGroupName을 "resourcegroup1"으로 사용하여 사용자 지정 도메인 "frontendpointname1-custom-xyz"에 대해 HTTPS를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="d292b-113">예제 2: PSFrontendendpoint 개체가 있는 사용자 지정 도메인에 대해 HTTPS를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Disable-AzFrontDoorCustomDomainHttps -InputObject $frontendEndpointObj 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="d292b-114">PSFrontendEndpoint 개체가 있는 사용자 지정 도메인에 대해 HTTPS를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="d292b-115">예제 3: ResourceId를 사용하여 사용자 지정 도메인에 대해 HTTPS를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="d292b-116">ResourceId를 사용하여 사용자 지정 도메인 "frontendpointname1-custom-xyz"에 대해 HTTPS를 $resourceId.</span><span class="sxs-lookup"><span data-stu-id="d292b-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="d292b-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d292b-117">PARAMETERS</span></span>

### <span data-ttu-id="d292b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d292b-118">-DefaultProfile</span></span>
<span data-ttu-id="d292b-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d292b-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="d292b-120">-FrontDoorName</span></span>
<span data-ttu-id="d292b-121">프런트 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="d292b-122">-FrontendpointName</span><span class="sxs-lookup"><span data-stu-id="d292b-122">-FrontendEndpointName</span></span>
<span data-ttu-id="d292b-123">프런트 엔드 엔드 엔드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="d292b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d292b-124">-InputObject</span></span>
<span data-ttu-id="d292b-125">업데이트할 Frontend 엔드 엔드포인트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-125">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d292b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d292b-126">-ResourceGroupName</span></span>
<span data-ttu-id="d292b-127">Front Door가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="d292b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d292b-128">-ResourceId</span></span>
<span data-ttu-id="d292b-129">https를 사용하지 않도록 설정하는 프런트 도어 엔드포인트의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d292b-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="d292b-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d292b-130">-Confirm</span></span>
<span data-ttu-id="d292b-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d292b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d292b-132">-WhatIf</span></span>
<span data-ttu-id="d292b-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d292b-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d292b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d292b-135">CommonParameters</span></span>
<span data-ttu-id="d292b-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d292b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d292b-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d292b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d292b-138">입력</span><span class="sxs-lookup"><span data-stu-id="d292b-138">INPUTS</span></span>

### <span data-ttu-id="d292b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d292b-139">System.String</span></span>

## <span data-ttu-id="d292b-140">출력</span><span class="sxs-lookup"><span data-stu-id="d292b-140">OUTPUTS</span></span>

### <span data-ttu-id="d292b-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="d292b-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="d292b-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d292b-142">NOTES</span></span>

## <span data-ttu-id="d292b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d292b-143">RELATED LINKS</span></span>
