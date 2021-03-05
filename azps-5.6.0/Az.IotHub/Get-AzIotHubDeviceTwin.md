---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 45966042a2c2c6a660f052280039204a1d5eb908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988031"
---
# <span data-ttu-id="13d5b-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="13d5b-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="13d5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="13d5b-103">디바이스 쌍을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13d5b-103">Gets a device twin.</span></span>

## <span data-ttu-id="13d5b-104">구문</span><span class="sxs-lookup"><span data-stu-id="13d5b-104">SYNTAX</span></span>

### <span data-ttu-id="13d5b-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="13d5b-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d5b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="13d5b-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d5b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="13d5b-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13d5b-108">설명</span><span class="sxs-lookup"><span data-stu-id="13d5b-108">DESCRIPTION</span></span>
<span data-ttu-id="13d5b-109">디바이스 쌍을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13d5b-109">Gets a device twin.</span></span> <span data-ttu-id="13d5b-110">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="13d5b-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="13d5b-111">예제</span><span class="sxs-lookup"><span data-stu-id="13d5b-111">EXAMPLES</span></span>

### <span data-ttu-id="13d5b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="13d5b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="13d5b-113">디바이스 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="13d5b-113">Returns the device twin object.</span></span>

## <span data-ttu-id="13d5b-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="13d5b-114">PARAMETERS</span></span>

### <span data-ttu-id="13d5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d5b-115">-DefaultProfile</span></span>
<span data-ttu-id="13d5b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13d5b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d5b-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="13d5b-117">-DeviceId</span></span>
<span data-ttu-id="13d5b-118">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="13d5b-118">Target Device Id.</span></span>

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

### <span data-ttu-id="13d5b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13d5b-119">-InputObject</span></span>
<span data-ttu-id="13d5b-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="13d5b-120">IotHub object</span></span>

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

### <span data-ttu-id="13d5b-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="13d5b-121">-IotHubName</span></span>
<span data-ttu-id="13d5b-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="13d5b-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="13d5b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d5b-123">-ResourceGroupName</span></span>
<span data-ttu-id="13d5b-124">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="13d5b-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="13d5b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13d5b-125">-ResourceId</span></span>
<span data-ttu-id="13d5b-126">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="13d5b-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="13d5b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d5b-127">CommonParameters</span></span>
<span data-ttu-id="13d5b-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13d5b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d5b-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="13d5b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d5b-130">입력</span><span class="sxs-lookup"><span data-stu-id="13d5b-130">INPUTS</span></span>

### <span data-ttu-id="13d5b-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="13d5b-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="13d5b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="13d5b-132">System.String</span></span>

## <span data-ttu-id="13d5b-133">출력</span><span class="sxs-lookup"><span data-stu-id="13d5b-133">OUTPUTS</span></span>

### <span data-ttu-id="13d5b-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="13d5b-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="13d5b-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13d5b-135">NOTES</span></span>

## <span data-ttu-id="13d5b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13d5b-136">RELATED LINKS</span></span>
