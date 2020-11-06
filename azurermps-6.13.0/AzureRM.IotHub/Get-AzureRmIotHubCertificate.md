---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
ms.openlocfilehash: 745fcb6fdfb9ee47faf28cde84985dcfd7199ecc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535904"
---
# <span data-ttu-id="4516d-101">Get-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="4516d-101">Get-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="4516d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4516d-102">SYNOPSIS</span></span>
<span data-ttu-id="4516d-103">모든 인증서 또는 Azure IoT Hub 내에 포함 된 특정 인증서를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4516d-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4516d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4516d-104">SYNTAX</span></span>

### <span data-ttu-id="4516d-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4516d-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4516d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4516d-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4516d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4516d-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4516d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4516d-108">DESCRIPTION</span></span>
<span data-ttu-id="4516d-109">Azure IoT Hub의 CA 인증서에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="4516d-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="4516d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4516d-110">EXAMPLES</span></span>

### <span data-ttu-id="4516d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4516d-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="4516d-112">MyIotHub의 모든 인증서 목록 표시</span><span class="sxs-lookup"><span data-stu-id="4516d-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="4516d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4516d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

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

<span data-ttu-id="4516d-114">MyCertificate에 대 한 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="4516d-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="4516d-115">변수</span><span class="sxs-lookup"><span data-stu-id="4516d-115">PARAMETERS</span></span>

### <span data-ttu-id="4516d-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4516d-116">-CertificateName</span></span>
<span data-ttu-id="4516d-117">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="4516d-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="4516d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4516d-118">-DefaultProfile</span></span>
<span data-ttu-id="4516d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4516d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4516d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4516d-120">-InputObject</span></span>
<span data-ttu-id="4516d-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="4516d-121">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4516d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="4516d-122">-Name</span></span>
<span data-ttu-id="4516d-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="4516d-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4516d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4516d-124">-ResourceGroupName</span></span>
<span data-ttu-id="4516d-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4516d-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4516d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4516d-126">-ResourceId</span></span>
<span data-ttu-id="4516d-127">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="4516d-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4516d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4516d-128">CommonParameters</span></span>
<span data-ttu-id="4516d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4516d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4516d-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4516d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4516d-131">입력</span><span class="sxs-lookup"><span data-stu-id="4516d-131">INPUTS</span></span>

### <span data-ttu-id="4516d-132">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="4516d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="4516d-133">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4516d-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4516d-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4516d-134">System.String</span></span>

## <span data-ttu-id="4516d-135">출력</span><span class="sxs-lookup"><span data-stu-id="4516d-135">OUTPUTS</span></span>

### <span data-ttu-id="4516d-136">IotHub. PSCertificateDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="4516d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="4516d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="4516d-137">NOTES</span></span>

## <span data-ttu-id="4516d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4516d-138">RELATED LINKS</span></span>
