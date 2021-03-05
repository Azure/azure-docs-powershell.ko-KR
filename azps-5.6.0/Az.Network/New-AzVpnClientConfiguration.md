---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: e5dd9da25bfa2c27bd605dc80b04f8e47fb7f95b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964123"
---
# <span data-ttu-id="15fab-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="15fab-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="15fab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15fab-102">SYNOPSIS</span></span>
<span data-ttu-id="15fab-103">이 명령을 사용하면 사용자가 일부 루트 인증서와 같은 구성해야 할 수 있는 몇 가지 추가 설정 외에도 VPN 게이트웨이에서 미리 구성된 VPN 설정을 기반으로 VPN 프로필 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="15fab-104">구문</span><span class="sxs-lookup"><span data-stu-id="15fab-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15fab-105">설명</span><span class="sxs-lookup"><span data-stu-id="15fab-105">DESCRIPTION</span></span>
<span data-ttu-id="15fab-106">이렇게 하면 사용자가 일부 루트 인증서와 같은 구성해야 할 수 있는 추가 설정 외에도 VPN 게이트웨이에서 미리 구성된 VPN 설정을 기반으로 VPN 프로필 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="15fab-107">예제</span><span class="sxs-lookup"><span data-stu-id="15fab-107">EXAMPLES</span></span>

### <span data-ttu-id="15fab-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="15fab-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="15fab-109">이 cmdlet은 ResourceGroup "ContosoResourceGroup"에서 "ContosoVirtualNetworkGateway"에 대한 VPN 클라이언트 프로필 zip 파일을 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="15fab-110">프로필은 VpnProfileRadiusCert 인증서 파일을 사용하여 "EAPTLS" 인증 방법을 사용하도록 구성된 미리 구성된 반경 서버에 대해 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="15fab-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="15fab-111">PARAMETERS</span></span>

### <span data-ttu-id="15fab-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="15fab-112">-AuthenticationMethod</span></span>
<span data-ttu-id="15fab-113">인증 메서드는 EAPMSCHAPv2 또는 EAPTLS 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="15fab-114">EAPMSCHAPv2를 지정하면 cmdlet은 인증 프로토콜을 사용하는 사용자 이름/암호 인증에 대한 클라이언트 EAP-MSCHAPv2 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="15fab-115">EAPTLS를 지정한 경우 cmdlet은 EAP-TLS 프로토콜을 사용하는 인증서 인증을 위해 클라이언트 구성 설치 관리자를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="15fab-116">"EapTls" 옵션은 신뢰할 수 있는 루트를 업로드하여 Virtual Network Gateway에서 수행한 RADIUS 기반 인증서 인증 및 인증 인증에 모두 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="15fab-117">cmdlet은 구성된 것을 자동으로 감지합니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fab-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="15fab-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="15fab-119">클라이언트 루트 인증서 경로 목록</span><span class="sxs-lookup"><span data-stu-id="15fab-119">A list of client root certificate paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fab-120">-DefaultProfile</span></span>
<span data-ttu-id="15fab-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15fab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="15fab-122">-Name</span></span>
<span data-ttu-id="15fab-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fab-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="15fab-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="15fab-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="15fab-125">ProcessorArchitecture</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fab-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="15fab-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="15fab-127">Radius 서버 루트 인증서 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-127">Radius server root certificate path.</span></span> <span data-ttu-id="15fab-128">RADIUS 인증을 사용하는 EAP-TLS를 사용할 때 지정해야 하는 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="15fab-129">클라이언트가 인증하는 동안 RADIUS 서버의 유효성을 검사하는 데 사용하는 RADIUS 루트 인증서를 포함하는 .cer 파일의 전체 경로 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fab-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15fab-130">-ResourceGroupName</span></span>
<span data-ttu-id="15fab-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fab-132">-확인</span><span class="sxs-lookup"><span data-stu-id="15fab-132">-Confirm</span></span>
<span data-ttu-id="15fab-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15fab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15fab-134">-WhatIf</span></span>
<span data-ttu-id="15fab-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15fab-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15fab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fab-137">CommonParameters</span></span>
<span data-ttu-id="15fab-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="15fab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fab-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="15fab-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fab-140">입력</span><span class="sxs-lookup"><span data-stu-id="15fab-140">INPUTS</span></span>

### <span data-ttu-id="15fab-141">System.String</span><span class="sxs-lookup"><span data-stu-id="15fab-141">System.String</span></span>

### <span data-ttu-id="15fab-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="15fab-142">System.String[]</span></span>

## <span data-ttu-id="15fab-143">출력</span><span class="sxs-lookup"><span data-stu-id="15fab-143">OUTPUTS</span></span>

### <span data-ttu-id="15fab-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="15fab-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="15fab-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="15fab-145">NOTES</span></span>

## <span data-ttu-id="15fab-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15fab-146">RELATED LINKS</span></span>

[<span data-ttu-id="15fab-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="15fab-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
