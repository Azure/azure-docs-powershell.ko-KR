---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: de0806585cee16eed19291766ab29696a9a1b960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878930"
---
# <span data-ttu-id="f1cb1-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1cb1-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="f1cb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cb1-103">사이트 연결을 위한 새 VpnServerConfiguration를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="f1cb1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1cb1-104">SYNTAX</span></span>

### <span data-ttu-id="f1cb1-105">ByVpnServerConfigurationNameByCertificateAuthentication (기본값)</span><span class="sxs-lookup"><span data-stu-id="f1cb1-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1cb1-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="f1cb1-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1cb1-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="f1cb1-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1cb1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f1cb1-108">DESCRIPTION</span></span>
<span data-ttu-id="f1cb1-109">**AzVpnServerConfiguration** cmdlet을 사용 하면 다른 VpnProtocols, VpnAuthenticationTypes, 정책 가능 정책을 사용 하 여 새 VpnServerConfiguration를 만들고, 선택 된 vpn 인증 유형 관련 매개 변수를 사이트 연결 지점의 고객 요구 사항에 따라 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="f1cb1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f1cb1-110">EXAMPLES</span></span>

### <span data-ttu-id="f1cb1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1cb1-111">Example 1</span></span>
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

<span data-ttu-id="f1cb1-112">위의 명령을 사용 하면 VpnAuthenticationType 인증서로 새 VpnServerConfiguration 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

## <span data-ttu-id="f1cb1-113">변수</span><span class="sxs-lookup"><span data-stu-id="f1cb1-113">PARAMETERS</span></span>

### <span data-ttu-id="f1cb1-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="f1cb1-114">-AadAudience</span></span>
<span data-ttu-id="f1cb1-115">P2S AAD 인증을 위한 AAD 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="f1cb1-116">-AadIssuer</span></span>
<span data-ttu-id="f1cb1-117">P2S AAD 인증에 대 한 AAD 발급자입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="f1cb1-118">-AadTenant</span></span>
<span data-ttu-id="f1cb1-119">P2S AAD 인증에 대 한 AAD 테 넌 트.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1cb1-120">-AsJob</span></span>
<span data-ttu-id="f1cb1-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f1cb1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1cb1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cb1-122">-DefaultProfile</span></span>
<span data-ttu-id="f1cb1-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1cb1-124">-위치</span><span class="sxs-lookup"><span data-stu-id="f1cb1-124">-Location</span></span>
<span data-ttu-id="f1cb1-125">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-125">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-126">-이름</span><span class="sxs-lookup"><span data-stu-id="f1cb1-126">-Name</span></span>
<span data-ttu-id="f1cb1-127">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="f1cb1-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="f1cb1-129">RadiusClientRootCertificate 파일 경로 목록</span><span class="sxs-lookup"><span data-stu-id="f1cb1-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="f1cb1-130">-RadiusServerAddress</span></span>
<span data-ttu-id="f1cb1-131">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-131">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-132">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="f1cb1-132">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="f1cb1-133">RadiusClientRootCertificate 파일 경로 목록</span><span class="sxs-lookup"><span data-stu-id="f1cb1-133">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-134">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="f1cb1-134">-RadiusServerSecret</span></span>
<span data-ttu-id="f1cb1-135">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-135">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1cb1-136">-ResourceGroupName</span></span>
<span data-ttu-id="f1cb1-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-138">태그</span><span class="sxs-lookup"><span data-stu-id="f1cb1-138">-Tag</span></span>
<span data-ttu-id="f1cb1-139">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f1cb1-140">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f1cb1-140">-VpnAuthenticationType</span></span>
<span data-ttu-id="f1cb1-141">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-141">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="f1cb1-142">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f1cb1-142">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="f1cb1-143">VpnServerConfiguration에 대 한 IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-143">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-144">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="f1cb1-144">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="f1cb1-145">파일 경로를 해지할 VpnClientCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="f1cb1-145">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-146">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="f1cb1-146">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="f1cb1-147">추가 되는 파일 경로에 대 한 VpnClientRootCertificates 목록</span><span class="sxs-lookup"><span data-stu-id="f1cb1-147">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cb1-148">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="f1cb1-148">-VpnProtocol</span></span>
<span data-ttu-id="f1cb1-149">P2S VPN 클라이언트 터널링 프로토콜 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-149">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="f1cb1-150">-확인</span><span class="sxs-lookup"><span data-stu-id="f1cb1-150">-Confirm</span></span>
<span data-ttu-id="f1cb1-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1cb1-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1cb1-152">-WhatIf</span></span>
<span data-ttu-id="f1cb1-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1cb1-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1cb1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cb1-155">CommonParameters</span></span>
<span data-ttu-id="f1cb1-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cb1-157">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1cb1-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cb1-158">입력</span><span class="sxs-lookup"><span data-stu-id="f1cb1-158">INPUTS</span></span>

### <span data-ttu-id="f1cb1-159">PSIpsecPolicy [] (으)로</span><span class="sxs-lookup"><span data-stu-id="f1cb1-159">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="f1cb1-160">출력</span><span class="sxs-lookup"><span data-stu-id="f1cb1-160">OUTPUTS</span></span>

### <span data-ttu-id="f1cb1-161">PSVpnServerConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f1cb1-161">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="f1cb1-162">상속자</span><span class="sxs-lookup"><span data-stu-id="f1cb1-162">NOTES</span></span>

## <span data-ttu-id="f1cb1-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1cb1-163">RELATED LINKS</span></span>
