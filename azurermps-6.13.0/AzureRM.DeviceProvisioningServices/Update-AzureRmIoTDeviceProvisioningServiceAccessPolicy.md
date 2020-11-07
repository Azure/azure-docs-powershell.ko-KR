---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f5d750dc795619f32f6c4f16a5fe1e3b5e111106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711378"
---
# <span data-ttu-id="d6b72-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d6b72-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="d6b72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6b72-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b72-103">Azure IoT Hub 디바이스 프로비저닝 서비스에서 공유 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b72-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6b72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6b72-104">SYNTAX</span></span>

### <span data-ttu-id="d6b72-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6b72-105">ResourceSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6b72-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d6b72-106">InputObjectSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b72-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d6b72-107">ResourceIdSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6b72-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d6b72-108">DESCRIPTION</span></span>
<span data-ttu-id="d6b72-109">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6b72-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d6b72-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d6b72-110">EXAMPLES</span></span>

### <span data-ttu-id="d6b72-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d6b72-111">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="d6b72-112">EnrollmentWrite 권한이 있는 Azure IoT Hub 디바이스 프로비저닝 서비스에서 액세스 정책 "mypolicy"을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b72-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="d6b72-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d6b72-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzureRmIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="d6b72-114">파이프라인을 사용 하 여 EnrollmentWrite 권한이 있는 Azure IoT Hub 디바이스 프로비저닝 서비스에서 액세스 정책 "mypolicy"을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b72-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="d6b72-115">변수</span><span class="sxs-lookup"><span data-stu-id="d6b72-115">PARAMETERS</span></span>

### <span data-ttu-id="d6b72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b72-116">-DefaultProfile</span></span>
<span data-ttu-id="d6b72-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6b72-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6b72-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6b72-118">-InputObject</span></span>
<span data-ttu-id="d6b72-119">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="d6b72-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d6b72-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d6b72-120">-KeyName</span></span>
<span data-ttu-id="d6b72-121">IoT Device 프로 비전 서비스 액세스 정책 키 이름</span><span class="sxs-lookup"><span data-stu-id="d6b72-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="d6b72-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d6b72-122">-Name</span></span>
<span data-ttu-id="d6b72-123">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="d6b72-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d6b72-124">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="d6b72-124">-Permissions</span></span>
<span data-ttu-id="d6b72-125">IoT Device 프로 비전 서비스 액세스 정책 사용 권한</span><span class="sxs-lookup"><span data-stu-id="d6b72-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="d6b72-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b72-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6b72-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6b72-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d6b72-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6b72-128">-ResourceId</span></span>
<span data-ttu-id="d6b72-129">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d6b72-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d6b72-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d6b72-130">-Confirm</span></span>
<span data-ttu-id="d6b72-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b72-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6b72-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6b72-132">-WhatIf</span></span>
<span data-ttu-id="d6b72-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6b72-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6b72-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6b72-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6b72-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b72-135">CommonParameters</span></span>
<span data-ttu-id="d6b72-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b72-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b72-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6b72-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b72-138">입력</span><span class="sxs-lookup"><span data-stu-id="d6b72-138">INPUTS</span></span>

### <span data-ttu-id="d6b72-139">DeviceProvisioningServices. Pssharedaccess서명 Authorizationrule를 Accessrightsdescription</span><span class="sxs-lookup"><span data-stu-id="d6b72-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="d6b72-140">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d6b72-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d6b72-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d6b72-141">System.String</span></span>

## <span data-ttu-id="d6b72-142">출력</span><span class="sxs-lookup"><span data-stu-id="d6b72-142">OUTPUTS</span></span>

### <span data-ttu-id="d6b72-143">DeviceProvisioningServices. Pssharedaccess서명 Authorizationrule를 Accessrightsdescription</span><span class="sxs-lookup"><span data-stu-id="d6b72-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="d6b72-144">상속자</span><span class="sxs-lookup"><span data-stu-id="d6b72-144">NOTES</span></span>

## <span data-ttu-id="d6b72-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6b72-145">RELATED LINKS</span></span>
