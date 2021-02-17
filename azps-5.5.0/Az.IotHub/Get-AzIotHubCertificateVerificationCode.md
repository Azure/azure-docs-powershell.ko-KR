---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 4bf362402ba3db0ba50d9144d6bb9fa79977a998
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192425"
---
# <span data-ttu-id="711cd-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="711cd-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="711cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="711cd-102">SYNOPSIS</span></span>
<span data-ttu-id="711cd-103">Azure IoT Hub 인증서에 대한 확인 코드를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="711cd-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="711cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="711cd-104">SYNTAX</span></span>

### <span data-ttu-id="711cd-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="711cd-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="711cd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="711cd-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="711cd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="711cd-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="711cd-108">설명</span><span class="sxs-lookup"><span data-stu-id="711cd-108">DESCRIPTION</span></span>
<span data-ttu-id="711cd-109">이 확인 코드는 인증서에 대한 소유 증명 단계를 완료하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="711cd-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="711cd-110">루트 인증서 개인 키로 서명된 새 인증서의 CN으로 이 확인 코드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="711cd-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="711cd-111">Azure IoT Hub의 CA 인증서에 대한 자세한 설명은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="711cd-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="711cd-112">예제</span><span class="sxs-lookup"><span data-stu-id="711cd-112">EXAMPLES</span></span>

### <span data-ttu-id="711cd-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="711cd-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="711cd-114">MyCertificate에 대한 확인 코드를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="711cd-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="711cd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="711cd-115">PARAMETERS</span></span>

### <span data-ttu-id="711cd-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="711cd-116">-CertificateName</span></span>
<span data-ttu-id="711cd-117">인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="711cd-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="711cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="711cd-118">-DefaultProfile</span></span>
<span data-ttu-id="711cd-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="711cd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="711cd-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="711cd-120">-Etag</span></span>
<span data-ttu-id="711cd-121">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="711cd-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="711cd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="711cd-122">-InputObject</span></span>
<span data-ttu-id="711cd-123">인증서 개체</span><span class="sxs-lookup"><span data-stu-id="711cd-123">Certificate Object</span></span>

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

### <span data-ttu-id="711cd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="711cd-124">-Name</span></span>
<span data-ttu-id="711cd-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="711cd-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="711cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="711cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="711cd-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="711cd-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="711cd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="711cd-128">-ResourceId</span></span>
<span data-ttu-id="711cd-129">인증서 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="711cd-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="711cd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711cd-130">CommonParameters</span></span>
<span data-ttu-id="711cd-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="711cd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711cd-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="711cd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711cd-133">입력</span><span class="sxs-lookup"><span data-stu-id="711cd-133">INPUTS</span></span>

### <span data-ttu-id="711cd-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="711cd-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="711cd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="711cd-135">System.String</span></span>

## <span data-ttu-id="711cd-136">출력</span><span class="sxs-lookup"><span data-stu-id="711cd-136">OUTPUTS</span></span>

### <span data-ttu-id="711cd-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="711cd-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="711cd-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="711cd-138">NOTES</span></span>

## <span data-ttu-id="711cd-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="711cd-139">RELATED LINKS</span></span>
