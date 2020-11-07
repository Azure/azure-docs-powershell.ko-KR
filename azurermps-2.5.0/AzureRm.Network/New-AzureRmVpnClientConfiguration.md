---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientconfiguration
schema: 2.0.0
ms.openlocfilehash: d49078e18b6082473c398c9f4aa7ac01f41909ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882186"
---
# <span data-ttu-id="bc24e-101">New-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc24e-101">New-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="bc24e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc24e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc24e-103">이 명령을 사용 하 여 사용자는 VPN 게이트웨이에서 미리 구성 된 vpn 설정을 기반으로 Vpn 프로필 패키지를 만들 수 있으며, 예를 들어 일부 루트 인증서와 같이 사용자가 구성 해야 하는 일부 추가 설정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc24e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc24e-104">SYNTAX</span></span>

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc24e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bc24e-105">DESCRIPTION</span></span>
<span data-ttu-id="bc24e-106">이렇게 하면 사용자가 VPN 게이트웨이에서 미리 구성 된 vpn 설정을 기반으로 Vpn 프로필 패키지를 만들 수 있으며, 예를 들어 일부 루트 인증서와 같이 사용자가 구성 해야 하는 일부 추가 설정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="bc24e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bc24e-107">EXAMPLES</span></span>

### <span data-ttu-id="bc24e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bc24e-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="bc24e-109">이 cmdlet은 ResourceGroup "ContosoResourceGroup"의 "ContosoVirtualNetworkGateway"에 대 한 VPN 클라이언트 프로필 zip 파일을 만드는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="bc24e-110">VpnProfileRadiusCert 인증서 파일과 함께 "EAPTLS" 인증 방법을 사용 하도록 구성 된 미리 구성 된 radius 서버에 대해 프로필이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="bc24e-111">변수</span><span class="sxs-lookup"><span data-stu-id="bc24e-111">PARAMETERS</span></span>

### <span data-ttu-id="bc24e-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="bc24e-112">-AuthenticationMethod</span></span>
<span data-ttu-id="bc24e-113">인증 방법에서는 값 EAPMSCHAPv2 또는 EAPTLS를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="bc24e-114">EAPMSCHAPv2가 지정 되 면 cmdlet은 EAP-MSCHAPv2 인증 프로토콜을 사용 하는 사용자 이름/암호 인증에 대 한 클라이언트 구성 설치 관리자를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="bc24e-115">EAPTLS가 지정 된 경우 cmdlet은 EAP-TLS 프로토콜을 사용 하는 인증서 인증을 위한 클라이언트 구성 설치 관리자를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="bc24e-116">"EapTls" 옵션은 신뢰할 수 있는 루트를 업로드 하 여 가상 네트워크 게이트웨이에서 수행 하는 RADIUS 기반 인증서 인증과 인증 인증 모두에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="bc24e-117">Cmdlet은 구성 된 항목을 자동으로 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24e-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="bc24e-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="bc24e-119">클라이언트 루트 인증서 경로 목록</span><span class="sxs-lookup"><span data-stu-id="bc24e-119">A list of client root certificate paths</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc24e-120">-DefaultProfile</span></span>
<span data-ttu-id="bc24e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="bc24e-122">-Name</span></span>
<span data-ttu-id="bc24e-123">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24e-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="bc24e-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="bc24e-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="bc24e-125">ProcessorArchitecture</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24e-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="bc24e-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="bc24e-127">Radius 서버 루트 인증서 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-127">Radius server root certificate path.</span></span> <span data-ttu-id="bc24e-128">이 매개 변수는 RADIUS 인증을 사용한 EAP-TLS를 사용 하는 경우에 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="bc24e-129">클라이언트가 인증 하는 동안 RADIUS 서버의 유효성을 검사 하는 데 사용 하는 RADIUS 루트 인증서를 포함 하는 .cer 파일의 전체 경로 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc24e-130">-ResourceGroupName</span></span>
<span data-ttu-id="bc24e-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24e-132">-확인</span><span class="sxs-lookup"><span data-stu-id="bc24e-132">-Confirm</span></span>
<span data-ttu-id="bc24e-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc24e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc24e-134">-WhatIf</span></span>
<span data-ttu-id="bc24e-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc24e-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc24e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc24e-137">CommonParameters</span></span>
<span data-ttu-id="bc24e-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc24e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc24e-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc24e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc24e-140">입력</span><span class="sxs-lookup"><span data-stu-id="bc24e-140">INPUTS</span></span>

### <span data-ttu-id="bc24e-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bc24e-141">System.String</span></span>
<span data-ttu-id="bc24e-142">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bc24e-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="bc24e-143">출력</span><span class="sxs-lookup"><span data-stu-id="bc24e-143">OUTPUTS</span></span>

### <span data-ttu-id="bc24e-144">PSVpnProfile에 대 한.</span><span class="sxs-lookup"><span data-stu-id="bc24e-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="bc24e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="bc24e-145">NOTES</span></span>

## <span data-ttu-id="bc24e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc24e-146">RELATED LINKS</span></span>

