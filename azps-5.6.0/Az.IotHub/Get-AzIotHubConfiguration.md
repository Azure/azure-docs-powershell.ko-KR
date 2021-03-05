---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: b50d0b493243a07632403890d0324fefaba7dc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988120"
---
# <span data-ttu-id="1a4b3-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a4b3-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="1a4b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a4b3-102">SYNOPSIS</span></span>
<span data-ttu-id="1a4b3-103">전체 또는 특정 IoT 자동 디바이스 관리 구성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="1a4b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a4b3-104">SYNTAX</span></span>

### <span data-ttu-id="1a4b3-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1a4b3-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a4b3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1a4b3-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a4b3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1a4b3-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a4b3-108">설명</span><span class="sxs-lookup"><span data-stu-id="1a4b3-108">DESCRIPTION</span></span>
<span data-ttu-id="1a4b3-109">IoT 자동 디바이스 관리 구성에 대한 세부 정보를 얻거나 IoT Hub에서 IoT 자동 디바이스 관리 구성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="1a4b3-110">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="1a4b3-111">예제</span><span class="sxs-lookup"><span data-stu-id="1a4b3-111">EXAMPLES</span></span>

### <span data-ttu-id="1a4b3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a4b3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="1a4b3-113">IoT 자동 디바이스 관리 구성에 대한 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="1a4b3-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="1a4b3-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="1a4b3-115">IoT Hub에 IoT 자동 디바이스 관리 구성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="1a4b3-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a4b3-116">PARAMETERS</span></span>

### <span data-ttu-id="1a4b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a4b3-117">-DefaultProfile</span></span>
<span data-ttu-id="1a4b3-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a4b3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a4b3-119">-InputObject</span></span>
<span data-ttu-id="1a4b3-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="1a4b3-120">IotHub object</span></span>

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

### <span data-ttu-id="1a4b3-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1a4b3-121">-IotHubName</span></span>
<span data-ttu-id="1a4b3-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="1a4b3-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1a4b3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1a4b3-123">-Name</span></span>
<span data-ttu-id="1a4b3-124">구성에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="1a4b3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a4b3-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a4b3-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="1a4b3-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1a4b3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a4b3-127">-ResourceId</span></span>
<span data-ttu-id="1a4b3-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1a4b3-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1a4b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a4b3-129">CommonParameters</span></span>
<span data-ttu-id="1a4b3-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a4b3-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a4b3-132">입력</span><span class="sxs-lookup"><span data-stu-id="1a4b3-132">INPUTS</span></span>

### <span data-ttu-id="1a4b3-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1a4b3-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1a4b3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1a4b3-134">System.String</span></span>

## <span data-ttu-id="1a4b3-135">출력</span><span class="sxs-lookup"><span data-stu-id="1a4b3-135">OUTPUTS</span></span>

### <span data-ttu-id="1a4b3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a4b3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="1a4b3-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="1a4b3-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="1a4b3-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a4b3-138">NOTES</span></span>

## <span data-ttu-id="1a4b3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a4b3-139">RELATED LINKS</span></span>
