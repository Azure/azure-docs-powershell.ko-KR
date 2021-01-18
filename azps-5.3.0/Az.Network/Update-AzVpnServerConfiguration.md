---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496432"
---
# <span data-ttu-id="74a31-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="74a31-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="74a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74a31-102">SYNOPSIS</span></span>
<span data-ttu-id="74a31-103">기존 VpnServerConfiguration을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="74a31-104">구문</span><span class="sxs-lookup"><span data-stu-id="74a31-104">SYNTAX</span></span>

### <span data-ttu-id="74a31-105">ByVpnServerConfigurationNameByCertificateAuthentication(기본값)</span><span class="sxs-lookup"><span data-stu-id="74a31-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74a31-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="74a31-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74a31-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="74a31-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74a31-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="74a31-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74a31-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="74a31-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74a31-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="74a31-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74a31-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="74a31-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74a31-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="74a31-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74a31-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="74a31-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74a31-114">설명</span><span class="sxs-lookup"><span data-stu-id="74a31-114">DESCRIPTION</span></span>
<span data-ttu-id="74a31-115">**Update-AzVpnServerConfiguration** cmdlet을 사용하면 지점 및 사이트 연결에 대한 고객의 요구 사항에 따라 다른 VpnProtocols, VpnAuthenticationTypes, IpsecPolicies로 기존 VpnServerConfiguration을 업데이트하고 선택한 VPN 인증 유형 관련 매개 변수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="74a31-116">예제</span><span class="sxs-lookup"><span data-stu-id="74a31-116">EXAMPLES</span></span>

### <span data-ttu-id="74a31-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="74a31-117">Example 1</span></span>
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

<span data-ttu-id="74a31-118">위의 명령은 기존 VpnServerConfiguration을 IkeV2로 VpnProtocol로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="74a31-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74a31-119">PARAMETERS</span></span>

### <span data-ttu-id="74a31-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="74a31-120">-AadAudience</span></span>
<span data-ttu-id="74a31-121">P2S AAD 인증에 대한 AAD 대상 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="74a31-122">-AadIssuer</span></span>
<span data-ttu-id="74a31-123">P2S AAD 인증에 대한 AAD 발급자입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="74a31-124">-AadTenant</span></span>
<span data-ttu-id="74a31-125">P2S AAD 인증을 위한 AAD 테넌트입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74a31-126">-AsJob</span></span>
<span data-ttu-id="74a31-127">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="74a31-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74a31-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a31-128">-DefaultProfile</span></span>
<span data-ttu-id="74a31-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74a31-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74a31-130">-InputObject</span></span>
<span data-ttu-id="74a31-131">수정할 vpn server 구성 개체</span><span class="sxs-lookup"><span data-stu-id="74a31-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-132">-Name</span><span class="sxs-lookup"><span data-stu-id="74a31-132">-Name</span></span>
<span data-ttu-id="74a31-133">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="74a31-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="74a31-135">RadiusClientRootCertificate 파일의 경로 목록</span><span class="sxs-lookup"><span data-stu-id="74a31-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="74a31-136">-RadiusServerAddress</span></span>
<span data-ttu-id="74a31-137">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-137">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-138">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="74a31-138">-RadiusServerList</span></span>
<span data-ttu-id="74a31-139">P2S 외부 다중 반경 서버.</span><span class="sxs-lookup"><span data-stu-id="74a31-139">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-140">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="74a31-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="74a31-141">RadiusClientRootCertificate 파일의 경로 목록</span><span class="sxs-lookup"><span data-stu-id="74a31-141">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="74a31-142">-RadiusServerSecret</span></span>
<span data-ttu-id="74a31-143">P2S 외부 Radius 서버 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-143">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a31-144">-ResourceGroupName</span></span>
<span data-ttu-id="74a31-145">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74a31-146">-ResourceId</span></span>
<span data-ttu-id="74a31-147">VPN 서버 구성에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-147">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="74a31-148">-Tag</span></span>
<span data-ttu-id="74a31-149">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="74a31-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="74a31-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="74a31-151">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="74a31-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="74a31-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="74a31-153">VpnServerConfiguration에 대한 IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="74a31-154">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="74a31-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="74a31-155">해지할 VpnClientCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="74a31-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-156">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="74a31-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="74a31-157">파일 경로에 추가할 VpnClientRootCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="74a31-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a31-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="74a31-158">-VpnProtocol</span></span>
<span data-ttu-id="74a31-159">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-159">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="74a31-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74a31-160">-Confirm</span></span>
<span data-ttu-id="74a31-161">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74a31-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a31-162">-WhatIf</span></span>
<span data-ttu-id="74a31-163">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="74a31-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74a31-164">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74a31-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a31-165">CommonParameters</span></span>
<span data-ttu-id="74a31-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74a31-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a31-167">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74a31-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a31-168">입력</span><span class="sxs-lookup"><span data-stu-id="74a31-168">INPUTS</span></span>

### <span data-ttu-id="74a31-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="74a31-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="74a31-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="74a31-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="74a31-171">출력</span><span class="sxs-lookup"><span data-stu-id="74a31-171">OUTPUTS</span></span>

### <span data-ttu-id="74a31-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="74a31-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="74a31-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74a31-173">NOTES</span></span>

## <span data-ttu-id="74a31-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74a31-174">RELATED LINKS</span></span>
