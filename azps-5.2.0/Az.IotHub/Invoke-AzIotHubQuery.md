---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331869"
---
# <span data-ttu-id="d862c-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="d862c-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="d862c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d862c-102">SYNOPSIS</span></span>
<span data-ttu-id="d862c-103">강력한 SQL 같은 언어를 사용하여 IoT Hub를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="d862c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d862c-104">SYNTAX</span></span>

### <span data-ttu-id="d862c-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d862c-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d862c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d862c-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d862c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d862c-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d862c-108">설명</span><span class="sxs-lookup"><span data-stu-id="d862c-108">DESCRIPTION</span></span>
<span data-ttu-id="d862c-109">강력한 SQL 같은 언어를 사용하여 IoT Hub를 쿼리하여 디바이스 및 모듈 쌍, 작업 및 메시지 라우팅에 대한 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="d862c-110">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d862c-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="d862c-111">예제</span><span class="sxs-lookup"><span data-stu-id="d862c-111">EXAMPLES</span></span>

### <span data-ttu-id="d862c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d862c-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="d862c-113">Azure IoT Hub에서 모든 디바이스 쌍 데이터를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="d862c-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="d862c-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="d862c-115">대상 디바이스에서 상위 2개 모듈 쌍 데이터를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="d862c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d862c-116">PARAMETERS</span></span>

### <span data-ttu-id="d862c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d862c-117">-DefaultProfile</span></span>
<span data-ttu-id="d862c-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d862c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d862c-119">-InputObject</span></span>
<span data-ttu-id="d862c-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="d862c-120">IotHub object</span></span>

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

### <span data-ttu-id="d862c-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d862c-121">-IotHubName</span></span>
<span data-ttu-id="d862c-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="d862c-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d862c-123">-Query</span><span class="sxs-lookup"><span data-stu-id="d862c-123">-Query</span></span>
<span data-ttu-id="d862c-124">실행할 사용자 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-124">User query to be executed.</span></span>

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

### <span data-ttu-id="d862c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d862c-125">-ResourceGroupName</span></span>
<span data-ttu-id="d862c-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="d862c-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d862c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d862c-127">-ResourceId</span></span>
<span data-ttu-id="d862c-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d862c-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d862c-129">-Top</span><span class="sxs-lookup"><span data-stu-id="d862c-129">-Top</span></span>
<span data-ttu-id="d862c-130">반환할 최대 요소 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="d862c-131">기본적으로 쿼리에는 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-131">By default query has no cap.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d862c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d862c-132">-Confirm</span></span>
<span data-ttu-id="d862c-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d862c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d862c-134">-WhatIf</span></span>
<span data-ttu-id="d862c-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d862c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d862c-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d862c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d862c-137">CommonParameters</span></span>
<span data-ttu-id="d862c-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d862c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d862c-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d862c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d862c-140">입력</span><span class="sxs-lookup"><span data-stu-id="d862c-140">INPUTS</span></span>

### <span data-ttu-id="d862c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d862c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d862c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d862c-142">System.String</span></span>

## <span data-ttu-id="d862c-143">출력</span><span class="sxs-lookup"><span data-stu-id="d862c-143">OUTPUTS</span></span>

### <span data-ttu-id="d862c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d862c-144">System.String</span></span>

## <span data-ttu-id="d862c-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d862c-145">NOTES</span></span>

## <span data-ttu-id="d862c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d862c-146">RELATED LINKS</span></span>
