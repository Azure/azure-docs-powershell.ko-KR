---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: e5bd6c612cb78d2c6d38a1484452c814ecdf714c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951440"
---
# <span data-ttu-id="9a59d-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a59d-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="9a59d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a59d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a59d-103">기존 VpnServerConfiguration을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="9a59d-104">구문</span><span class="sxs-lookup"><span data-stu-id="9a59d-104">SYNTAX</span></span>

### <span data-ttu-id="9a59d-105">ByVpnServerConfigurationName(기본값)</span><span class="sxs-lookup"><span data-stu-id="9a59d-105">ByVpnServerConfigurationName (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a59d-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="9a59d-106">ByVpnServerConfigurationObject</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a59d-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="9a59d-107">ByVpnServerConfigurationResourceId</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a59d-108">설명</span><span class="sxs-lookup"><span data-stu-id="9a59d-108">DESCRIPTION</span></span>
<span data-ttu-id="9a59d-109">**Update-AzVpnServerConfiguration** cmdlet을 사용하면 다른 VpnProtocols, VpnAuthenticationTypes, IpsecPolicies로 기존 VpnServerConfiguration을 업데이트하고 사이트 연결 지점에 대한 고객의 요구 사항에 따라 선택한 VPN 인증 형식 관련 매개 변수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-109">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="9a59d-110">예제</span><span class="sxs-lookup"><span data-stu-id="9a59d-110">EXAMPLES</span></span>

### <span data-ttu-id="9a59d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a59d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2

PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2}
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

<span data-ttu-id="9a59d-112">위의 명령은 기존 VpnServerConfiguration을 IkeV2로 VpnProtocol로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-112">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="9a59d-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9a59d-113">PARAMETERS</span></span>

### <span data-ttu-id="9a59d-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="9a59d-114">-AadAudience</span></span>
<span data-ttu-id="9a59d-115">P2S AAD 인증에 대한 AAD 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="9a59d-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="9a59d-116">-AadIssuer</span></span>
<span data-ttu-id="9a59d-117">P2S AAD 인증에 대한 AAD 발급자입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="9a59d-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="9a59d-118">-AadTenant</span></span>
<span data-ttu-id="9a59d-119">P2S AAD 인증에 대한 AAD 테넌트입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="9a59d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a59d-120">-AsJob</span></span>
<span data-ttu-id="9a59d-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9a59d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a59d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a59d-122">-DefaultProfile</span></span>
<span data-ttu-id="9a59d-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a59d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a59d-124">-InputObject</span></span>
<span data-ttu-id="9a59d-125">수정할 VPN 서버 구성 개체</span><span class="sxs-lookup"><span data-stu-id="9a59d-125">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a59d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9a59d-126">-Name</span></span>
<span data-ttu-id="9a59d-127">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a59d-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="9a59d-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="9a59d-129">RadiusClientRootCertificate 파일 경로 목록</span><span class="sxs-lookup"><span data-stu-id="9a59d-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="9a59d-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="9a59d-130">-RadiusServerAddress</span></span>
<span data-ttu-id="9a59d-131">P2S 외부 반경 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="9a59d-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="9a59d-132">-RadiusServerList</span></span>
<span data-ttu-id="9a59d-133">P2S 외부 다중 반지름 서버.</span><span class="sxs-lookup"><span data-stu-id="9a59d-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="9a59d-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="9a59d-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="9a59d-135">RadiusClientRootCertificate 파일 경로 목록</span><span class="sxs-lookup"><span data-stu-id="9a59d-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="9a59d-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="9a59d-136">-RadiusServerSecret</span></span>
<span data-ttu-id="9a59d-137">P2S 외부 반경 서버 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="9a59d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a59d-138">-ResourceGroupName</span></span>
<span data-ttu-id="9a59d-139">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a59d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a59d-140">-ResourceId</span></span>
<span data-ttu-id="9a59d-141">VPN 서버 구성에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-141">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a59d-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="9a59d-142">-Tag</span></span>
<span data-ttu-id="9a59d-143">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-143">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9a59d-144">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="9a59d-144">-VpnAuthenticationType</span></span>
<span data-ttu-id="9a59d-145">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-145">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="9a59d-146">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="9a59d-146">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="9a59d-147">VpnServerConfiguration에 대한 IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-147">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a59d-148">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="9a59d-148">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="9a59d-149">해지될 VpnClientCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="9a59d-149">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="9a59d-150">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="9a59d-150">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="9a59d-151">파일 경로를 추가할 VpnClientRootCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="9a59d-151">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="9a59d-152">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="9a59d-152">-VpnProtocol</span></span>
<span data-ttu-id="9a59d-153">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-153">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="9a59d-154">-확인</span><span class="sxs-lookup"><span data-stu-id="9a59d-154">-Confirm</span></span>
<span data-ttu-id="9a59d-155">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a59d-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a59d-156">-WhatIf</span></span>
<span data-ttu-id="9a59d-157">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a59d-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a59d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a59d-159">CommonParameters</span></span>
<span data-ttu-id="9a59d-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a59d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a59d-161">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a59d-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a59d-162">입력</span><span class="sxs-lookup"><span data-stu-id="9a59d-162">INPUTS</span></span>

### <span data-ttu-id="9a59d-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a59d-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="9a59d-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="9a59d-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="9a59d-165">출력</span><span class="sxs-lookup"><span data-stu-id="9a59d-165">OUTPUTS</span></span>

### <span data-ttu-id="9a59d-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a59d-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="9a59d-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9a59d-167">NOTES</span></span>

## <span data-ttu-id="9a59d-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a59d-168">RELATED LINKS</span></span>
