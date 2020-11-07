---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f978e6c0a496273535551663a442989b2ab1648e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700927"
---
# <span data-ttu-id="d7bfa-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d7bfa-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="d7bfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bfa-103">Azure IoT Hub device 프로비저닝 서비스의 공유 액세스 정책에 대 한 세부 정보를 모두 나열 하거나 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d7bfa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7bfa-104">SYNTAX</span></span>

### <span data-ttu-id="d7bfa-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d7bfa-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7bfa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d7bfa-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7bfa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d7bfa-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7bfa-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d7bfa-108">DESCRIPTION</span></span>
<span data-ttu-id="d7bfa-109">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d7bfa-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d7bfa-110">EXAMPLES</span></span>

### <span data-ttu-id="d7bfa-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7bfa-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="d7bfa-112">"Myiotdps"의 모든 공유 액세스 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="d7bfa-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d7bfa-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="d7bfa-114">Azure IoT Hub 디바이스 프로비저닝 서비스에서 공유 액세스 정책의 "mypolicy"에 대 한 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d7bfa-115">변수</span><span class="sxs-lookup"><span data-stu-id="d7bfa-115">PARAMETERS</span></span>

### <span data-ttu-id="d7bfa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bfa-116">-DefaultProfile</span></span>
<span data-ttu-id="d7bfa-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7bfa-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d7bfa-118">-DpsObject</span></span>
<span data-ttu-id="d7bfa-119">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="d7bfa-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d7bfa-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d7bfa-120">-KeyName</span></span>
<span data-ttu-id="d7bfa-121">IoT Device 프로 비전 서비스 액세스 정책 키 이름</span><span class="sxs-lookup"><span data-stu-id="d7bfa-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="d7bfa-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d7bfa-122">-Name</span></span>
<span data-ttu-id="d7bfa-123">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="d7bfa-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d7bfa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bfa-124">-ResourceGroupName</span></span>
<span data-ttu-id="d7bfa-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d7bfa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7bfa-126">-ResourceId</span></span>
<span data-ttu-id="d7bfa-127">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d7bfa-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d7bfa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bfa-128">CommonParameters</span></span>
<span data-ttu-id="d7bfa-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bfa-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7bfa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bfa-131">입력</span><span class="sxs-lookup"><span data-stu-id="d7bfa-131">INPUTS</span></span>

### <span data-ttu-id="d7bfa-132">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="d7bfa-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d7bfa-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d7bfa-133">System.String</span></span>

## <span data-ttu-id="d7bfa-134">출력</span><span class="sxs-lookup"><span data-stu-id="d7bfa-134">OUTPUTS</span></span>

### <span data-ttu-id="d7bfa-135">DeviceProvisioningServices. Pssharedaccess서명 Authorizationrule를 Accessrightsdescription</span><span class="sxs-lookup"><span data-stu-id="d7bfa-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="d7bfa-136">상속자</span><span class="sxs-lookup"><span data-stu-id="d7bfa-136">NOTES</span></span>

## <span data-ttu-id="d7bfa-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7bfa-137">RELATED LINKS</span></span>
