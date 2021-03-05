---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 06a6f2ea8ffbd0d90689a24d3fcec5ca8222f9ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988162"
---
# <span data-ttu-id="e5758-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="e5758-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="e5758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5758-102">SYNOPSIS</span></span>
<span data-ttu-id="e5758-103">Azure IoT Hub에 포함된 모든 인증서 또는 특정 인증서를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e5758-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="e5758-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5758-104">SYNTAX</span></span>

### <span data-ttu-id="e5758-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e5758-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5758-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e5758-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5758-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e5758-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5758-108">설명</span><span class="sxs-lookup"><span data-stu-id="e5758-108">DESCRIPTION</span></span>
<span data-ttu-id="e5758-109">Azure IoT Hub의 CA 인증서에 대한 자세한 설명은 https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="e5758-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="e5758-110">예제</span><span class="sxs-lookup"><span data-stu-id="e5758-110">EXAMPLES</span></span>

### <span data-ttu-id="e5758-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5758-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="e5758-112">MyIotHub의 모든 인증서 나열</span><span class="sxs-lookup"><span data-stu-id="e5758-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="e5758-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e5758-113">Example 2</span></span>
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

<span data-ttu-id="e5758-114">MyCertificate에 대한 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="e5758-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="e5758-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e5758-115">PARAMETERS</span></span>

### <span data-ttu-id="e5758-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e5758-116">-CertificateName</span></span>
<span data-ttu-id="e5758-117">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="e5758-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="e5758-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5758-118">-DefaultProfile</span></span>
<span data-ttu-id="e5758-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5758-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5758-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5758-120">-InputObject</span></span>
<span data-ttu-id="e5758-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="e5758-121">IotHub Object</span></span>

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

### <span data-ttu-id="e5758-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e5758-122">-Name</span></span>
<span data-ttu-id="e5758-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="e5758-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e5758-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5758-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5758-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e5758-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e5758-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5758-126">-ResourceId</span></span>
<span data-ttu-id="e5758-127">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e5758-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e5758-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5758-128">CommonParameters</span></span>
<span data-ttu-id="e5758-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5758-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5758-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5758-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5758-131">입력</span><span class="sxs-lookup"><span data-stu-id="e5758-131">INPUTS</span></span>

### <span data-ttu-id="e5758-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e5758-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e5758-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e5758-133">System.String</span></span>

## <span data-ttu-id="e5758-134">출력</span><span class="sxs-lookup"><span data-stu-id="e5758-134">OUTPUTS</span></span>

### <span data-ttu-id="e5758-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="e5758-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="e5758-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5758-136">NOTES</span></span>

## <span data-ttu-id="e5758-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5758-137">RELATED LINKS</span></span>
