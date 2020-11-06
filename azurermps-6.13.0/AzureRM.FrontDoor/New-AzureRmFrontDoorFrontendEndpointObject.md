---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 638617cfe55e01121b46c7fe283d3664948e76b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524408"
---
# <span data-ttu-id="0b621-101">New-AzureRmFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0b621-101">New-AzureRmFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="0b621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b621-102">SYNOPSIS</span></span>
<span data-ttu-id="0b621-103">전방 도어 만들기에 대 한 PSFrontendEndpoint 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0b621-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b621-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b621-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b621-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b621-105">DESCRIPTION</span></span>
<span data-ttu-id="0b621-106">전방 도어 만들기에 대 한 PSFrontendEndpoint 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0b621-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="0b621-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0b621-107">EXAMPLES</span></span>

### <span data-ttu-id="0b621-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b621-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


HostName                         : frontdoor5.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  : Shared
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
```

<span data-ttu-id="0b621-109">전방 도어 만들기에 대 한 PSFrontendEndpoint 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0b621-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="0b621-110">변수</span><span class="sxs-lookup"><span data-stu-id="0b621-110">PARAMETERS</span></span>

### <span data-ttu-id="0b621-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="0b621-111">-CertificateSource</span></span>
<span data-ttu-id="0b621-112">SSL 인증서의 원본</span><span class="sxs-lookup"><span data-stu-id="0b621-112">The source of the SSL certificate</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateSource
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, FrontDoor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="0b621-113">-CertificateType</span></span>
<span data-ttu-id="0b621-114">frontendEndpoint에 대 한 보안 연결에 사용 되는 인증서의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateType
Parameter Sets: (All)
Aliases:
Accepted values: Shared, Dedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b621-115">-DefaultProfile</span></span>
<span data-ttu-id="0b621-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="0b621-117">-HostName</span></span>
<span data-ttu-id="0b621-118">FrontendEndpoint의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="0b621-119">도메인 이름 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="0b621-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0b621-120">-Name</span></span>
<span data-ttu-id="0b621-121">프런트 엔드 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="0b621-122">ProtocolType</span><span class="sxs-lookup"><span data-stu-id="0b621-122">-ProtocolType</span></span>
<span data-ttu-id="0b621-123">보안 배달에 사용 되는 TLS 확장 프로토콜</span><span class="sxs-lookup"><span data-stu-id="0b621-123">The TLS extension protocol that is used for secure delivery</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocolType
Parameter Sets: (All)
Aliases:
Accepted values: ServerNameIndication, IPBased

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b621-124">-SecretName</span><span class="sxs-lookup"><span data-stu-id="0b621-124">-SecretName</span></span>
<span data-ttu-id="0b621-125">전체 인증서 PFX를 나타내는 키 보관소 비밀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="0b621-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="0b621-126">-SecretVersion</span></span>
<span data-ttu-id="0b621-127">전체 인증서 PFX를 나타내는 키 보관소 비밀의 버전</span><span class="sxs-lookup"><span data-stu-id="0b621-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="0b621-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="0b621-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="0b621-129">이 호스트에서 세션 선호도를 허용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="0b621-130">기본값을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="0b621-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="0b621-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="0b621-132">해당 되는 경우 세션 선호도에 대 한 시간 (초)을 사용 하는 TTL입니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="0b621-133">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-133">Default value is 0</span></span>

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

### <span data-ttu-id="0b621-134">-저장실</span><span class="sxs-lookup"><span data-stu-id="0b621-134">-Vault</span></span>
<span data-ttu-id="0b621-135">SSL 인증서를 포함 하는 키 보관소</span><span class="sxs-lookup"><span data-stu-id="0b621-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="0b621-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="0b621-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="0b621-137">각 호스트에 대 한 웹 응용 프로그램 방화벽 정책의 리소스 id (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="0b621-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="0b621-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b621-138">CommonParameters</span></span>
<span data-ttu-id="0b621-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b621-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b621-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b621-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b621-141">입력</span><span class="sxs-lookup"><span data-stu-id="0b621-141">INPUTS</span></span>

### <span data-ttu-id="0b621-142">않아야</span><span class="sxs-lookup"><span data-stu-id="0b621-142">None</span></span>

## <span data-ttu-id="0b621-143">출력</span><span class="sxs-lookup"><span data-stu-id="0b621-143">OUTPUTS</span></span>

### <span data-ttu-id="0b621-144">FrontDoor. PSFrontendEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="0b621-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="0b621-145">상속자</span><span class="sxs-lookup"><span data-stu-id="0b621-145">NOTES</span></span>

## <span data-ttu-id="0b621-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b621-146">RELATED LINKS</span></span>

<span data-ttu-id="0b621-147">[새로운 AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="0b621-147">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
