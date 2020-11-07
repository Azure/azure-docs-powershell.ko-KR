---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 5a8d9c4240ed71b3e5395a3b27927c9477051665
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868134"
---
# <span data-ttu-id="fd125-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="fd125-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="fd125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd125-102">SYNOPSIS</span></span>
<span data-ttu-id="fd125-103">모든 인증서 또는 Azure IoT Hub 내에 포함 된 특정 인증서를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd125-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="fd125-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd125-104">SYNTAX</span></span>

### <span data-ttu-id="fd125-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd125-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd125-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd125-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd125-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd125-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd125-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fd125-108">DESCRIPTION</span></span>
<span data-ttu-id="fd125-109">Azure IoT Hub의 CA 인증서에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="fd125-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="fd125-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fd125-110">EXAMPLES</span></span>

### <span data-ttu-id="fd125-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd125-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="fd125-112">MyIotHub의 모든 인증서 목록 표시</span><span class="sxs-lookup"><span data-stu-id="fd125-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="fd125-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="fd125-113">Example 2</span></span>
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

<span data-ttu-id="fd125-114">MyCertificate에 대 한 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="fd125-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="fd125-115">변수</span><span class="sxs-lookup"><span data-stu-id="fd125-115">PARAMETERS</span></span>

### <span data-ttu-id="fd125-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="fd125-116">-CertificateName</span></span>
<span data-ttu-id="fd125-117">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="fd125-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="fd125-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd125-118">-DefaultProfile</span></span>
<span data-ttu-id="fd125-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd125-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd125-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd125-120">-InputObject</span></span>
<span data-ttu-id="fd125-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="fd125-121">IotHub Object</span></span>

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

### <span data-ttu-id="fd125-122">-이름</span><span class="sxs-lookup"><span data-stu-id="fd125-122">-Name</span></span>
<span data-ttu-id="fd125-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="fd125-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fd125-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd125-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd125-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd125-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fd125-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd125-126">-ResourceId</span></span>
<span data-ttu-id="fd125-127">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="fd125-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fd125-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd125-128">CommonParameters</span></span>
<span data-ttu-id="fd125-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd125-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd125-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd125-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd125-131">입력</span><span class="sxs-lookup"><span data-stu-id="fd125-131">INPUTS</span></span>

### <span data-ttu-id="fd125-132">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="fd125-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fd125-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd125-133">System.String</span></span>

## <span data-ttu-id="fd125-134">출력</span><span class="sxs-lookup"><span data-stu-id="fd125-134">OUTPUTS</span></span>

### <span data-ttu-id="fd125-135">IotHub. PSCertificateDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="fd125-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="fd125-136">상속자</span><span class="sxs-lookup"><span data-stu-id="fd125-136">NOTES</span></span>

## <span data-ttu-id="fd125-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd125-137">RELATED LINKS</span></span>
