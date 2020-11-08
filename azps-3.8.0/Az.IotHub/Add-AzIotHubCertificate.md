---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 6d77bcc6d940c5891b4fc06875dc353af5f75939
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044258"
---
# <span data-ttu-id="a1763-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="a1763-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="a1763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1763-102">SYNOPSIS</span></span>
<span data-ttu-id="a1763-103">Azure IoT Hub 인증서를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="a1763-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1763-104">SYNTAX</span></span>

### <span data-ttu-id="a1763-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a1763-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1763-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a1763-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1763-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a1763-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1763-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a1763-108">DESCRIPTION</span></span>
<span data-ttu-id="a1763-109">새 인증서를 업로드 하거나 같은 이름으로 기존 인증서를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="a1763-110">Azure IoT Hub의 CA 인증서에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="a1763-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="a1763-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a1763-111">EXAMPLES</span></span>

### <span data-ttu-id="a1763-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a1763-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="a1763-113">IoT hub에 CA 인증서 CER 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="a1763-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="a1763-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="a1763-115">새 CER 파일을 업로드 하 여 IoT hub에서 CA 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="a1763-116">변수</span><span class="sxs-lookup"><span data-stu-id="a1763-116">PARAMETERS</span></span>

### <span data-ttu-id="a1763-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a1763-117">-CertificateName</span></span>
<span data-ttu-id="a1763-118">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="a1763-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="a1763-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1763-119">-DefaultProfile</span></span>
<span data-ttu-id="a1763-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1763-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="a1763-121">-Etag</span></span>
<span data-ttu-id="a1763-122">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="a1763-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="a1763-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1763-123">-InputObject</span></span>
<span data-ttu-id="a1763-124">인증서 개체</span><span class="sxs-lookup"><span data-stu-id="a1763-124">Certificate Object</span></span>

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

### <span data-ttu-id="a1763-125">-이름</span><span class="sxs-lookup"><span data-stu-id="a1763-125">-Name</span></span>
<span data-ttu-id="a1763-126">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="a1763-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a1763-127">-Path</span><span class="sxs-lookup"><span data-stu-id="a1763-127">-Path</span></span>
<span data-ttu-id="a1763-128">base-64는 X509 인증서 .cer 파일 또는 pem 파일 경로의 표시입니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="a1763-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1763-129">-ResourceGroupName</span></span>
<span data-ttu-id="a1763-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a1763-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1763-131">-ResourceId</span></span>
<span data-ttu-id="a1763-132">인증서 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="a1763-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="a1763-133">-확인</span><span class="sxs-lookup"><span data-stu-id="a1763-133">-Confirm</span></span>
<span data-ttu-id="a1763-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1763-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1763-135">-WhatIf</span></span>
<span data-ttu-id="a1763-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1763-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1763-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1763-138">CommonParameters</span></span>
<span data-ttu-id="a1763-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1763-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1763-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1763-141">입력</span><span class="sxs-lookup"><span data-stu-id="a1763-141">INPUTS</span></span>

### <span data-ttu-id="a1763-142">IotHub. PSCertificateDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="a1763-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="a1763-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a1763-143">System.String</span></span>

## <span data-ttu-id="a1763-144">출력</span><span class="sxs-lookup"><span data-stu-id="a1763-144">OUTPUTS</span></span>

### <span data-ttu-id="a1763-145">IotHub. PSCertificateDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="a1763-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="a1763-146">상속자</span><span class="sxs-lookup"><span data-stu-id="a1763-146">NOTES</span></span>

## <span data-ttu-id="a1763-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1763-147">RELATED LINKS</span></span>
