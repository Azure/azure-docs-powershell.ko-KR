---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 78881a7bd82aedeed4dca2a7ee08ea40812a0b05
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214506"
---
# <span data-ttu-id="02c44-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="02c44-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="02c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02c44-102">SYNOPSIS</span></span>
<span data-ttu-id="02c44-103">Azure IoT Hub 인증서를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="02c44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02c44-104">SYNTAX</span></span>

### <span data-ttu-id="02c44-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="02c44-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02c44-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="02c44-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c44-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="02c44-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c44-108">설명은</span><span class="sxs-lookup"><span data-stu-id="02c44-108">DESCRIPTION</span></span>
<span data-ttu-id="02c44-109">Cmdlet AzIotHubCertificateVerificationCode에서 얻은 확인 코드를 포함 하는 확인 인증서를 업로드 하 여 인증서를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="02c44-110">이는 소유 증명 프로세스의 마지막 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="02c44-111">Azure IoT Hub의 CA 인증서에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="02c44-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="02c44-112">예제의</span><span class="sxs-lookup"><span data-stu-id="02c44-112">EXAMPLES</span></span>

### <span data-ttu-id="02c44-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="02c44-113">Example 1</span></span>
```
PS C:\> Set-AzIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="02c44-114">MyCertificate 개인 키의 소유권을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="02c44-115">변수</span><span class="sxs-lookup"><span data-stu-id="02c44-115">PARAMETERS</span></span>

### <span data-ttu-id="02c44-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="02c44-116">-CertificateName</span></span>
<span data-ttu-id="02c44-117">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="02c44-117">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c44-118">-DefaultProfile</span></span>
<span data-ttu-id="02c44-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02c44-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="02c44-120">-Etag</span></span>
<span data-ttu-id="02c44-121">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="02c44-121">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c44-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02c44-122">-InputObject</span></span>
<span data-ttu-id="02c44-123">인증서 개체</span><span class="sxs-lookup"><span data-stu-id="02c44-123">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02c44-124">-이름</span><span class="sxs-lookup"><span data-stu-id="02c44-124">-Name</span></span>
<span data-ttu-id="02c44-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="02c44-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c44-126">-Path</span><span class="sxs-lookup"><span data-stu-id="02c44-126">-Path</span></span>
<span data-ttu-id="02c44-127">base-64는 X509 인증서 .cer 파일 또는 pem 파일 경로의 표시입니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c44-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c44-128">-ResourceGroupName</span></span>
<span data-ttu-id="02c44-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c44-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02c44-130">-ResourceId</span></span>
<span data-ttu-id="02c44-131">인증서 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="02c44-131">Certificate Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c44-132">-확인</span><span class="sxs-lookup"><span data-stu-id="02c44-132">-Confirm</span></span>
<span data-ttu-id="02c44-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c44-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c44-134">-WhatIf</span></span>
<span data-ttu-id="02c44-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c44-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c44-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c44-137">CommonParameters</span></span>
<span data-ttu-id="02c44-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02c44-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c44-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c44-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c44-140">입력</span><span class="sxs-lookup"><span data-stu-id="02c44-140">INPUTS</span></span>

### <span data-ttu-id="02c44-141">IotHub. PSCertificateDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="02c44-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="02c44-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02c44-142">System.String</span></span>

## <span data-ttu-id="02c44-143">출력</span><span class="sxs-lookup"><span data-stu-id="02c44-143">OUTPUTS</span></span>

### <span data-ttu-id="02c44-144">IotHub. PSCertificateDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="02c44-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="02c44-145">상속자</span><span class="sxs-lookup"><span data-stu-id="02c44-145">NOTES</span></span>

## <span data-ttu-id="02c44-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02c44-146">RELATED LINKS</span></span>
