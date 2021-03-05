---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 4c4a9259f80360cfa8947035e84368ca18ed77d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988106"
---
# <span data-ttu-id="927f6-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="927f6-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="927f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="927f6-102">SYNOPSIS</span></span>
<span data-ttu-id="927f6-103">전체 또는 특정 IoT Edge 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="927f6-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="927f6-104">구문</span><span class="sxs-lookup"><span data-stu-id="927f6-104">SYNTAX</span></span>

### <span data-ttu-id="927f6-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="927f6-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="927f6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="927f6-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="927f6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="927f6-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="927f6-108">설명</span><span class="sxs-lookup"><span data-stu-id="927f6-108">DESCRIPTION</span></span>
<span data-ttu-id="927f6-109">IoT Hub에서 IoT Edge 배포 또는 IoT Edge 배포 나열에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="927f6-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="927f6-110">자세한 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="927f6-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="927f6-111">예제</span><span class="sxs-lookup"><span data-stu-id="927f6-111">EXAMPLES</span></span>

### <span data-ttu-id="927f6-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="927f6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="927f6-113">IoT Edge 배포에 대한 세부 정보를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="927f6-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="927f6-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="927f6-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="927f6-115">IoT Hub에 모든 IoT Edge 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="927f6-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="927f6-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="927f6-116">PARAMETERS</span></span>

### <span data-ttu-id="927f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="927f6-117">-DefaultProfile</span></span>
<span data-ttu-id="927f6-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="927f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="927f6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="927f6-119">-InputObject</span></span>
<span data-ttu-id="927f6-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="927f6-120">IotHub object</span></span>

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

### <span data-ttu-id="927f6-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="927f6-121">-IotHubName</span></span>
<span data-ttu-id="927f6-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="927f6-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="927f6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="927f6-123">-Name</span></span>
<span data-ttu-id="927f6-124">배포의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="927f6-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="927f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="927f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="927f6-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="927f6-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="927f6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="927f6-127">-ResourceId</span></span>
<span data-ttu-id="927f6-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="927f6-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="927f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927f6-129">CommonParameters</span></span>
<span data-ttu-id="927f6-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="927f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927f6-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="927f6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927f6-132">입력</span><span class="sxs-lookup"><span data-stu-id="927f6-132">INPUTS</span></span>

### <span data-ttu-id="927f6-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="927f6-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="927f6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="927f6-134">System.String</span></span>

## <span data-ttu-id="927f6-135">출력</span><span class="sxs-lookup"><span data-stu-id="927f6-135">OUTPUTS</span></span>

### <span data-ttu-id="927f6-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDMicrosoft.Azure.Commands.Management.IotHub.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="927f6-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="927f6-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span><span class="sxs-lookup"><span data-stu-id="927f6-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="927f6-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="927f6-138">NOTES</span></span>

## <span data-ttu-id="927f6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="927f6-139">RELATED LINKS</span></span>
