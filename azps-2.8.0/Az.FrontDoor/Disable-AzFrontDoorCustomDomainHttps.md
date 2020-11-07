---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 2f6b5635b029548f8d92917e0abfca18d5c0c415
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689903"
---
# <span data-ttu-id="ae895-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="ae895-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="ae895-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae895-102">SYNOPSIS</span></span>
<span data-ttu-id="ae895-103">사용자 지정 도메인에 대해 HTTPS 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="ae895-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="ae895-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae895-104">SYNTAX</span></span>

### <span data-ttu-id="ae895-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ae895-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae895-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae895-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae895-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae895-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae895-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ae895-108">DESCRIPTION</span></span>
<span data-ttu-id="ae895-109">**Disable-AzFrontDoorCustomDomainHttps** 는 사용자 지정 도메인에 대해 HTTPS를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="ae895-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ae895-110">EXAMPLES</span></span>

### <span data-ttu-id="ae895-111">예제 1: FrontDoorName 및 ResourceGroupName를 사용 하는 사용자 지정 도메인에 대해 HTTPS를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
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

<span data-ttu-id="ae895-112">"Frontendpointname1-custom-xyz" 사용자 지정 도메인에 대해 HTTPS를 사용 하지 않도록 설정 하 고 FrontDoorName "frontdoor1" 및 ResourceGroupName를 "resourcegroup1"로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="ae895-113">예제 2: PSFrontendEndpoint 개체를 사용 하는 사용자 지정 도메인에 대해 HTTPS를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
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

<span data-ttu-id="ae895-114">PSFrontendEndpoint 개체를 사용 하는 사용자 지정 도메인에 대해 HTTPS를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="ae895-115">예제 3: ResourceId를 사용 하는 사용자 지정 도메인에 대해 HTTPS를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
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

<span data-ttu-id="ae895-116">$ResourceId에 ResourceId가 있는 사용자 지정 도메인 "frontendpointname1-xyz"에 대해 HTTPS를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="ae895-117">변수</span><span class="sxs-lookup"><span data-stu-id="ae895-117">PARAMETERS</span></span>

### <span data-ttu-id="ae895-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae895-118">-DefaultProfile</span></span>
<span data-ttu-id="ae895-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae895-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ae895-120">-FrontDoorName</span></span>
<span data-ttu-id="ae895-121">앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="ae895-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="ae895-122">-FrontendEndpointName</span></span>
<span data-ttu-id="ae895-123">프런트 엔드 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="ae895-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae895-124">-InputObject</span></span>
<span data-ttu-id="ae895-125">업데이트할 프런트 엔드 끝점 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-125">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="ae895-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae895-126">-ResourceGroupName</span></span>
<span data-ttu-id="ae895-127">앞 문이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="ae895-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae895-128">-ResourceId</span></span>
<span data-ttu-id="ae895-129">Https를 사용 하지 않도록 설정 하는 프론트 도어 끝점의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="ae895-130">-확인</span><span class="sxs-lookup"><span data-stu-id="ae895-130">-Confirm</span></span>
<span data-ttu-id="ae895-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae895-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae895-132">-WhatIf</span></span>
<span data-ttu-id="ae895-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae895-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae895-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae895-135">CommonParameters</span></span>
<span data-ttu-id="ae895-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae895-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae895-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae895-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae895-138">입력</span><span class="sxs-lookup"><span data-stu-id="ae895-138">INPUTS</span></span>

### <span data-ttu-id="ae895-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ae895-139">System.String</span></span>

## <span data-ttu-id="ae895-140">출력</span><span class="sxs-lookup"><span data-stu-id="ae895-140">OUTPUTS</span></span>

### <span data-ttu-id="ae895-141">FrontDoor. PSFrontendEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="ae895-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="ae895-142">상속자</span><span class="sxs-lookup"><span data-stu-id="ae895-142">NOTES</span></span>

## <span data-ttu-id="ae895-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae895-143">RELATED LINKS</span></span>