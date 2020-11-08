---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048307"
---
# <span data-ttu-id="c15cf-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c15cf-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="c15cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c15cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c15cf-103">Azure IoT Hub 디바이스 프로비저닝 서비스에서 새 공유 액세스 정책을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15cf-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c15cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c15cf-104">SYNTAX</span></span>

### <span data-ttu-id="c15cf-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c15cf-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c15cf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c15cf-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c15cf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c15cf-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c15cf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c15cf-108">DESCRIPTION</span></span>
<span data-ttu-id="c15cf-109">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="c15cf-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c15cf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c15cf-110">EXAMPLES</span></span>

### <span data-ttu-id="c15cf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c15cf-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="c15cf-112">Azure IoT Hub 디바이스 프로 비전 서비스에서 EnrollmentWrite 및 ServiceConfig 권한이 있는 새 공유 액세스 정책을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15cf-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="c15cf-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c15cf-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="c15cf-114">Azure IoT Hub device 프로비저닝 서비스에서 EnrollmentRead 권한이 있는 새 공유 액세스 정책을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15cf-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="c15cf-115">변수</span><span class="sxs-lookup"><span data-stu-id="c15cf-115">PARAMETERS</span></span>

### <span data-ttu-id="c15cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c15cf-116">-DefaultProfile</span></span>
<span data-ttu-id="c15cf-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c15cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c15cf-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c15cf-118">-DpsObject</span></span>
<span data-ttu-id="c15cf-119">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="c15cf-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c15cf-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c15cf-120">-KeyName</span></span>
<span data-ttu-id="c15cf-121">IoT Device 프로 비전 서비스 액세스 정책 키 이름</span><span class="sxs-lookup"><span data-stu-id="c15cf-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="c15cf-122">-이름</span><span class="sxs-lookup"><span data-stu-id="c15cf-122">-Name</span></span>
<span data-ttu-id="c15cf-123">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="c15cf-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c15cf-124">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="c15cf-124">-Permissions</span></span>
<span data-ttu-id="c15cf-125">IoT Device 프로 비전 서비스 액세스 정책 사용 권한</span><span class="sxs-lookup"><span data-stu-id="c15cf-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="c15cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c15cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="c15cf-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c15cf-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c15cf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c15cf-128">-ResourceId</span></span>
<span data-ttu-id="c15cf-129">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c15cf-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c15cf-130">-확인</span><span class="sxs-lookup"><span data-stu-id="c15cf-130">-Confirm</span></span>
<span data-ttu-id="c15cf-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c15cf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c15cf-132">-WhatIf</span></span>
<span data-ttu-id="c15cf-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c15cf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c15cf-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c15cf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c15cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15cf-135">CommonParameters</span></span>
<span data-ttu-id="c15cf-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15cf-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c15cf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15cf-138">입력</span><span class="sxs-lookup"><span data-stu-id="c15cf-138">INPUTS</span></span>

### <span data-ttu-id="c15cf-139">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="c15cf-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c15cf-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c15cf-140">System.String</span></span>

## <span data-ttu-id="c15cf-141">출력</span><span class="sxs-lookup"><span data-stu-id="c15cf-141">OUTPUTS</span></span>

### <span data-ttu-id="c15cf-142">DeviceProvisioningServices. Pssharedaccess서명 Authorizationrule를 Accessrightsdescription</span><span class="sxs-lookup"><span data-stu-id="c15cf-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="c15cf-143">상속자</span><span class="sxs-lookup"><span data-stu-id="c15cf-143">NOTES</span></span>

## <span data-ttu-id="c15cf-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c15cf-144">RELATED LINKS</span></span>
