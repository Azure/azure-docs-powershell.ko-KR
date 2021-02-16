---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 5f2dfec045364852d9846fa3bb35bd903c78ca5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187921"
---
# <span data-ttu-id="ec30e-101">Get-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ec30e-101">Get-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="ec30e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec30e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec30e-103">대역폭 일정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec30e-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="ec30e-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec30e-104">SYNTAX</span></span>

### <span data-ttu-id="ec30e-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ec30e-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec30e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec30e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec30e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec30e-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec30e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec30e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="ec30e-109">설명</span><span class="sxs-lookup"><span data-stu-id="ec30e-109">DESCRIPTION</span></span>
<span data-ttu-id="ec30e-110">**Get-AzStackEdgeBandwidthSchedule** cmdlet은 대역폭 일정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec30e-110">The **Get-AzStackEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="ec30e-111">리소스 그룹 이름 및 디바이스 이름과 함께 일정 이름을 지정하여 특정 대역폭 일정에 대한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec30e-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="ec30e-112">예제</span><span class="sxs-lookup"><span data-stu-id="ec30e-112">EXAMPLES</span></span>

### <span data-ttu-id="ec30e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec30e-113">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="ec30e-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ec30e-114">Example 2</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="ec30e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec30e-115">PARAMETERS</span></span>

### <span data-ttu-id="ec30e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec30e-116">-DefaultProfile</span></span>
<span data-ttu-id="ec30e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec30e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec30e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ec30e-118">-DeviceName</span></span>
<span data-ttu-id="ec30e-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="ec30e-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec30e-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ec30e-120">-DeviceObject</span></span>
<span data-ttu-id="ec30e-121">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="ec30e-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec30e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ec30e-122">-Name</span></span>
<span data-ttu-id="ec30e-123">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="ec30e-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: BandwidthScheduleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec30e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec30e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec30e-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ec30e-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec30e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec30e-126">-ResourceId</span></span>
<span data-ttu-id="ec30e-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec30e-127">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec30e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec30e-128">CommonParameters</span></span>
<span data-ttu-id="ec30e-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec30e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec30e-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec30e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec30e-131">입력</span><span class="sxs-lookup"><span data-stu-id="ec30e-131">INPUTS</span></span>

### <span data-ttu-id="ec30e-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ec30e-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="ec30e-133">출력</span><span class="sxs-lookup"><span data-stu-id="ec30e-133">OUTPUTS</span></span>

### <span data-ttu-id="ec30e-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ec30e-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="ec30e-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec30e-135">NOTES</span></span>

## <span data-ttu-id="ec30e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec30e-136">RELATED LINKS</span></span>
