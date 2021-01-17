---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489735"
---
# <span data-ttu-id="024c3-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="024c3-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="024c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="024c3-102">SYNOPSIS</span></span>
<span data-ttu-id="024c3-103">Front Door 만들기를 위한 PSFrontendEndpoint 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="024c3-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="024c3-104">구문</span><span class="sxs-lookup"><span data-stu-id="024c3-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="024c3-105">설명</span><span class="sxs-lookup"><span data-stu-id="024c3-105">DESCRIPTION</span></span>
<span data-ttu-id="024c3-106">Front Door 만들기를 위한 PSFrontendEndpoint 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="024c3-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="024c3-107">예제</span><span class="sxs-lookup"><span data-stu-id="024c3-107">EXAMPLES</span></span>

### <span data-ttu-id="024c3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="024c3-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName "frontendendpoint1"


HostName                         : frontendendpoint1
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                :
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
ProtocolType                     : ServerNameIndication
```

<span data-ttu-id="024c3-109">Front Door를 만들기 위한 PSFrontendEndpoint 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="024c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="024c3-110">PARAMETERS</span></span>

### <span data-ttu-id="024c3-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="024c3-111">-CertificateSource</span></span>
<span data-ttu-id="024c3-112">SSL 인증서의 원본</span><span class="sxs-lookup"><span data-stu-id="024c3-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="024c3-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="024c3-113">-CertificateType</span></span>
<span data-ttu-id="024c3-114">frontendEndpoint에 대한 보안 연결에 사용되는 인증서의 형식</span><span class="sxs-lookup"><span data-stu-id="024c3-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="024c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="024c3-115">-DefaultProfile</span></span>
<span data-ttu-id="024c3-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="024c3-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="024c3-117">-HostName</span></span>
<span data-ttu-id="024c3-118">frontendEndpoint의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="024c3-119">도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-119">Must be a domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024c3-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="024c3-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="024c3-121">클라이언트에서 Front Door로 SSL 핸드 핸드 싱크를 설정하는 데 필요한 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="024c3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="024c3-122">-Name</span></span>
<span data-ttu-id="024c3-123">프런트 엔드 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024c3-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="024c3-124">-ProtocolType</span></span>
<span data-ttu-id="024c3-125">보안 배달에 사용되는 TLS 확장 프로토콜</span><span class="sxs-lookup"><span data-stu-id="024c3-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="024c3-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="024c3-126">-SecretName</span></span>
<span data-ttu-id="024c3-127">전체 인증서 PFX를 나타내는 Key Vault 비밀의 이름</span><span class="sxs-lookup"><span data-stu-id="024c3-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="024c3-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="024c3-128">-SecretVersion</span></span>
<span data-ttu-id="024c3-129">전체 인증서 PFX를 나타내는 Key Vault 비밀의 버전</span><span class="sxs-lookup"><span data-stu-id="024c3-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="024c3-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="024c3-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="024c3-131">이 호스트에서 세션 관련성을 허용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="024c3-132">기본값은 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-132">Default value is Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024c3-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="024c3-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="024c3-134">해당하는 경우 세션에 대한 효율성에 사용할 TTL(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="024c3-135">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-135">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024c3-136">-Vault</span><span class="sxs-lookup"><span data-stu-id="024c3-136">-Vault</span></span>
<span data-ttu-id="024c3-137">SSL 인증서를 포함하는 Key Vault</span><span class="sxs-lookup"><span data-stu-id="024c3-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="024c3-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="024c3-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="024c3-139">각 호스트에 대한 웹 애플리케이션 방화벽 정책의 리소스 ID(해당하는 경우)</span><span class="sxs-lookup"><span data-stu-id="024c3-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="024c3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024c3-140">CommonParameters</span></span>
<span data-ttu-id="024c3-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="024c3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024c3-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="024c3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024c3-143">입력</span><span class="sxs-lookup"><span data-stu-id="024c3-143">INPUTS</span></span>

### <span data-ttu-id="024c3-144">없음</span><span class="sxs-lookup"><span data-stu-id="024c3-144">None</span></span>
## <span data-ttu-id="024c3-145">출력</span><span class="sxs-lookup"><span data-stu-id="024c3-145">OUTPUTS</span></span>

### <span data-ttu-id="024c3-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="024c3-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="024c3-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="024c3-147">NOTES</span></span>

## <span data-ttu-id="024c3-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="024c3-148">RELATED LINKS</span></span>

<span data-ttu-id="024c3-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="024c3-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
