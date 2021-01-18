---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495380"
---
# <span data-ttu-id="e9ac1-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="e9ac1-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="e9ac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ac1-103">디바이스 쌍을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9ac1-103">Gets a device twin.</span></span>

## <span data-ttu-id="e9ac1-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9ac1-104">SYNTAX</span></span>

### <span data-ttu-id="e9ac1-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e9ac1-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9ac1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e9ac1-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9ac1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e9ac1-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9ac1-108">설명</span><span class="sxs-lookup"><span data-stu-id="e9ac1-108">DESCRIPTION</span></span>
<span data-ttu-id="e9ac1-109">디바이스 쌍을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9ac1-109">Gets a device twin.</span></span> <span data-ttu-id="e9ac1-110">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e9ac1-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="e9ac1-111">예제</span><span class="sxs-lookup"><span data-stu-id="e9ac1-111">EXAMPLES</span></span>

### <span data-ttu-id="e9ac1-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9ac1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="e9ac1-113">디바이스 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e9ac1-113">Returns the device twin object.</span></span>

## <span data-ttu-id="e9ac1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9ac1-114">PARAMETERS</span></span>

### <span data-ttu-id="e9ac1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ac1-115">-DefaultProfile</span></span>
<span data-ttu-id="e9ac1-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9ac1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9ac1-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e9ac1-117">-DeviceId</span></span>
<span data-ttu-id="e9ac1-118">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e9ac1-118">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ac1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9ac1-119">-InputObject</span></span>
<span data-ttu-id="e9ac1-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="e9ac1-120">IotHub object</span></span>

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

### <span data-ttu-id="e9ac1-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e9ac1-121">-IotHubName</span></span>
<span data-ttu-id="e9ac1-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="e9ac1-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e9ac1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9ac1-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9ac1-124">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e9ac1-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e9ac1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9ac1-125">-ResourceId</span></span>
<span data-ttu-id="e9ac1-126">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e9ac1-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e9ac1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ac1-127">CommonParameters</span></span>
<span data-ttu-id="e9ac1-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9ac1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ac1-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e9ac1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ac1-130">입력</span><span class="sxs-lookup"><span data-stu-id="e9ac1-130">INPUTS</span></span>

### <span data-ttu-id="e9ac1-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e9ac1-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e9ac1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e9ac1-132">System.String</span></span>

## <span data-ttu-id="e9ac1-133">출력</span><span class="sxs-lookup"><span data-stu-id="e9ac1-133">OUTPUTS</span></span>

### <span data-ttu-id="e9ac1-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="e9ac1-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="e9ac1-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9ac1-135">NOTES</span></span>

## <span data-ttu-id="e9ac1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9ac1-136">RELATED LINKS</span></span>
