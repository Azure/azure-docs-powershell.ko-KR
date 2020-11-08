---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213558"
---
# <span data-ttu-id="fe9af-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="fe9af-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="fe9af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe9af-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9af-103">전체 또는 특정 IoT Edge 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9af-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="fe9af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe9af-104">SYNTAX</span></span>

### <span data-ttu-id="fe9af-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fe9af-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe9af-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe9af-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe9af-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fe9af-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe9af-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fe9af-108">DESCRIPTION</span></span>
<span data-ttu-id="fe9af-109">Iot Hub에서 iot edge 배포 또는 목록 IoT Edge 배포에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe9af-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="fe9af-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fe9af-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="fe9af-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fe9af-111">EXAMPLES</span></span>

### <span data-ttu-id="fe9af-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fe9af-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="fe9af-113">IoT Edge 배포에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe9af-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="fe9af-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="fe9af-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="fe9af-115">IoT Hub의 모든 IoT Edge 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9af-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="fe9af-116">변수</span><span class="sxs-lookup"><span data-stu-id="fe9af-116">PARAMETERS</span></span>

### <span data-ttu-id="fe9af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9af-117">-DefaultProfile</span></span>
<span data-ttu-id="fe9af-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe9af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe9af-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe9af-119">-InputObject</span></span>
<span data-ttu-id="fe9af-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="fe9af-120">IotHub object</span></span>

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

### <span data-ttu-id="fe9af-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fe9af-121">-IotHubName</span></span>
<span data-ttu-id="fe9af-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="fe9af-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fe9af-123">-이름</span><span class="sxs-lookup"><span data-stu-id="fe9af-123">-Name</span></span>
<span data-ttu-id="fe9af-124">배포의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fe9af-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="fe9af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9af-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe9af-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe9af-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fe9af-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe9af-127">-ResourceId</span></span>
<span data-ttu-id="fe9af-128">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="fe9af-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fe9af-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9af-129">CommonParameters</span></span>
<span data-ttu-id="fe9af-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9af-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9af-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe9af-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9af-132">입력</span><span class="sxs-lookup"><span data-stu-id="fe9af-132">INPUTS</span></span>

### <span data-ttu-id="fe9af-133">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="fe9af-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fe9af-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fe9af-134">System.String</span></span>

## <span data-ttu-id="fe9af-135">출력</span><span class="sxs-lookup"><span data-stu-id="fe9af-135">OUTPUTS</span></span>

### <span data-ttu-id="fe9af-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="fe9af-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="fe9af-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="fe9af-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="fe9af-138">상속자</span><span class="sxs-lookup"><span data-stu-id="fe9af-138">NOTES</span></span>

## <span data-ttu-id="fe9af-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe9af-139">RELATED LINKS</span></span>
