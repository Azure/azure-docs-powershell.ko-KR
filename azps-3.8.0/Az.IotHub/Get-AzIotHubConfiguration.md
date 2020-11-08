---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033912"
---
# <span data-ttu-id="789b5-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="789b5-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="789b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="789b5-102">SYNOPSIS</span></span>
<span data-ttu-id="789b5-103">모든 또는 특정 IoT 자동 장치 관리 구성을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="789b5-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="789b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="789b5-104">SYNTAX</span></span>

### <span data-ttu-id="789b5-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="789b5-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="789b5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="789b5-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="789b5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="789b5-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="789b5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="789b5-108">DESCRIPTION</span></span>
<span data-ttu-id="789b5-109">Iot Hub에서 IoT 자동 장치 관리 구성에 대 한 세부 정보를 가져오거나 IoT 자동 장치 관리 구성을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="789b5-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="789b5-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="789b5-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="789b5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="789b5-111">EXAMPLES</span></span>

### <span data-ttu-id="789b5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="789b5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="789b5-113">IoT 자동 장치 관리 구성에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="789b5-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="789b5-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="789b5-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="789b5-115">IoT Hub에 IoT 자동 장치 관리 구성을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="789b5-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="789b5-116">변수</span><span class="sxs-lookup"><span data-stu-id="789b5-116">PARAMETERS</span></span>

### <span data-ttu-id="789b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789b5-117">-DefaultProfile</span></span>
<span data-ttu-id="789b5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="789b5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="789b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="789b5-119">-InputObject</span></span>
<span data-ttu-id="789b5-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="789b5-120">IotHub object</span></span>

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

### <span data-ttu-id="789b5-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="789b5-121">-IotHubName</span></span>
<span data-ttu-id="789b5-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="789b5-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="789b5-123">-이름</span><span class="sxs-lookup"><span data-stu-id="789b5-123">-Name</span></span>
<span data-ttu-id="789b5-124">구성의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="789b5-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="789b5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="789b5-125">-ResourceGroupName</span></span>
<span data-ttu-id="789b5-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="789b5-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="789b5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="789b5-127">-ResourceId</span></span>
<span data-ttu-id="789b5-128">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="789b5-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="789b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789b5-129">CommonParameters</span></span>
<span data-ttu-id="789b5-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="789b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789b5-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="789b5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789b5-132">입력</span><span class="sxs-lookup"><span data-stu-id="789b5-132">INPUTS</span></span>

### <span data-ttu-id="789b5-133">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="789b5-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="789b5-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="789b5-134">System.String</span></span>

## <span data-ttu-id="789b5-135">출력</span><span class="sxs-lookup"><span data-stu-id="789b5-135">OUTPUTS</span></span>

### <span data-ttu-id="789b5-136">IotHub에 대 한. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="789b5-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="789b5-137">IotHub. m a m a 구성 []</span><span class="sxs-lookup"><span data-stu-id="789b5-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="789b5-138">상속자</span><span class="sxs-lookup"><span data-stu-id="789b5-138">NOTES</span></span>

## <span data-ttu-id="789b5-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="789b5-139">RELATED LINKS</span></span>
