---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 9b6c9b77ae29214c7d998e3d2c859e4ac7521db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211746"
---
# <span data-ttu-id="5e849-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e849-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="5e849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e849-102">SYNOPSIS</span></span>
<span data-ttu-id="5e849-103">구성 등록의 변경 가능한 필드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="5e849-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e849-104">SYNTAX</span></span>

### <span data-ttu-id="5e849-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5e849-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e849-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5e849-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e849-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5e849-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e849-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5e849-108">DESCRIPTION</span></span>
<span data-ttu-id="5e849-109">IoT 자동 장치 관리 구성의 지정 된 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="5e849-110">참고: 구성 콘텐츠는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="5e849-111">업데이트할 수 있는 구성 속성은 ' 레이블 ', ' 메트릭 ', ' priority ' 및 ' targetCondition '입니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="5e849-112"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5e849-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="5e849-113">예제의</span><span class="sxs-lookup"><span data-stu-id="5e849-113">EXAMPLES</span></span>

### <span data-ttu-id="5e849-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="5e849-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="5e849-115">장치 구성의 우선 순위 변경 및 해당 대상 상태 업데이트</span><span class="sxs-lookup"><span data-stu-id="5e849-115">Alter the priority of a device configuration and update its target condition</span></span>

## <span data-ttu-id="5e849-116">변수</span><span class="sxs-lookup"><span data-stu-id="5e849-116">PARAMETERS</span></span>

### <span data-ttu-id="5e849-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e849-117">-DefaultProfile</span></span>
<span data-ttu-id="5e849-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e849-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5e849-119">-Force</span></span>
<span data-ttu-id="5e849-120">마지막으로 검색 한 후에 업데이트 된 경우에도 구성 개체를 바꿀 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-120">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e849-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e849-121">-InputObject</span></span>
<span data-ttu-id="5e849-122">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="5e849-122">IotHub object</span></span>

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

### <span data-ttu-id="5e849-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5e849-123">-IotHubName</span></span>
<span data-ttu-id="5e849-124">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="5e849-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5e849-125">-레이블</span><span class="sxs-lookup"><span data-stu-id="5e849-125">-Label</span></span>
<span data-ttu-id="5e849-126">대상 구성에 적용 되는 레이블의 맵입니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-126">Map of labels to be applied to target configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e849-127">-미터법</span><span class="sxs-lookup"><span data-stu-id="5e849-127">-Metric</span></span>
<span data-ttu-id="5e849-128">구성 메트릭 정의에 대 한 쿼리 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-128">Queries collection for configuration metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e849-129">-이름</span><span class="sxs-lookup"><span data-stu-id="5e849-129">-Name</span></span>
<span data-ttu-id="5e849-130">구성의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="5e849-131">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="5e849-131">-Priority</span></span>
<span data-ttu-id="5e849-132">경합 하는 규칙 (최고 wins)에 대 한 장치 구성의 가중치.</span><span class="sxs-lookup"><span data-stu-id="5e849-132">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="5e849-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e849-133">-ResourceGroupName</span></span>
<span data-ttu-id="5e849-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5e849-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e849-135">-ResourceId</span></span>
<span data-ttu-id="5e849-136">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="5e849-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5e849-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="5e849-137">-TargetCondition</span></span>
<span data-ttu-id="5e849-138">장치 구성이 적용 되는 대상 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-138">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="5e849-139">-확인</span><span class="sxs-lookup"><span data-stu-id="5e849-139">-Confirm</span></span>
<span data-ttu-id="5e849-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e849-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e849-141">-WhatIf</span></span>
<span data-ttu-id="5e849-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e849-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e849-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e849-144">CommonParameters</span></span>
<span data-ttu-id="5e849-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e849-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e849-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e849-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e849-147">입력</span><span class="sxs-lookup"><span data-stu-id="5e849-147">INPUTS</span></span>

### <span data-ttu-id="5e849-148">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="5e849-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5e849-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5e849-149">System.String</span></span>

## <span data-ttu-id="5e849-150">출력</span><span class="sxs-lookup"><span data-stu-id="5e849-150">OUTPUTS</span></span>

### <span data-ttu-id="5e849-151">IotHub에 대 한. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e849-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="5e849-152">상속자</span><span class="sxs-lookup"><span data-stu-id="5e849-152">NOTES</span></span>

## <span data-ttu-id="5e849-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e849-153">RELATED LINKS</span></span>
