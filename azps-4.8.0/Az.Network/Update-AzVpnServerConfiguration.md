---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214769"
---
# <span data-ttu-id="78995-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="78995-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="78995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78995-102">SYNOPSIS</span></span>
<span data-ttu-id="78995-103">기존 VpnServerConfiguration를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="78995-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="78995-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78995-104">SYNTAX</span></span>

### <span data-ttu-id="78995-105">ByVpnServerConfigurationNameByCertificateAuthentication (기본값)</span><span class="sxs-lookup"><span data-stu-id="78995-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78995-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="78995-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78995-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="78995-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78995-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="78995-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78995-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="78995-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78995-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="78995-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78995-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="78995-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78995-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="78995-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78995-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="78995-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78995-114">설명은</span><span class="sxs-lookup"><span data-stu-id="78995-114">DESCRIPTION</span></span>
<span data-ttu-id="78995-115">**AzVpnServerConfiguration** cmdlet을 사용 하면 다른 VpnProtocols, VpnAuthenticationTypes, VpnServerConfiguration 정책을 사용 하 여 기존를 업데이트 하 고, 사이트 연결을 위한 고객의 요구 사항에 따라 선택한 vpn 인증 유형 관련 매개 변수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78995-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="78995-116">예제의</span><span class="sxs-lookup"><span data-stu-id="78995-116">EXAMPLES</span></span>

### <span data-ttu-id="78995-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="78995-117">Example 1</span></span>
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

<span data-ttu-id="78995-118">위의 명령을 사용 하면 IkeV2로 VpnProtocol 하는 기존 VpnServerConfiguration 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78995-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="78995-119">변수</span><span class="sxs-lookup"><span data-stu-id="78995-119">PARAMETERS</span></span>

### <span data-ttu-id="78995-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="78995-120">-AadAudience</span></span>
<span data-ttu-id="78995-121">P2S AAD 인증을 위한 AAD 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-121">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="78995-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="78995-122">-AadIssuer</span></span>
<span data-ttu-id="78995-123">P2S AAD 인증에 대 한 AAD 발급자입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-123">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="78995-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="78995-124">-AadTenant</span></span>
<span data-ttu-id="78995-125">P2S AAD 인증에 대 한 AAD 테 넌 트.</span><span class="sxs-lookup"><span data-stu-id="78995-125">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="78995-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78995-126">-AsJob</span></span>
<span data-ttu-id="78995-127">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="78995-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78995-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78995-128">-DefaultProfile</span></span>
<span data-ttu-id="78995-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78995-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78995-130">-InputObject</span></span>
<span data-ttu-id="78995-131">수정할 vpn 서버 구성 개체</span><span class="sxs-lookup"><span data-stu-id="78995-131">The vpn server configuration object to be modified</span></span>

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

### <span data-ttu-id="78995-132">-이름</span><span class="sxs-lookup"><span data-stu-id="78995-132">-Name</span></span>
<span data-ttu-id="78995-133">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-133">The resource name.</span></span>

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

### <span data-ttu-id="78995-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="78995-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="78995-135">RadiusClientRootCertificate 파일 경로 목록</span><span class="sxs-lookup"><span data-stu-id="78995-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="78995-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="78995-136">-RadiusServerAddress</span></span>
<span data-ttu-id="78995-137">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-137">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="78995-138">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="78995-138">-RadiusServerList</span></span>
<span data-ttu-id="78995-139">외부 다중 radius 서버를 P2S.</span><span class="sxs-lookup"><span data-stu-id="78995-139">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="78995-140">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="78995-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="78995-141">RadiusClientRootCertificate 파일 경로 목록</span><span class="sxs-lookup"><span data-stu-id="78995-141">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="78995-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="78995-142">-RadiusServerSecret</span></span>
<span data-ttu-id="78995-143">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="78995-143">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="78995-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78995-144">-ResourceGroupName</span></span>
<span data-ttu-id="78995-145">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-145">The resource group name.</span></span>

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

### <span data-ttu-id="78995-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78995-146">-ResourceId</span></span>
<span data-ttu-id="78995-147">Vpn 서버 구성에 대 한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-147">The Azure resource ID for the vpn server configuration.</span></span>

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

### <span data-ttu-id="78995-148">태그</span><span class="sxs-lookup"><span data-stu-id="78995-148">-Tag</span></span>
<span data-ttu-id="78995-149">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="78995-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="78995-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="78995-151">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="78995-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="78995-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="78995-153">VpnServerConfiguration에 대 한 IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="78995-154">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="78995-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="78995-155">파일 경로를 해지할 VpnClientCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="78995-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="78995-156">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="78995-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="78995-157">추가 되는 파일 경로에 대 한 VpnClientRootCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="78995-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="78995-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="78995-158">-VpnProtocol</span></span>
<span data-ttu-id="78995-159">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="78995-159">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="78995-160">-확인</span><span class="sxs-lookup"><span data-stu-id="78995-160">-Confirm</span></span>
<span data-ttu-id="78995-161">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78995-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78995-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78995-162">-WhatIf</span></span>
<span data-ttu-id="78995-163">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78995-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78995-164">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78995-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78995-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78995-165">CommonParameters</span></span>
<span data-ttu-id="78995-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78995-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78995-167">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="78995-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78995-168">입력</span><span class="sxs-lookup"><span data-stu-id="78995-168">INPUTS</span></span>

### <span data-ttu-id="78995-169">PSVpnServerConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="78995-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="78995-170">PSIpsecPolicy []을 (를).</span><span class="sxs-lookup"><span data-stu-id="78995-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="78995-171">출력</span><span class="sxs-lookup"><span data-stu-id="78995-171">OUTPUTS</span></span>

### <span data-ttu-id="78995-172">PSVpnServerConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="78995-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="78995-173">상속자</span><span class="sxs-lookup"><span data-stu-id="78995-173">NOTES</span></span>

## <span data-ttu-id="78995-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78995-174">RELATED LINKS</span></span>
