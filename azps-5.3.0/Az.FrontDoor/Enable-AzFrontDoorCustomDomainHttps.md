---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489751"
---
# <span data-ttu-id="d0f2e-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="d0f2e-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="d0f2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f2e-103">Front Door 관리 인증서를 사용하여 사용자 지정 도메인에 HTTPS를 사용하도록 설정하거나 Azure Key Vault에서 자체 인증서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="d0f2e-104">구문</span><span class="sxs-lookup"><span data-stu-id="d0f2e-104">SYNTAX</span></span>

### <span data-ttu-id="d0f2e-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d0f2e-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f2e-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0f2e-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0f2e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0f2e-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f2e-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0f2e-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f2e-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0f2e-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f2e-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0f2e-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f2e-111">설명</span><span class="sxs-lookup"><span data-stu-id="d0f2e-111">DESCRIPTION</span></span>
<span data-ttu-id="d0f2e-112">**Enable-AzFrontDoorCustomDomainHttps를** 사용하면 사용자 지정 도메인에 HTTPS를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="d0f2e-113">예제</span><span class="sxs-lookup"><span data-stu-id="d0f2e-113">EXAMPLES</span></span>

### <span data-ttu-id="d0f2e-114">예제 1: Front Door 관리 인증서를 사용하여 FrontDoorName 및 ResourceGroupName을 사용하여 사용자 지정 도메인에 HTTPS를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d0f2e-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -MinimumTlsVersion "1.2"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="d0f2e-115">Front Door 관리 인증서를 사용하여 리소스 그룹 "resourcegroup1"에서 Front Door "frontdoor1"의 일부인 사용자 지정 도메인 "frontendpointname1-custom-xyz"에 HTTPS를 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="d0f2e-116">예제 2: Key Vault에서 자체 인증서를 사용하여 FrontDoorName 및 ResourceGroupName을 사용하여 사용자 지정 도메인에 HTTPS를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d0f2e-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion -MinimumTlsVersion "1.0"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.0
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

<span data-ttu-id="d0f2e-117">Front Door 관리 인증서를 사용하여 리소스 그룹 "resourcegroup1"에서 Front Door "frontdoor1"의 일부인 사용자 지정 도메인 "frontendpointname1-custom-xyz"에 HTTPS를 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="d0f2e-118">예제 3: Front Door 관리 인증서를 사용하여 PSFrontendEndpoint 개체가 있는 사용자 지정 도메인에 HTTPS를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d0f2e-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -Name "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="d0f2e-119">Front Door 관리 인증서를 사용하여 PSFrontendEndpoint 개체가 있는 사용자 지정 도메인에 HTTPS를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d0f2e-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="d0f2e-120">예제 4: Front Door 관리 인증서를 사용하여 리소스 ID가 있는 사용자 지정 도메인에 HTTPS를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d0f2e-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="d0f2e-121">Front Door 관리 인증서를 사용하여 리소스 ID가 있는 사용자 지정 도메인 "frontendpointname1-custom-xyz"$resourceId HTTPS를 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="d0f2e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0f2e-122">PARAMETERS</span></span>

### <span data-ttu-id="d0f2e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f2e-123">-DefaultProfile</span></span>
<span data-ttu-id="d0f2e-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f2e-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="d0f2e-125">-FrontDoorName</span></span>
<span data-ttu-id="d0f2e-126">Front Door의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-126">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f2e-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="d0f2e-127">-FrontendEndpointName</span></span>
<span data-ttu-id="d0f2e-128">프런트 엔드 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-128">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f2e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0f2e-129">-InputObject</span></span>
<span data-ttu-id="d0f2e-130">업데이트할 프런트 엔드 엔드포인트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-130">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f2e-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d0f2e-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="d0f2e-132">클라이언트에서 Front Door로 SSL 핸드 핸드 싱크를 설정하는 데 필요한 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f2e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f2e-133">-ResourceGroupName</span></span>
<span data-ttu-id="d0f2e-134">Front Door가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-134">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f2e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0f2e-135">-ResourceId</span></span>
<span data-ttu-id="d0f2e-136">https를 사용하도록 설정하기 위한 Front Door 엔드포인트의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d0f2e-136">Resource Id of the Front Door endpoint to enable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f2e-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="d0f2e-137">-SecretName</span></span>
<span data-ttu-id="d0f2e-138">전체 인증서 PFX를 나타내는 Key Vault 비밀의 이름</span><span class="sxs-lookup"><span data-stu-id="d0f2e-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f2e-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="d0f2e-139">-SecretVersion</span></span>
<span data-ttu-id="d0f2e-140">전체 인증서 PFX를 나타내는 Key Vault 비밀의 버전</span><span class="sxs-lookup"><span data-stu-id="d0f2e-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f2e-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d0f2e-141">-VaultId</span></span>
<span data-ttu-id="d0f2e-142">SSL 인증서를 포함하는 Key Vault ID</span><span class="sxs-lookup"><span data-stu-id="d0f2e-142">The Key Vault id containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f2e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0f2e-143">-Confirm</span></span>
<span data-ttu-id="d0f2e-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f2e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f2e-145">-WhatIf</span></span>
<span data-ttu-id="d0f2e-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d0f2e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0f2e-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f2e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f2e-148">CommonParameters</span></span>
<span data-ttu-id="d0f2e-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f2e-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d0f2e-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f2e-151">입력</span><span class="sxs-lookup"><span data-stu-id="d0f2e-151">INPUTS</span></span>

### <span data-ttu-id="d0f2e-152">System.String</span><span class="sxs-lookup"><span data-stu-id="d0f2e-152">System.String</span></span>
## <span data-ttu-id="d0f2e-153">출력</span><span class="sxs-lookup"><span data-stu-id="d0f2e-153">OUTPUTS</span></span>

### <span data-ttu-id="d0f2e-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0f2e-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="d0f2e-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d0f2e-155">NOTES</span></span>

## <span data-ttu-id="d0f2e-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0f2e-156">RELATED LINKS</span></span>
