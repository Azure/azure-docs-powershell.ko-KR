---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188228"
---
# <span data-ttu-id="ee9c2-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee9c2-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="ee9c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9c2-103">전체 또는 특정 IoT 자동 디바이스 관리 구성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ee9c2-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="ee9c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee9c2-104">SYNTAX</span></span>

### <span data-ttu-id="ee9c2-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ee9c2-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee9c2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ee9c2-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee9c2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ee9c2-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee9c2-108">설명</span><span class="sxs-lookup"><span data-stu-id="ee9c2-108">DESCRIPTION</span></span>
<span data-ttu-id="ee9c2-109">IoT 자동 디바이스 관리 구성의 세부 정보를 확인하거나 IoT Hub에 IoT 자동 디바이스 관리 구성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ee9c2-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="ee9c2-110">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ee9c2-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="ee9c2-111">예제</span><span class="sxs-lookup"><span data-stu-id="ee9c2-111">EXAMPLES</span></span>

### <span data-ttu-id="ee9c2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee9c2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="ee9c2-113">IoT 자동 디바이스 관리 구성의 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ee9c2-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="ee9c2-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ee9c2-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="ee9c2-115">IoT Hub에서 IoT 자동 디바이스 관리 구성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ee9c2-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="ee9c2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee9c2-116">PARAMETERS</span></span>

### <span data-ttu-id="ee9c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee9c2-117">-DefaultProfile</span></span>
<span data-ttu-id="ee9c2-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee9c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee9c2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee9c2-119">-InputObject</span></span>
<span data-ttu-id="ee9c2-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="ee9c2-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9c2-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ee9c2-121">-IotHubName</span></span>
<span data-ttu-id="ee9c2-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="ee9c2-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ee9c2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ee9c2-123">-Name</span></span>
<span data-ttu-id="ee9c2-124">구성에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ee9c2-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="ee9c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee9c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="ee9c2-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="ee9c2-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ee9c2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee9c2-127">-ResourceId</span></span>
<span data-ttu-id="ee9c2-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ee9c2-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ee9c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9c2-129">CommonParameters</span></span>
<span data-ttu-id="ee9c2-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee9c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9c2-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ee9c2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9c2-132">입력</span><span class="sxs-lookup"><span data-stu-id="ee9c2-132">INPUTS</span></span>

### <span data-ttu-id="ee9c2-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ee9c2-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ee9c2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ee9c2-134">System.String</span></span>

## <span data-ttu-id="ee9c2-135">출력</span><span class="sxs-lookup"><span data-stu-id="ee9c2-135">OUTPUTS</span></span>

### <span data-ttu-id="ee9c2-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee9c2-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="ee9c2-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="ee9c2-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="ee9c2-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee9c2-138">NOTES</span></span>

## <span data-ttu-id="ee9c2-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee9c2-139">RELATED LINKS</span></span>
