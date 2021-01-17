---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492017"
---
# <span data-ttu-id="5c2a0-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="5c2a0-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="5c2a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2a0-103">디바이스 등록 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c2a0-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="5c2a0-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c2a0-104">SYNTAX</span></span>

### <span data-ttu-id="5c2a0-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5c2a0-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c2a0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5c2a0-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c2a0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5c2a0-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c2a0-108">설명</span><span class="sxs-lookup"><span data-stu-id="5c2a0-108">DESCRIPTION</span></span>
<span data-ttu-id="5c2a0-109">Azure IoT Hub Device Provisioning Service에서 디바이스 등록 세부 정보를 얻거나 디바이스 등록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5c2a0-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="5c2a0-110">예제</span><span class="sxs-lookup"><span data-stu-id="5c2a0-110">EXAMPLES</span></span>

### <span data-ttu-id="5c2a0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c2a0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="5c2a0-112">Azure IoT Hub Device Provisioning Service에서 디바이스 등록 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5c2a0-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="5c2a0-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5c2a0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="5c2a0-114">Azure IoT Hub Device Provisioning Service에서 디바이스 등록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5c2a0-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="5c2a0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c2a0-115">PARAMETERS</span></span>

### <span data-ttu-id="5c2a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2a0-116">-DefaultProfile</span></span>
<span data-ttu-id="5c2a0-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c2a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c2a0-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="5c2a0-118">-DpsName</span></span>
<span data-ttu-id="5c2a0-119">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="5c2a0-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5c2a0-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5c2a0-120">-DpsObject</span></span>
<span data-ttu-id="5c2a0-121">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="5c2a0-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5c2a0-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="5c2a0-122">-RegistrationId</span></span>
<span data-ttu-id="5c2a0-123">개별 등록 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5c2a0-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="5c2a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c2a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c2a0-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="5c2a0-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5c2a0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c2a0-126">-ResourceId</span></span>
<span data-ttu-id="5c2a0-127">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5c2a0-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5c2a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2a0-128">CommonParameters</span></span>
<span data-ttu-id="5c2a0-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c2a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2a0-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5c2a0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2a0-131">입력</span><span class="sxs-lookup"><span data-stu-id="5c2a0-131">INPUTS</span></span>

### <span data-ttu-id="5c2a0-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5c2a0-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5c2a0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5c2a0-133">System.String</span></span>

## <span data-ttu-id="5c2a0-134">출력</span><span class="sxs-lookup"><span data-stu-id="5c2a0-134">OUTPUTS</span></span>

### <span data-ttu-id="5c2a0-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="5c2a0-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="5c2a0-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span><span class="sxs-lookup"><span data-stu-id="5c2a0-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="5c2a0-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c2a0-137">NOTES</span></span>

## <span data-ttu-id="5c2a0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c2a0-138">RELATED LINKS</span></span>
