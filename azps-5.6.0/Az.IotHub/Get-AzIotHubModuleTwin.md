---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 915fdf5bd0e53e7e8ed2817d83438597d515007d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987933"
---
# <span data-ttu-id="8aa62-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="8aa62-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="8aa62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa62-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa62-103">IoT 디바이스 모듈 쌍을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa62-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="8aa62-104">구문</span><span class="sxs-lookup"><span data-stu-id="8aa62-104">SYNTAX</span></span>

### <span data-ttu-id="8aa62-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8aa62-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa62-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8aa62-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa62-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8aa62-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aa62-108">설명</span><span class="sxs-lookup"><span data-stu-id="8aa62-108">DESCRIPTION</span></span>
<span data-ttu-id="8aa62-109">IoT 디바이스 모듈 쌍을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa62-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="8aa62-110">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8aa62-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="8aa62-111">예제</span><span class="sxs-lookup"><span data-stu-id="8aa62-111">EXAMPLES</span></span>

### <span data-ttu-id="8aa62-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8aa62-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="8aa62-113">디바이스 모듈 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa62-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="8aa62-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8aa62-114">PARAMETERS</span></span>

### <span data-ttu-id="8aa62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa62-115">-DefaultProfile</span></span>
<span data-ttu-id="8aa62-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa62-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aa62-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8aa62-117">-DeviceId</span></span>
<span data-ttu-id="8aa62-118">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa62-118">Target Device Id.</span></span>

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

### <span data-ttu-id="8aa62-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8aa62-119">-InputObject</span></span>
<span data-ttu-id="8aa62-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="8aa62-120">IotHub object</span></span>

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

### <span data-ttu-id="8aa62-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8aa62-121">-IotHubName</span></span>
<span data-ttu-id="8aa62-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="8aa62-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8aa62-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="8aa62-123">-ModuleId</span></span>
<span data-ttu-id="8aa62-124">대상 모듈 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa62-124">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa62-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa62-125">-ResourceGroupName</span></span>
<span data-ttu-id="8aa62-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="8aa62-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8aa62-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8aa62-127">-ResourceId</span></span>
<span data-ttu-id="8aa62-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="8aa62-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8aa62-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa62-129">CommonParameters</span></span>
<span data-ttu-id="8aa62-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa62-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa62-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8aa62-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa62-132">입력</span><span class="sxs-lookup"><span data-stu-id="8aa62-132">INPUTS</span></span>

### <span data-ttu-id="8aa62-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8aa62-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8aa62-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8aa62-134">System.String</span></span>

## <span data-ttu-id="8aa62-135">출력</span><span class="sxs-lookup"><span data-stu-id="8aa62-135">OUTPUTS</span></span>

### <span data-ttu-id="8aa62-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="8aa62-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="8aa62-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8aa62-137">NOTES</span></span>

## <span data-ttu-id="8aa62-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8aa62-138">RELATED LINKS</span></span>
