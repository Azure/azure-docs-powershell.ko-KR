---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 56aadda2d7f1dccb77795d5226fb79c8a0fc65ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958720"
---
# <span data-ttu-id="0d1b1-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="0d1b1-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="0d1b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1b1-103">디바이스 등록 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="0d1b1-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d1b1-104">SYNTAX</span></span>

### <span data-ttu-id="0d1b1-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0d1b1-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d1b1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0d1b1-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d1b1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0d1b1-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d1b1-108">설명</span><span class="sxs-lookup"><span data-stu-id="0d1b1-108">DESCRIPTION</span></span>
<span data-ttu-id="0d1b1-109">Azure IoT Hub Device Provisioning Service에서 디바이스 등록 세부 정보를 얻거나 디바이스 등록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="0d1b1-110">예제</span><span class="sxs-lookup"><span data-stu-id="0d1b1-110">EXAMPLES</span></span>

### <span data-ttu-id="0d1b1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d1b1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="0d1b1-112">Azure IoT Hub Device Provisioning Service에서 디바이스 등록 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="0d1b1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0d1b1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="0d1b1-114">Azure IoT Hub 디바이스 프로비전 서비스에 디바이스 등록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="0d1b1-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d1b1-115">PARAMETERS</span></span>

### <span data-ttu-id="0d1b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1b1-116">-DefaultProfile</span></span>
<span data-ttu-id="0d1b1-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d1b1-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="0d1b1-118">-DpsName</span></span>
<span data-ttu-id="0d1b1-119">IoT 디바이스 프로비전 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="0d1b1-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0d1b1-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="0d1b1-120">-DpsObject</span></span>
<span data-ttu-id="0d1b1-121">IoT 디바이스 프로비전 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="0d1b1-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1b1-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="0d1b1-122">-RegistrationId</span></span>
<span data-ttu-id="0d1b1-123">개별 등록 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="0d1b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d1b1-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="0d1b1-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1b1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d1b1-126">-ResourceId</span></span>
<span data-ttu-id="0d1b1-127">IoT 디바이스 프로비전 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0d1b1-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0d1b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1b1-128">CommonParameters</span></span>
<span data-ttu-id="0d1b1-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1b1-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1b1-131">입력</span><span class="sxs-lookup"><span data-stu-id="0d1b1-131">INPUTS</span></span>

### <span data-ttu-id="0d1b1-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0d1b1-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0d1b1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0d1b1-133">System.String</span></span>

## <span data-ttu-id="0d1b1-134">출력</span><span class="sxs-lookup"><span data-stu-id="0d1b1-134">OUTPUTS</span></span>

### <span data-ttu-id="0d1b1-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="0d1b1-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="0d1b1-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span><span class="sxs-lookup"><span data-stu-id="0d1b1-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="0d1b1-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d1b1-137">NOTES</span></span>

## <span data-ttu-id="0d1b1-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d1b1-138">RELATED LINKS</span></span>
