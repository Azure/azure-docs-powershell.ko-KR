---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226973"
---
# <span data-ttu-id="d704d-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="d704d-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="d704d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d704d-102">SYNOPSIS</span></span>
<span data-ttu-id="d704d-103">강력한 SQL과 같은 언어를 사용 하 여 IoT Hub를 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="d704d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d704d-104">SYNTAX</span></span>

### <span data-ttu-id="d704d-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d704d-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d704d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d704d-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d704d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d704d-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d704d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d704d-108">DESCRIPTION</span></span>
<span data-ttu-id="d704d-109">강력한 SQL과 같은 언어를 사용 하 여 IoT Hub를 쿼리하여 장치 및 모듈 twins, 작업 및 메시지 라우팅과 관련 된 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="d704d-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d704d-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="d704d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d704d-111">EXAMPLES</span></span>

### <span data-ttu-id="d704d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d704d-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="d704d-113">Azure IoT Hub의 모든 장치 트윈 데이터를 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="d704d-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="d704d-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="d704d-115">쿼리 상위 2 모듈 대상 장치에서 데이터를 트윈 합니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="d704d-116">변수</span><span class="sxs-lookup"><span data-stu-id="d704d-116">PARAMETERS</span></span>

### <span data-ttu-id="d704d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d704d-117">-DefaultProfile</span></span>
<span data-ttu-id="d704d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d704d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d704d-119">-InputObject</span></span>
<span data-ttu-id="d704d-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="d704d-120">IotHub object</span></span>

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

### <span data-ttu-id="d704d-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d704d-121">-IotHubName</span></span>
<span data-ttu-id="d704d-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="d704d-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d704d-123">-쿼리</span><span class="sxs-lookup"><span data-stu-id="d704d-123">-Query</span></span>
<span data-ttu-id="d704d-124">실행할 사용자 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-124">User query to be executed.</span></span>

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

### <span data-ttu-id="d704d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d704d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d704d-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d704d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d704d-127">-ResourceId</span></span>
<span data-ttu-id="d704d-128">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d704d-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d704d-129">-위쪽</span><span class="sxs-lookup"><span data-stu-id="d704d-129">-Top</span></span>
<span data-ttu-id="d704d-130">반환할 요소의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="d704d-131">기본적으로 쿼리에는 cap가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="d704d-132">-확인</span><span class="sxs-lookup"><span data-stu-id="d704d-132">-Confirm</span></span>
<span data-ttu-id="d704d-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d704d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d704d-134">-WhatIf</span></span>
<span data-ttu-id="d704d-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d704d-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d704d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d704d-137">CommonParameters</span></span>
<span data-ttu-id="d704d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d704d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d704d-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d704d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d704d-140">입력</span><span class="sxs-lookup"><span data-stu-id="d704d-140">INPUTS</span></span>

### <span data-ttu-id="d704d-141">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="d704d-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d704d-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d704d-142">System.String</span></span>

## <span data-ttu-id="d704d-143">출력</span><span class="sxs-lookup"><span data-stu-id="d704d-143">OUTPUTS</span></span>

### <span data-ttu-id="d704d-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d704d-144">System.String</span></span>

## <span data-ttu-id="d704d-145">상속자</span><span class="sxs-lookup"><span data-stu-id="d704d-145">NOTES</span></span>

## <span data-ttu-id="d704d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d704d-146">RELATED LINKS</span></span>
