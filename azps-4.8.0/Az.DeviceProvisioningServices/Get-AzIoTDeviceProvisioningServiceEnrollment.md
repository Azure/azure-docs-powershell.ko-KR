---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048295"
---
# <span data-ttu-id="219cf-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="219cf-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="219cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="219cf-102">SYNOPSIS</span></span>
<span data-ttu-id="219cf-103">장치 등록 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="219cf-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="219cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="219cf-104">SYNTAX</span></span>

### <span data-ttu-id="219cf-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="219cf-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="219cf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="219cf-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="219cf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="219cf-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="219cf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="219cf-108">DESCRIPTION</span></span>
<span data-ttu-id="219cf-109">Azure IoT Hub Device 프로비저닝 서비스에서 장치 등록 세부 정보를 가져오거나 장치 enrollments를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="219cf-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="219cf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="219cf-110">EXAMPLES</span></span>

### <span data-ttu-id="219cf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="219cf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="219cf-112">Azure IoT Hub 디바이스 프로비저닝 서비스에서 장치 등록 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="219cf-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="219cf-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="219cf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="219cf-114">Azure IoT Hub 디바이스 프로비저닝 서비스에서 디바이스 enrollments를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="219cf-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="219cf-115">변수</span><span class="sxs-lookup"><span data-stu-id="219cf-115">PARAMETERS</span></span>

### <span data-ttu-id="219cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219cf-116">-DefaultProfile</span></span>
<span data-ttu-id="219cf-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="219cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="219cf-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="219cf-118">-DpsName</span></span>
<span data-ttu-id="219cf-119">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="219cf-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="219cf-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="219cf-120">-DpsObject</span></span>
<span data-ttu-id="219cf-121">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="219cf-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="219cf-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="219cf-122">-RegistrationId</span></span>
<span data-ttu-id="219cf-123">개별 등록 등록 id입니다.</span><span class="sxs-lookup"><span data-stu-id="219cf-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="219cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="219cf-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="219cf-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="219cf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="219cf-126">-ResourceId</span></span>
<span data-ttu-id="219cf-127">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="219cf-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="219cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219cf-128">CommonParameters</span></span>
<span data-ttu-id="219cf-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="219cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219cf-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="219cf-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219cf-131">입력</span><span class="sxs-lookup"><span data-stu-id="219cf-131">INPUTS</span></span>

### <span data-ttu-id="219cf-132">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="219cf-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="219cf-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="219cf-133">System.String</span></span>

## <span data-ttu-id="219cf-134">출력</span><span class="sxs-lookup"><span data-stu-id="219cf-134">OUTPUTS</span></span>

### <span data-ttu-id="219cf-135">DeviceProvisioningServices. PSIndividualEnrollment/. \*</span><span class="sxs-lookup"><span data-stu-id="219cf-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="219cf-136">DeviceProvisioningServices를 PSIndividualEnrollments []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="219cf-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="219cf-137">상속자</span><span class="sxs-lookup"><span data-stu-id="219cf-137">NOTES</span></span>

## <span data-ttu-id="219cf-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="219cf-138">RELATED LINKS</span></span>
