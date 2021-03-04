---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 6fff4be5fb4d0c8b76643e215dfda6d2f3d34ab8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975803"
---
# <span data-ttu-id="b6ec0-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b6ec0-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="b6ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ec0-103">Azure IoT Hub 디바이스 프로비전 서비스에 공유 액세스 정책의 세부 정보를 모두 나열하거나 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ec0-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b6ec0-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6ec0-104">SYNTAX</span></span>

### <span data-ttu-id="b6ec0-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b6ec0-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6ec0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b6ec0-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6ec0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b6ec0-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6ec0-108">설명</span><span class="sxs-lookup"><span data-stu-id="b6ec0-108">DESCRIPTION</span></span>
<span data-ttu-id="b6ec0-109">Azure IoT Hub 디바이스 프로비전 서비스에 대한 소개는 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b6ec0-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b6ec0-110">예제</span><span class="sxs-lookup"><span data-stu-id="b6ec0-110">EXAMPLES</span></span>

### <span data-ttu-id="b6ec0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6ec0-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="b6ec0-112">"myiotdps"에 모든 공유 액세스 정책을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ec0-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="b6ec0-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b6ec0-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="b6ec0-114">Azure IoT Hub 디바이스 프로비전 서비스에서 공유 액세스 정책 "mypolicy"에 대한 세부 정보를 보여 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b6ec0-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b6ec0-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6ec0-115">PARAMETERS</span></span>

### <span data-ttu-id="b6ec0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ec0-116">-DefaultProfile</span></span>
<span data-ttu-id="b6ec0-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ec0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6ec0-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="b6ec0-118">-DpsObject</span></span>
<span data-ttu-id="b6ec0-119">IoT 디바이스 프로비전 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="b6ec0-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="b6ec0-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b6ec0-120">-KeyName</span></span>
<span data-ttu-id="b6ec0-121">IoT Device Provisioning Service 액세스 정책 키 이름</span><span class="sxs-lookup"><span data-stu-id="b6ec0-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="b6ec0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b6ec0-122">-Name</span></span>
<span data-ttu-id="b6ec0-123">IoT 디바이스 프로비전 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="b6ec0-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b6ec0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ec0-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6ec0-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b6ec0-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b6ec0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6ec0-126">-ResourceId</span></span>
<span data-ttu-id="b6ec0-127">IoT 디바이스 프로비전 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b6ec0-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b6ec0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ec0-128">CommonParameters</span></span>
<span data-ttu-id="b6ec0-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ec0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ec0-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b6ec0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ec0-131">입력</span><span class="sxs-lookup"><span data-stu-id="b6ec0-131">INPUTS</span></span>

### <span data-ttu-id="b6ec0-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b6ec0-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="b6ec0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b6ec0-133">System.String</span></span>

## <span data-ttu-id="b6ec0-134">출력</span><span class="sxs-lookup"><span data-stu-id="b6ec0-134">OUTPUTS</span></span>

### <span data-ttu-id="b6ec0-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="b6ec0-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="b6ec0-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6ec0-136">NOTES</span></span>

## <span data-ttu-id="b6ec0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6ec0-137">RELATED LINKS</span></span>
