---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215515"
---
# <span data-ttu-id="441d7-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="441d7-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="441d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="441d7-102">SYNOPSIS</span></span>
<span data-ttu-id="441d7-103">장치 등록 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="441d7-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="441d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="441d7-104">SYNTAX</span></span>

### <span data-ttu-id="441d7-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="441d7-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="441d7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="441d7-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="441d7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="441d7-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="441d7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="441d7-108">DESCRIPTION</span></span>
<span data-ttu-id="441d7-109">Azure IoT Hub Device 프로비저닝 서비스에서 등록 그룹의 세부 정보를 가져오거나 모든 등록 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="441d7-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="441d7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="441d7-110">EXAMPLES</span></span>

### <span data-ttu-id="441d7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="441d7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="441d7-112">Azure IoT Hub 디바이스 프로비저닝 서비스에서 장치 등록 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="441d7-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="441d7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="441d7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="441d7-114">Azure IoT Hub 디바이스 프로비저닝 서비스의 모든 장치 등록 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="441d7-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="441d7-115">변수</span><span class="sxs-lookup"><span data-stu-id="441d7-115">PARAMETERS</span></span>

### <span data-ttu-id="441d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="441d7-116">-DefaultProfile</span></span>
<span data-ttu-id="441d7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="441d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="441d7-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="441d7-118">-DpsName</span></span>
<span data-ttu-id="441d7-119">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="441d7-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="441d7-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="441d7-120">-DpsObject</span></span>
<span data-ttu-id="441d7-121">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="441d7-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="441d7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="441d7-122">-Name</span></span>
<span data-ttu-id="441d7-123">등록 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="441d7-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="441d7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="441d7-124">-ResourceGroupName</span></span>
<span data-ttu-id="441d7-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="441d7-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="441d7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="441d7-126">-ResourceId</span></span>
<span data-ttu-id="441d7-127">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="441d7-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="441d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="441d7-128">CommonParameters</span></span>
<span data-ttu-id="441d7-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="441d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="441d7-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="441d7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="441d7-131">입력</span><span class="sxs-lookup"><span data-stu-id="441d7-131">INPUTS</span></span>

### <span data-ttu-id="441d7-132">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="441d7-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="441d7-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="441d7-133">System.String</span></span>

## <span data-ttu-id="441d7-134">출력</span><span class="sxs-lookup"><span data-stu-id="441d7-134">OUTPUTS</span></span>

### <span data-ttu-id="441d7-135">DeviceProvisioningServices. PSEnrollmentGroup/. \*</span><span class="sxs-lookup"><span data-stu-id="441d7-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="441d7-136">DeviceProvisioningServices를 PSEnrollmentGroups []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="441d7-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="441d7-137">상속자</span><span class="sxs-lookup"><span data-stu-id="441d7-137">NOTES</span></span>

## <span data-ttu-id="441d7-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="441d7-138">RELATED LINKS</span></span>
