---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: b46f346c1aa58b8c6f155ad9a742271fa121f630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202666"
---
# <span data-ttu-id="28874-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="28874-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="28874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28874-102">SYNOPSIS</span></span>
<span data-ttu-id="28874-103">지점 및 사이트 연결에 대한 새 VpnServerConfiguration을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="28874-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="28874-104">구문</span><span class="sxs-lookup"><span data-stu-id="28874-104">SYNTAX</span></span>

```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28874-105">설명</span><span class="sxs-lookup"><span data-stu-id="28874-105">DESCRIPTION</span></span>
<span data-ttu-id="28874-106">**New-AzVpnServerConfiguration** cmdlet을 사용하면 다른 VpnProtocols, VpnAuthenticationTypes, IpsecPolicies를 사용하여 새 VpnServerConfiguration을 만들고 지점 및 사이트 연결에 대한 고객의 요구 사항에 따라 선택한 VPN 인증 유형 관련 매개 변수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28874-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="28874-107">예제</span><span class="sxs-lookup"><span data-stu-id="28874-107">EXAMPLES</span></span>

### <span data-ttu-id="28874-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="28874-108">Example 1</span></span>
```powershell
PS C:\> $VpnServerConfigCertFilePath = Join-Path -Path $basedir -ChildPath "\ScenarioTests\Data\ApplicationGatewayAuthCert.cer"
PS C:\> $listOfCerts = New-Object "System.Collections.Generic.List[String]"
PS C:\> $listOfCerts.Add($VpnServerConfigCertFilePath)
PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="28874-109">위의 명령은 VpnAuthenticationType을 인증서로 사용하여 새 VpnServerConfiguration을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="28874-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="28874-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="28874-110">Example 2</span></span>

<span data-ttu-id="28874-111">지점 및 사이트 연결에 대한 새 VpnServerConfiguration을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28874-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="28874-112">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="28874-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="28874-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28874-113">PARAMETERS</span></span>

### <span data-ttu-id="28874-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="28874-114">-AadAudience</span></span>
<span data-ttu-id="28874-115">P2S AAD 인증에 대한 AAD 대상 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="28874-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="28874-116">-AadIssuer</span></span>
<span data-ttu-id="28874-117">P2S AAD 인증에 대한 AAD 발급자입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="28874-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="28874-118">-AadTenant</span></span>
<span data-ttu-id="28874-119">P2S AAD 인증을 위한 AAD 테넌트입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="28874-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28874-120">-AsJob</span></span>
<span data-ttu-id="28874-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="28874-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28874-122">-DefaultProfile</span></span>
<span data-ttu-id="28874-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28874-124">-Location</span><span class="sxs-lookup"><span data-stu-id="28874-124">-Location</span></span>
<span data-ttu-id="28874-125">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-125">The resource location.</span></span>

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

### <span data-ttu-id="28874-126">-Name</span><span class="sxs-lookup"><span data-stu-id="28874-126">-Name</span></span>
<span data-ttu-id="28874-127">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="28874-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="28874-129">RadiusClientRootCertificate 파일의 경로 목록</span><span class="sxs-lookup"><span data-stu-id="28874-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="28874-130">-RadiusServerAddress</span></span>
<span data-ttu-id="28874-131">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="28874-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="28874-132">-RadiusServerList</span></span>
<span data-ttu-id="28874-133">P2S 외부 다중 반경 서버.</span><span class="sxs-lookup"><span data-stu-id="28874-133">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="28874-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="28874-135">RadiusClientRootCertificate 파일의 경로 목록</span><span class="sxs-lookup"><span data-stu-id="28874-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="28874-136">-RadiusServerSecret</span></span>
<span data-ttu-id="28874-137">P2S 외부 Radius 서버 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-137">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28874-138">-ResourceGroupName</span></span>
<span data-ttu-id="28874-139">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-139">The resource group name.</span></span>

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

### <span data-ttu-id="28874-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="28874-140">-Tag</span></span>
<span data-ttu-id="28874-141">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="28874-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="28874-143">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-143">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="28874-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="28874-145">VpnServerConfiguration에 대한 IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28874-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="28874-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="28874-147">해지할 VpnClientCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="28874-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="28874-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="28874-149">파일 경로에 추가할 VpnClientRootCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="28874-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="28874-150">-VpnProtocol</span></span>
<span data-ttu-id="28874-151">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="28874-151">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28874-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28874-152">-Confirm</span></span>
<span data-ttu-id="28874-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="28874-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28874-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28874-154">-WhatIf</span></span>
<span data-ttu-id="28874-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="28874-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28874-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28874-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28874-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28874-157">CommonParameters</span></span>
<span data-ttu-id="28874-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28874-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28874-159">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28874-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28874-160">입력</span><span class="sxs-lookup"><span data-stu-id="28874-160">INPUTS</span></span>

### <span data-ttu-id="28874-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="28874-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="28874-162">출력</span><span class="sxs-lookup"><span data-stu-id="28874-162">OUTPUTS</span></span>

### <span data-ttu-id="28874-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="28874-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="28874-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="28874-164">NOTES</span></span>

## <span data-ttu-id="28874-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28874-165">RELATED LINKS</span></span>
