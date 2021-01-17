---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492016"
---
# <span data-ttu-id="c943a-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="c943a-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="c943a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c943a-102">SYNOPSIS</span></span>
<span data-ttu-id="c943a-103">디바이스 등록 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c943a-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="c943a-104">구문</span><span class="sxs-lookup"><span data-stu-id="c943a-104">SYNTAX</span></span>

### <span data-ttu-id="c943a-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c943a-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c943a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c943a-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c943a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c943a-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c943a-108">설명</span><span class="sxs-lookup"><span data-stu-id="c943a-108">DESCRIPTION</span></span>
<span data-ttu-id="c943a-109">등록 그룹의 세부 정보를 확인하거나 Azure IoT Hub Device Provisioning Service의 모든 등록 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c943a-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c943a-110">예제</span><span class="sxs-lookup"><span data-stu-id="c943a-110">EXAMPLES</span></span>

### <span data-ttu-id="c943a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c943a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="c943a-112">Azure IoT Hub Device Provisioning Service에서 디바이스 등록 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c943a-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="c943a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c943a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="c943a-114">Azure IoT Hub Device Provisioning Service의 모든 디바이스 등록 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c943a-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c943a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c943a-115">PARAMETERS</span></span>

### <span data-ttu-id="c943a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c943a-116">-DefaultProfile</span></span>
<span data-ttu-id="c943a-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c943a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c943a-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="c943a-118">-DpsName</span></span>
<span data-ttu-id="c943a-119">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="c943a-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c943a-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c943a-120">-DpsObject</span></span>
<span data-ttu-id="c943a-121">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="c943a-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c943a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c943a-122">-Name</span></span>
<span data-ttu-id="c943a-123">등록 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c943a-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="c943a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c943a-124">-ResourceGroupName</span></span>
<span data-ttu-id="c943a-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="c943a-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c943a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c943a-126">-ResourceId</span></span>
<span data-ttu-id="c943a-127">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c943a-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c943a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c943a-128">CommonParameters</span></span>
<span data-ttu-id="c943a-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c943a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c943a-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c943a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c943a-131">입력</span><span class="sxs-lookup"><span data-stu-id="c943a-131">INPUTS</span></span>

### <span data-ttu-id="c943a-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c943a-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c943a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c943a-133">System.String</span></span>

## <span data-ttu-id="c943a-134">출력</span><span class="sxs-lookup"><span data-stu-id="c943a-134">OUTPUTS</span></span>

### <span data-ttu-id="c943a-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="c943a-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="c943a-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span><span class="sxs-lookup"><span data-stu-id="c943a-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="c943a-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c943a-137">NOTES</span></span>

## <span data-ttu-id="c943a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c943a-138">RELATED LINKS</span></span>
