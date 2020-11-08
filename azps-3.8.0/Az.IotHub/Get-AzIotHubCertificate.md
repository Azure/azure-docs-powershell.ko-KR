---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 8bc586ea9543c7545e7d24e3bc6d7bc36bb77d49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033913"
---
# <span data-ttu-id="8e1b7-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="8e1b7-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="8e1b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1b7-103">모든 인증서 또는 Azure IoT Hub 내에 포함 된 특정 인증서를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="8e1b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e1b7-104">SYNTAX</span></span>

### <span data-ttu-id="8e1b7-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8e1b7-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e1b7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8e1b7-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e1b7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8e1b7-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e1b7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8e1b7-108">DESCRIPTION</span></span>
<span data-ttu-id="8e1b7-109">Azure IoT Hub의 CA 인증서에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="8e1b7-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="8e1b7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8e1b7-110">EXAMPLES</span></span>

### <span data-ttu-id="8e1b7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e1b7-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="8e1b7-112">MyIotHub의 모든 인증서 목록 표시</span><span class="sxs-lookup"><span data-stu-id="8e1b7-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="8e1b7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8e1b7-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

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

<span data-ttu-id="8e1b7-114">MyCertificate에 대 한 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="8e1b7-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="8e1b7-115">변수</span><span class="sxs-lookup"><span data-stu-id="8e1b7-115">PARAMETERS</span></span>

### <span data-ttu-id="8e1b7-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="8e1b7-116">-CertificateName</span></span>
<span data-ttu-id="8e1b7-117">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="8e1b7-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="8e1b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1b7-118">-DefaultProfile</span></span>
<span data-ttu-id="8e1b7-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e1b7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e1b7-120">-InputObject</span></span>
<span data-ttu-id="8e1b7-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="8e1b7-121">IotHub Object</span></span>

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

### <span data-ttu-id="8e1b7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="8e1b7-122">-Name</span></span>
<span data-ttu-id="8e1b7-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="8e1b7-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8e1b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e1b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="8e1b7-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8e1b7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e1b7-126">-ResourceId</span></span>
<span data-ttu-id="8e1b7-127">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="8e1b7-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8e1b7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1b7-128">CommonParameters</span></span>
<span data-ttu-id="8e1b7-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1b7-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e1b7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1b7-131">입력</span><span class="sxs-lookup"><span data-stu-id="8e1b7-131">INPUTS</span></span>

### <span data-ttu-id="8e1b7-132">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="8e1b7-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8e1b7-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8e1b7-133">System.String</span></span>

## <span data-ttu-id="8e1b7-134">출력</span><span class="sxs-lookup"><span data-stu-id="8e1b7-134">OUTPUTS</span></span>

### <span data-ttu-id="8e1b7-135">IotHub. PSCertificateDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="8e1b7-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="8e1b7-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8e1b7-136">NOTES</span></span>

## <span data-ttu-id="8e1b7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e1b7-137">RELATED LINKS</span></span>
