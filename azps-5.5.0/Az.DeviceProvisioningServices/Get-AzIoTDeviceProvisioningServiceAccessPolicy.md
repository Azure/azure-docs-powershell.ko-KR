---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 87c6bdd72229baec8e65c40d4e2e4309bde59aba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200425"
---
# <span data-ttu-id="45a4f-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="45a4f-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="45a4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="45a4f-103">Azure IoT Hub 디바이스 프로비저닝 서비스에서 공유 액세스 정책의 세부 정보를 모두 나열하거나 세부 정보를 보여 주면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="45a4f-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="45a4f-104">구문</span><span class="sxs-lookup"><span data-stu-id="45a4f-104">SYNTAX</span></span>

### <span data-ttu-id="45a4f-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="45a4f-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45a4f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="45a4f-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45a4f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="45a4f-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45a4f-108">설명</span><span class="sxs-lookup"><span data-stu-id="45a4f-108">DESCRIPTION</span></span>
<span data-ttu-id="45a4f-109">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="45a4f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="45a4f-110">예제</span><span class="sxs-lookup"><span data-stu-id="45a4f-110">EXAMPLES</span></span>

### <span data-ttu-id="45a4f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="45a4f-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="45a4f-112">"myiotdps"에 모든 공유 액세스 정책을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="45a4f-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="45a4f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="45a4f-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="45a4f-114">Azure IoT Hub 디바이스 프로비전 서비스에서 공유 액세스 정책 "mypolicy"에 대한 세부 정보를 보여 니다.</span><span class="sxs-lookup"><span data-stu-id="45a4f-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="45a4f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45a4f-115">PARAMETERS</span></span>

### <span data-ttu-id="45a4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a4f-116">-DefaultProfile</span></span>
<span data-ttu-id="45a4f-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45a4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45a4f-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="45a4f-118">-DpsObject</span></span>
<span data-ttu-id="45a4f-119">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="45a4f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="45a4f-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="45a4f-120">-KeyName</span></span>
<span data-ttu-id="45a4f-121">IoT Device Provisioning Service 액세스 정책 키 이름</span><span class="sxs-lookup"><span data-stu-id="45a4f-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="45a4f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="45a4f-122">-Name</span></span>
<span data-ttu-id="45a4f-123">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="45a4f-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="45a4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="45a4f-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="45a4f-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="45a4f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45a4f-126">-ResourceId</span></span>
<span data-ttu-id="45a4f-127">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="45a4f-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="45a4f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a4f-128">CommonParameters</span></span>
<span data-ttu-id="45a4f-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="45a4f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a4f-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="45a4f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a4f-131">입력</span><span class="sxs-lookup"><span data-stu-id="45a4f-131">INPUTS</span></span>

### <span data-ttu-id="45a4f-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="45a4f-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="45a4f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="45a4f-133">System.String</span></span>

## <span data-ttu-id="45a4f-134">출력</span><span class="sxs-lookup"><span data-stu-id="45a4f-134">OUTPUTS</span></span>

### <span data-ttu-id="45a4f-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="45a4f-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="45a4f-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="45a4f-136">NOTES</span></span>

## <span data-ttu-id="45a4f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45a4f-137">RELATED LINKS</span></span>
