---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209672"
---
# <span data-ttu-id="108ab-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="108ab-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="108ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="108ab-102">SYNOPSIS</span></span>
<span data-ttu-id="108ab-103">Azure IoT Hub 디바이스 프로비전 서비스에 새 공유 액세스 정책을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="108ab-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="108ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="108ab-104">SYNTAX</span></span>

### <span data-ttu-id="108ab-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="108ab-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="108ab-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="108ab-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="108ab-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="108ab-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="108ab-108">설명</span><span class="sxs-lookup"><span data-stu-id="108ab-108">DESCRIPTION</span></span>
<span data-ttu-id="108ab-109">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="108ab-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="108ab-110">예제</span><span class="sxs-lookup"><span data-stu-id="108ab-110">EXAMPLES</span></span>

### <span data-ttu-id="108ab-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="108ab-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="108ab-112">EnrollmentWrite 및 ServiceConfig 권한을 사용하여 Azure IoT Hub 디바이스 프로비전 서비스에 새 공유 액세스 정책을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="108ab-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="108ab-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="108ab-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="108ab-114">EnrollmentRead 권한을 사용하여 Azure IoT Hub 디바이스 프로비전 서비스에 새 공유 액세스 정책을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="108ab-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="108ab-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="108ab-115">PARAMETERS</span></span>

### <span data-ttu-id="108ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108ab-116">-DefaultProfile</span></span>
<span data-ttu-id="108ab-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="108ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="108ab-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="108ab-118">-DpsObject</span></span>
<span data-ttu-id="108ab-119">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="108ab-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="108ab-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="108ab-120">-KeyName</span></span>
<span data-ttu-id="108ab-121">IoT Device Provisioning Service 액세스 정책 키 이름</span><span class="sxs-lookup"><span data-stu-id="108ab-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="108ab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="108ab-122">-Name</span></span>
<span data-ttu-id="108ab-123">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="108ab-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="108ab-124">-Permissions</span><span class="sxs-lookup"><span data-stu-id="108ab-124">-Permissions</span></span>
<span data-ttu-id="108ab-125">IoT Device Provisioning Service 액세스 정책 권한</span><span class="sxs-lookup"><span data-stu-id="108ab-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108ab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="108ab-126">-ResourceGroupName</span></span>
<span data-ttu-id="108ab-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="108ab-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="108ab-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="108ab-128">-ResourceId</span></span>
<span data-ttu-id="108ab-129">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="108ab-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="108ab-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="108ab-130">-Confirm</span></span>
<span data-ttu-id="108ab-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="108ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="108ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="108ab-132">-WhatIf</span></span>
<span data-ttu-id="108ab-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="108ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="108ab-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="108ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="108ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108ab-135">CommonParameters</span></span>
<span data-ttu-id="108ab-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="108ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108ab-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="108ab-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108ab-138">입력</span><span class="sxs-lookup"><span data-stu-id="108ab-138">INPUTS</span></span>

### <span data-ttu-id="108ab-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="108ab-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="108ab-140">System.String</span><span class="sxs-lookup"><span data-stu-id="108ab-140">System.String</span></span>

## <span data-ttu-id="108ab-141">출력</span><span class="sxs-lookup"><span data-stu-id="108ab-141">OUTPUTS</span></span>

### <span data-ttu-id="108ab-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="108ab-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="108ab-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="108ab-143">NOTES</span></span>

## <span data-ttu-id="108ab-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="108ab-144">RELATED LINKS</span></span>
