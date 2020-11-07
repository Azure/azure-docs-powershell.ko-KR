---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877730"
---
# <span data-ttu-id="f0132-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="f0132-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="f0132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0132-102">SYNOPSIS</span></span>
<span data-ttu-id="f0132-103">전방 도어 만들기에 대 한 PSFrontendEndpoint 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="f0132-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="f0132-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0132-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0132-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f0132-105">DESCRIPTION</span></span>
<span data-ttu-id="f0132-106">전방 도어 만들기에 대 한 PSFrontendEndpoint 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="f0132-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="f0132-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f0132-107">EXAMPLES</span></span>

### <span data-ttu-id="f0132-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0132-108">Example 1</span></span>
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

<span data-ttu-id="f0132-109">전방 도어 만들기에 대 한 PSFrontendEndpoint 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="f0132-110">변수</span><span class="sxs-lookup"><span data-stu-id="f0132-110">PARAMETERS</span></span>

### <span data-ttu-id="f0132-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="f0132-111">-CertificateSource</span></span>
<span data-ttu-id="f0132-112">SSL 인증서의 원본</span><span class="sxs-lookup"><span data-stu-id="f0132-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="f0132-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="f0132-113">-CertificateType</span></span>
<span data-ttu-id="f0132-114">frontendEndpoint에 대 한 보안 연결에 사용 되는 인증서의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="f0132-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0132-115">-DefaultProfile</span></span>
<span data-ttu-id="f0132-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0132-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="f0132-117">-HostName</span></span>
<span data-ttu-id="f0132-118">FrontendEndpoint의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="f0132-119">도메인 이름 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="f0132-120">-없음 Tls 버전</span><span class="sxs-lookup"><span data-stu-id="f0132-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="f0132-121">클라이언트가 전면 도어를 사용 하 여 SSL 핸드셰이크를 설정 하는 데 필요한 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="f0132-122">-이름</span><span class="sxs-lookup"><span data-stu-id="f0132-122">-Name</span></span>
<span data-ttu-id="f0132-123">프런트 엔드 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="f0132-124">ProtocolType</span><span class="sxs-lookup"><span data-stu-id="f0132-124">-ProtocolType</span></span>
<span data-ttu-id="f0132-125">보안 배달에 사용 되는 TLS 확장 프로토콜</span><span class="sxs-lookup"><span data-stu-id="f0132-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="f0132-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="f0132-126">-SecretName</span></span>
<span data-ttu-id="f0132-127">전체 인증서 PFX를 나타내는 키 보관소 비밀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="f0132-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="f0132-128">-SecretVersion</span></span>
<span data-ttu-id="f0132-129">전체 인증서 PFX를 나타내는 키 보관소 비밀의 버전</span><span class="sxs-lookup"><span data-stu-id="f0132-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="f0132-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="f0132-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="f0132-131">이 호스트에서 세션 선호도를 허용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="f0132-132">기본값을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="f0132-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f0132-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="f0132-134">해당 되는 경우 세션 선호도에 대 한 시간 (초)을 사용 하는 TTL입니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="f0132-135">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-135">Default value is 0</span></span>

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

### <span data-ttu-id="f0132-136">-저장실</span><span class="sxs-lookup"><span data-stu-id="f0132-136">-Vault</span></span>
<span data-ttu-id="f0132-137">SSL 인증서를 포함 하는 키 보관소</span><span class="sxs-lookup"><span data-stu-id="f0132-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="f0132-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="f0132-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="f0132-139">각 호스트에 대 한 웹 응용 프로그램 방화벽 정책의 리소스 id (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="f0132-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="f0132-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0132-140">CommonParameters</span></span>
<span data-ttu-id="f0132-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0132-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0132-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0132-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0132-143">입력</span><span class="sxs-lookup"><span data-stu-id="f0132-143">INPUTS</span></span>

### <span data-ttu-id="f0132-144">않아야</span><span class="sxs-lookup"><span data-stu-id="f0132-144">None</span></span>
## <span data-ttu-id="f0132-145">출력</span><span class="sxs-lookup"><span data-stu-id="f0132-145">OUTPUTS</span></span>

### <span data-ttu-id="f0132-146">FrontDoor. PSFrontendEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="f0132-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="f0132-147">상속자</span><span class="sxs-lookup"><span data-stu-id="f0132-147">NOTES</span></span>

## <span data-ttu-id="f0132-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0132-148">RELATED LINKS</span></span>

<span data-ttu-id="f0132-149">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="f0132-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
