---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186009"
---
# <span data-ttu-id="89b28-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="89b28-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="89b28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89b28-102">SYNOPSIS</span></span>
<span data-ttu-id="89b28-103">디바이스 등록 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="89b28-103">Gets the device registration state.</span></span>

## <span data-ttu-id="89b28-104">구문</span><span class="sxs-lookup"><span data-stu-id="89b28-104">SYNTAX</span></span>

### <span data-ttu-id="89b28-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="89b28-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89b28-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="89b28-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89b28-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="89b28-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89b28-108">설명</span><span class="sxs-lookup"><span data-stu-id="89b28-108">DESCRIPTION</span></span>
<span data-ttu-id="89b28-109">Azure IoT Hub Device Provisioning Service의 enrollmentGroup에서 디바이스 등록 상태 또는 디바이스의 등록 상태를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="89b28-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="89b28-110">예제</span><span class="sxs-lookup"><span data-stu-id="89b28-110">EXAMPLES</span></span>

### <span data-ttu-id="89b28-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="89b28-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="89b28-112">Azure IoT Hub Device Provisioning Service에서 디바이스 등록 상태 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="89b28-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="89b28-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="89b28-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="89b28-114">이 enrollmentGroup에서 디바이스의 모든 등록 상태를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="89b28-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="89b28-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89b28-115">PARAMETERS</span></span>

### <span data-ttu-id="89b28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b28-116">-DefaultProfile</span></span>
<span data-ttu-id="89b28-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89b28-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89b28-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="89b28-118">-DpsName</span></span>
<span data-ttu-id="89b28-119">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="89b28-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="89b28-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="89b28-120">-DpsObject</span></span>
<span data-ttu-id="89b28-121">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="89b28-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="89b28-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="89b28-122">-EnrollmentId</span></span>
<span data-ttu-id="89b28-123">등록 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="89b28-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="89b28-124">-Query</span><span class="sxs-lookup"><span data-stu-id="89b28-124">-Query</span></span>
<span data-ttu-id="89b28-125">Sql 쿼리.</span><span class="sxs-lookup"><span data-stu-id="89b28-125">Sql query.</span></span>

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

### <span data-ttu-id="89b28-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="89b28-126">-RegistrationId</span></span>
<span data-ttu-id="89b28-127">디바이스 등록의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="89b28-127">ID of device registration.</span></span>

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

### <span data-ttu-id="89b28-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b28-128">-ResourceGroupName</span></span>
<span data-ttu-id="89b28-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="89b28-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="89b28-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89b28-130">-ResourceId</span></span>
<span data-ttu-id="89b28-131">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="89b28-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="89b28-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b28-132">CommonParameters</span></span>
<span data-ttu-id="89b28-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89b28-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b28-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="89b28-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b28-135">입력</span><span class="sxs-lookup"><span data-stu-id="89b28-135">INPUTS</span></span>

### <span data-ttu-id="89b28-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="89b28-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="89b28-137">System.String</span><span class="sxs-lookup"><span data-stu-id="89b28-137">System.String</span></span>

## <span data-ttu-id="89b28-138">출력</span><span class="sxs-lookup"><span data-stu-id="89b28-138">OUTPUTS</span></span>

### <span data-ttu-id="89b28-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="89b28-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="89b28-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span><span class="sxs-lookup"><span data-stu-id="89b28-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="89b28-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="89b28-141">NOTES</span></span>

## <span data-ttu-id="89b28-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89b28-142">RELATED LINKS</span></span>
