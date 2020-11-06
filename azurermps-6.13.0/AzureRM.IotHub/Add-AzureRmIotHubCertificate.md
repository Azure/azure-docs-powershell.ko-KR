---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubCertificate.md
ms.openlocfilehash: d411b0613b85a70a1f3dc0d1726f847148a0f30c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530288"
---
# <span data-ttu-id="aef07-101">Add-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="aef07-101">Add-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="aef07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aef07-102">SYNOPSIS</span></span>
<span data-ttu-id="aef07-103">Azure IoT Hub 인증서를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-103">Create/update an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aef07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aef07-104">SYNTAX</span></span>

### <span data-ttu-id="aef07-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aef07-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aef07-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aef07-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef07-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aef07-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aef07-108">설명은</span><span class="sxs-lookup"><span data-stu-id="aef07-108">DESCRIPTION</span></span>
<span data-ttu-id="aef07-109">새 인증서를 업로드 하거나 같은 이름으로 기존 인증서를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="aef07-110">Azure IoT Hub의 CA 인증서에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="aef07-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="aef07-111">예제의</span><span class="sxs-lookup"><span data-stu-id="aef07-111">EXAMPLES</span></span>

### <span data-ttu-id="aef07-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="aef07-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="aef07-113">IoT hub에 CA 인증서 CER 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="aef07-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="aef07-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="aef07-115">새 CER 파일을 업로드 하 여 IoT hub에서 CA 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="aef07-116">변수</span><span class="sxs-lookup"><span data-stu-id="aef07-116">PARAMETERS</span></span>

### <span data-ttu-id="aef07-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="aef07-117">-CertificateName</span></span>
<span data-ttu-id="aef07-118">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="aef07-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="aef07-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef07-119">-DefaultProfile</span></span>
<span data-ttu-id="aef07-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef07-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="aef07-121">-Etag</span></span>
<span data-ttu-id="aef07-122">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="aef07-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="aef07-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aef07-123">-InputObject</span></span>
<span data-ttu-id="aef07-124">인증서 개체</span><span class="sxs-lookup"><span data-stu-id="aef07-124">Certificate Object</span></span>

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

### <span data-ttu-id="aef07-125">-이름</span><span class="sxs-lookup"><span data-stu-id="aef07-125">-Name</span></span>
<span data-ttu-id="aef07-126">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="aef07-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="aef07-127">-Path</span><span class="sxs-lookup"><span data-stu-id="aef07-127">-Path</span></span>
<span data-ttu-id="aef07-128">base-64는 X509 인증서 .cer 파일 또는 pem 파일 경로의 표시입니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="aef07-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aef07-129">-ResourceGroupName</span></span>
<span data-ttu-id="aef07-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aef07-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aef07-131">-ResourceId</span></span>
<span data-ttu-id="aef07-132">인증서 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="aef07-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="aef07-133">-확인</span><span class="sxs-lookup"><span data-stu-id="aef07-133">-Confirm</span></span>
<span data-ttu-id="aef07-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aef07-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aef07-135">-WhatIf</span></span>
<span data-ttu-id="aef07-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aef07-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aef07-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef07-138">CommonParameters</span></span>
<span data-ttu-id="aef07-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aef07-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef07-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aef07-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef07-141">입력</span><span class="sxs-lookup"><span data-stu-id="aef07-141">INPUTS</span></span>

### <span data-ttu-id="aef07-142">IotHub. PSCertificateDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="aef07-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="aef07-143">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aef07-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="aef07-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aef07-144">System.String</span></span>

## <span data-ttu-id="aef07-145">출력</span><span class="sxs-lookup"><span data-stu-id="aef07-145">OUTPUTS</span></span>

### <span data-ttu-id="aef07-146">IotHub. PSCertificateDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="aef07-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="aef07-147">상속자</span><span class="sxs-lookup"><span data-stu-id="aef07-147">NOTES</span></span>

## <span data-ttu-id="aef07-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aef07-148">RELATED LINKS</span></span>
