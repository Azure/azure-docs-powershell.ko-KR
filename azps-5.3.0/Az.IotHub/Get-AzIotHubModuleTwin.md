---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495365"
---
# <span data-ttu-id="fc31b-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="fc31b-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="fc31b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc31b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc31b-103">IoT 디바이스 모듈 쌍을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fc31b-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="fc31b-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc31b-104">SYNTAX</span></span>

### <span data-ttu-id="fc31b-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fc31b-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc31b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc31b-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc31b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc31b-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc31b-108">설명</span><span class="sxs-lookup"><span data-stu-id="fc31b-108">DESCRIPTION</span></span>
<span data-ttu-id="fc31b-109">IoT 디바이스 모듈 쌍을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fc31b-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="fc31b-110">자세한 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc31b-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="fc31b-111">예제</span><span class="sxs-lookup"><span data-stu-id="fc31b-111">EXAMPLES</span></span>

### <span data-ttu-id="fc31b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fc31b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="fc31b-113">디바이스 모듈 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fc31b-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="fc31b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc31b-114">PARAMETERS</span></span>

### <span data-ttu-id="fc31b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc31b-115">-DefaultProfile</span></span>
<span data-ttu-id="fc31b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc31b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc31b-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fc31b-117">-DeviceId</span></span>
<span data-ttu-id="fc31b-118">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc31b-118">Target Device Id.</span></span>

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

### <span data-ttu-id="fc31b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc31b-119">-InputObject</span></span>
<span data-ttu-id="fc31b-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="fc31b-120">IotHub object</span></span>

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

### <span data-ttu-id="fc31b-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fc31b-121">-IotHubName</span></span>
<span data-ttu-id="fc31b-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="fc31b-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fc31b-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="fc31b-123">-ModuleId</span></span>
<span data-ttu-id="fc31b-124">대상 모듈 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc31b-124">Target Module Id.</span></span>

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

### <span data-ttu-id="fc31b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc31b-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc31b-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="fc31b-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fc31b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc31b-127">-ResourceId</span></span>
<span data-ttu-id="fc31b-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fc31b-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fc31b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc31b-129">CommonParameters</span></span>
<span data-ttu-id="fc31b-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc31b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc31b-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc31b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc31b-132">입력</span><span class="sxs-lookup"><span data-stu-id="fc31b-132">INPUTS</span></span>

### <span data-ttu-id="fc31b-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fc31b-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fc31b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fc31b-134">System.String</span></span>

## <span data-ttu-id="fc31b-135">출력</span><span class="sxs-lookup"><span data-stu-id="fc31b-135">OUTPUTS</span></span>

### <span data-ttu-id="fc31b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="fc31b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="fc31b-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc31b-137">NOTES</span></span>

## <span data-ttu-id="fc31b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc31b-138">RELATED LINKS</span></span>
