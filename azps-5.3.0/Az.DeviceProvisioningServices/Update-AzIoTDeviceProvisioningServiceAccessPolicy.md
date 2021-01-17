---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492001"
---
# <span data-ttu-id="73f1c-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="73f1c-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="73f1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="73f1c-103">Azure IoT Hub 디바이스 프로비전 서비스에서 공유 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1c-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="73f1c-104">구문</span><span class="sxs-lookup"><span data-stu-id="73f1c-104">SYNTAX</span></span>

### <span data-ttu-id="73f1c-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="73f1c-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73f1c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="73f1c-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f1c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="73f1c-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f1c-108">설명</span><span class="sxs-lookup"><span data-stu-id="73f1c-108">DESCRIPTION</span></span>
<span data-ttu-id="73f1c-109">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1c-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="73f1c-110">예제</span><span class="sxs-lookup"><span data-stu-id="73f1c-110">EXAMPLES</span></span>

### <span data-ttu-id="73f1c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="73f1c-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="73f1c-112">EnrollmentWrite 권한을 사용하여 Azure IoT Hub 디바이스 프로비전 서비스에서 액세스 정책 "mypolicy"를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1c-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="73f1c-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="73f1c-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="73f1c-114">파이프라인을 사용하여 EnrollmentWrite를 사용하여 Azure IoT Hub 디바이스 프로비전 서비스에서 액세스 정책 "mypolicy"를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1c-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="73f1c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73f1c-115">PARAMETERS</span></span>

### <span data-ttu-id="73f1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f1c-116">-DefaultProfile</span></span>
<span data-ttu-id="73f1c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f1c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73f1c-118">-InputObject</span></span>
<span data-ttu-id="73f1c-119">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="73f1c-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73f1c-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="73f1c-120">-KeyName</span></span>
<span data-ttu-id="73f1c-121">IoT Device Provisioning Service 액세스 정책 키 이름</span><span class="sxs-lookup"><span data-stu-id="73f1c-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="73f1c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="73f1c-122">-Name</span></span>
<span data-ttu-id="73f1c-123">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="73f1c-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="73f1c-124">-Permissions</span><span class="sxs-lookup"><span data-stu-id="73f1c-124">-Permissions</span></span>
<span data-ttu-id="73f1c-125">IoT Device Provisioning Service 액세스 정책 권한</span><span class="sxs-lookup"><span data-stu-id="73f1c-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="73f1c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f1c-126">-ResourceGroupName</span></span>
<span data-ttu-id="73f1c-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="73f1c-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="73f1c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f1c-128">-ResourceId</span></span>
<span data-ttu-id="73f1c-129">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="73f1c-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="73f1c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73f1c-130">-Confirm</span></span>
<span data-ttu-id="73f1c-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73f1c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f1c-132">-WhatIf</span></span>
<span data-ttu-id="73f1c-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="73f1c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73f1c-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73f1c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f1c-135">CommonParameters</span></span>
<span data-ttu-id="73f1c-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f1c-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f1c-138">입력</span><span class="sxs-lookup"><span data-stu-id="73f1c-138">INPUTS</span></span>

### <span data-ttu-id="73f1c-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="73f1c-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="73f1c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="73f1c-140">System.String</span></span>

## <span data-ttu-id="73f1c-141">출력</span><span class="sxs-lookup"><span data-stu-id="73f1c-141">OUTPUTS</span></span>

### <span data-ttu-id="73f1c-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="73f1c-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="73f1c-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="73f1c-143">NOTES</span></span>

## <span data-ttu-id="73f1c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73f1c-144">RELATED LINKS</span></span>
