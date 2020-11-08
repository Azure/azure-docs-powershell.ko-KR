---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 14f43ab66800969eb46554de898525ce8d687f5b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043211"
---
# <span data-ttu-id="a643f-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a643f-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="a643f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a643f-102">SYNOPSIS</span></span>
<span data-ttu-id="a643f-103">기존 VpnServerConfiguration를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="a643f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a643f-104">SYNTAX</span></span>

### <span data-ttu-id="a643f-105">ByVpnServerConfigurationNameByCertificateAuthentication (기본값)</span><span class="sxs-lookup"><span data-stu-id="a643f-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a643f-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a643f-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a643f-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a643f-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a643f-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="a643f-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a643f-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a643f-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a643f-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a643f-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a643f-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="a643f-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a643f-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a643f-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a643f-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a643f-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a643f-114">설명은</span><span class="sxs-lookup"><span data-stu-id="a643f-114">DESCRIPTION</span></span>
<span data-ttu-id="a643f-115">**AzVpnServerConfiguration** cmdlet을 사용 하면 다른 VpnProtocols, VpnAuthenticationTypes, VpnServerConfiguration 정책을 사용 하 여 기존를 업데이트 하 고, 사이트 연결을 위한 고객의 요구 사항에 따라 선택한 vpn 인증 유형 관련 매개 변수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="a643f-116">예제의</span><span class="sxs-lookup"><span data-stu-id="a643f-116">EXAMPLES</span></span>

### <span data-ttu-id="a643f-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="a643f-117">Example 1</span></span>
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

<span data-ttu-id="a643f-118">위의 명령을 사용 하면 IkeV2로 VpnProtocol 하는 기존 VpnServerConfiguration 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="a643f-119">변수</span><span class="sxs-lookup"><span data-stu-id="a643f-119">PARAMETERS</span></span>

### <span data-ttu-id="a643f-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="a643f-120">-AadAudience</span></span>
<span data-ttu-id="a643f-121">P2S AAD 인증을 위한 AAD 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="a643f-122">-AadIssuer</span></span>
<span data-ttu-id="a643f-123">P2S AAD 인증에 대 한 AAD 발급자입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="a643f-124">-AadTenant</span></span>
<span data-ttu-id="a643f-125">P2S AAD 인증에 대 한 AAD 테 넌 트.</span><span class="sxs-lookup"><span data-stu-id="a643f-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a643f-126">-AsJob</span></span>
<span data-ttu-id="a643f-127">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a643f-127">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a643f-128">-DefaultProfile</span></span>
<span data-ttu-id="a643f-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a643f-130">-InputObject</span></span>
<span data-ttu-id="a643f-131">수정할 vpn 서버 구성 개체</span><span class="sxs-lookup"><span data-stu-id="a643f-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-132">-이름</span><span class="sxs-lookup"><span data-stu-id="a643f-132">-Name</span></span>
<span data-ttu-id="a643f-133">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a643f-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="a643f-135">RadiusClientRootCertificate 파일 경로 목록</span><span class="sxs-lookup"><span data-stu-id="a643f-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a643f-136">-RadiusServerAddress</span></span>
<span data-ttu-id="a643f-137">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-137">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-138">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a643f-138">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="a643f-139">RadiusClientRootCertificate 파일 경로 목록</span><span class="sxs-lookup"><span data-stu-id="a643f-139">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-140">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a643f-140">-RadiusServerSecret</span></span>
<span data-ttu-id="a643f-141">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="a643f-141">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a643f-142">-ResourceGroupName</span></span>
<span data-ttu-id="a643f-143">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-143">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a643f-144">-ResourceId</span></span>
<span data-ttu-id="a643f-145">Vpn 서버 구성에 대 한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-145">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-146">태그</span><span class="sxs-lookup"><span data-stu-id="a643f-146">-Tag</span></span>
<span data-ttu-id="a643f-147">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-147">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-148">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a643f-148">-VpnAuthenticationType</span></span>
<span data-ttu-id="a643f-149">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-149">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-150">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="a643f-150">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a643f-151">VpnServerConfiguration에 대 한 IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-151">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-152">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a643f-152">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="a643f-153">파일 경로를 해지할 VpnClientCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="a643f-153">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-154">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a643f-154">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="a643f-155">추가 되는 파일 경로에 대 한 VpnClientRootCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="a643f-155">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-156">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="a643f-156">-VpnProtocol</span></span>
<span data-ttu-id="a643f-157">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-157">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-158">-확인</span><span class="sxs-lookup"><span data-stu-id="a643f-158">-Confirm</span></span>
<span data-ttu-id="a643f-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a643f-160">-WhatIf</span></span>
<span data-ttu-id="a643f-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a643f-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a643f-163">CommonParameters</span></span>
<span data-ttu-id="a643f-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a643f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a643f-165">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a643f-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a643f-166">입력</span><span class="sxs-lookup"><span data-stu-id="a643f-166">INPUTS</span></span>

### <span data-ttu-id="a643f-167">PSVpnServerConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a643f-167">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="a643f-168">PSIpsecPolicy []을 (를).</span><span class="sxs-lookup"><span data-stu-id="a643f-168">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="a643f-169">출력</span><span class="sxs-lookup"><span data-stu-id="a643f-169">OUTPUTS</span></span>

### <span data-ttu-id="a643f-170">PSVpnServerConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a643f-170">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a643f-171">상속자</span><span class="sxs-lookup"><span data-stu-id="a643f-171">NOTES</span></span>

## <span data-ttu-id="a643f-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a643f-172">RELATED LINKS</span></span>
