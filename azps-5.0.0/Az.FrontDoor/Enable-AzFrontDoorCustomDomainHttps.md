---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219063"
---
# <span data-ttu-id="88f75-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="88f75-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="88f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88f75-102">SYNOPSIS</span></span>
<span data-ttu-id="88f75-103">전면 도어 관리 인증서를 사용 하 여 사용자 지정 도메인에 대해 HTTPS를 사용 하도록 설정 하거나 Azure 키 자격 증명 모음의 자체 인증서를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="88f75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88f75-104">SYNTAX</span></span>

### <span data-ttu-id="88f75-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="88f75-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88f75-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="88f75-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88f75-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88f75-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88f75-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="88f75-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88f75-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88f75-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88f75-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="88f75-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88f75-111">설명은</span><span class="sxs-lookup"><span data-stu-id="88f75-111">DESCRIPTION</span></span>
<span data-ttu-id="88f75-112">**AzFrontDoorCustomDomainHttps를 사용** 하면 사용자 지정 도메인에 대해 HTTPS를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="88f75-113">예제의</span><span class="sxs-lookup"><span data-stu-id="88f75-113">EXAMPLES</span></span>

### <span data-ttu-id="88f75-114">예제 1: FrontDoorName 및 ResourceGroupName를 사용 하 여 사용자 지정 도메인에 대해 HTTPS 사용 (앞면 도어 관리 됨)</span><span class="sxs-lookup"><span data-stu-id="88f75-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
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

<span data-ttu-id="88f75-115">"Frontendpointname1-custom-xyz" 사용자 지정 도메인에 대해 "resourcegroup1" 리소스 그룹에 있는 "frontdoor1"을 (를) 전면 도어 관리 되는 인증서를 사용 하 여 전면 도어 "의 일부인</span><span class="sxs-lookup"><span data-stu-id="88f75-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="88f75-116">예제 2: FrontDoorName 및 ResourceGroupName를 사용 하는 사용자 지정 도메인에 대해 HTTPS 사용 (키 자격 증명 모음에서 자체 인증서 사용)</span><span class="sxs-lookup"><span data-stu-id="88f75-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
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

<span data-ttu-id="88f75-117">"Frontendpointname1-custom-xyz" 사용자 지정 도메인에 대해 "resourcegroup1" 리소스 그룹에 있는 "frontdoor1"을 (를) 전면 도어 관리 되는 인증서를 사용 하 여 전면 도어 "의 일부인</span><span class="sxs-lookup"><span data-stu-id="88f75-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="88f75-118">예제 3: 전면 도어 관리 인증서를 사용 하 여 PSFrontendEndpoint 개체가 있는 사용자 지정 도메인에 대해 HTTPS 사용</span><span class="sxs-lookup"><span data-stu-id="88f75-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
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

<span data-ttu-id="88f75-119">프론트 도어 관리 인증서를 사용 하 여 PSFrontendEndpoint 개체가 있는 사용자 지정 도메인에 대해 HTTPS를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="88f75-120">예제 4: 전면 도어 관리 인증서를 사용 하 여 리소스 id를 가진 사용자 지정 도메인에 대해 HTTPS 사용</span><span class="sxs-lookup"><span data-stu-id="88f75-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="88f75-121">사용자 지정 도메인에 대해 HTTPS 사용 "frontendpointname1-사용자 지정-xyz"를 사용 하 여 리소스 id $resourceId에서 전면 도어 관리 된 인증서를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="88f75-122">변수</span><span class="sxs-lookup"><span data-stu-id="88f75-122">PARAMETERS</span></span>

### <span data-ttu-id="88f75-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f75-123">-DefaultProfile</span></span>
<span data-ttu-id="88f75-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88f75-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="88f75-125">-FrontDoorName</span></span>
<span data-ttu-id="88f75-126">앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="88f75-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="88f75-127">-FrontendEndpointName</span></span>
<span data-ttu-id="88f75-128">프런트 엔드 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="88f75-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88f75-129">-InputObject</span></span>
<span data-ttu-id="88f75-130">업데이트할 프런트 엔드 끝점 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="88f75-131">-없음 Tls 버전</span><span class="sxs-lookup"><span data-stu-id="88f75-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="88f75-132">클라이언트가 전면 도어를 사용 하 여 SSL 핸드셰이크를 설정 하는 데 필요한 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="88f75-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88f75-133">-ResourceGroupName</span></span>
<span data-ttu-id="88f75-134">앞 문이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-134">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="88f75-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88f75-135">-ResourceId</span></span>
<span data-ttu-id="88f75-136">Https를 사용 하도록 설정 하는 프런트 도어 끝점의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-136">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="88f75-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="88f75-137">-SecretName</span></span>
<span data-ttu-id="88f75-138">전체 인증서 PFX를 나타내는 키 보관소 비밀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="88f75-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="88f75-139">-SecretVersion</span></span>
<span data-ttu-id="88f75-140">전체 인증서 PFX를 나타내는 키 보관소 비밀의 버전</span><span class="sxs-lookup"><span data-stu-id="88f75-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="88f75-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="88f75-141">-VaultId</span></span>
<span data-ttu-id="88f75-142">SSL 인증서를 포함 하는 키 자격 증명 모음 id</span><span class="sxs-lookup"><span data-stu-id="88f75-142">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="88f75-143">-확인</span><span class="sxs-lookup"><span data-stu-id="88f75-143">-Confirm</span></span>
<span data-ttu-id="88f75-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88f75-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88f75-145">-WhatIf</span></span>
<span data-ttu-id="88f75-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88f75-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88f75-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f75-148">CommonParameters</span></span>
<span data-ttu-id="88f75-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88f75-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f75-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="88f75-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f75-151">입력</span><span class="sxs-lookup"><span data-stu-id="88f75-151">INPUTS</span></span>

### <span data-ttu-id="88f75-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88f75-152">System.String</span></span>
## <span data-ttu-id="88f75-153">출력</span><span class="sxs-lookup"><span data-stu-id="88f75-153">OUTPUTS</span></span>

### <span data-ttu-id="88f75-154">FrontDoor. PSFrontendEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="88f75-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="88f75-155">상속자</span><span class="sxs-lookup"><span data-stu-id="88f75-155">NOTES</span></span>

## <span data-ttu-id="88f75-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88f75-156">RELATED LINKS</span></span>
