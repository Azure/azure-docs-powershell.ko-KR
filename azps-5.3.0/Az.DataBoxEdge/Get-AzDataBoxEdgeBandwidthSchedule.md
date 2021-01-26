---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e3453e3359bb800180ebdeb3fa5158b890fd237a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495707"
---
# <span data-ttu-id="88fc1-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="88fc1-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="88fc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="88fc1-103">대역폭 일정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88fc1-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="88fc1-104">구문</span><span class="sxs-lookup"><span data-stu-id="88fc1-104">SYNTAX</span></span>

### <span data-ttu-id="88fc1-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="88fc1-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88fc1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88fc1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88fc1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="88fc1-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88fc1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88fc1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="88fc1-109">설명</span><span class="sxs-lookup"><span data-stu-id="88fc1-109">DESCRIPTION</span></span>
<span data-ttu-id="88fc1-110">**Get-AzDataBoxEdgeBandwidthSchedule** cmdlet은 대역폭 일정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88fc1-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="88fc1-111">리소스 그룹 이름 및 디바이스 이름과 함께 일정 이름을 지정하여 특정 대역폭 일정에 대한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88fc1-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="88fc1-112">예제</span><span class="sxs-lookup"><span data-stu-id="88fc1-112">EXAMPLES</span></span>

### <span data-ttu-id="88fc1-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="88fc1-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="88fc1-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="88fc1-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="88fc1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88fc1-115">PARAMETERS</span></span>

### <span data-ttu-id="88fc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88fc1-116">-DefaultProfile</span></span>
<span data-ttu-id="88fc1-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88fc1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88fc1-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="88fc1-118">-DeviceName</span></span>
<span data-ttu-id="88fc1-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="88fc1-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fc1-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="88fc1-120">-DeviceObject</span></span>
<span data-ttu-id="88fc1-121">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="88fc1-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88fc1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="88fc1-122">-Name</span></span>
<span data-ttu-id="88fc1-123">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="88fc1-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fc1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88fc1-124">-ResourceGroupName</span></span>
<span data-ttu-id="88fc1-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="88fc1-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fc1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88fc1-126">-ResourceId</span></span>
<span data-ttu-id="88fc1-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="88fc1-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="88fc1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88fc1-128">CommonParameters</span></span>
<span data-ttu-id="88fc1-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88fc1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88fc1-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88fc1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88fc1-131">입력</span><span class="sxs-lookup"><span data-stu-id="88fc1-131">INPUTS</span></span>

### <span data-ttu-id="88fc1-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="88fc1-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="88fc1-133">출력</span><span class="sxs-lookup"><span data-stu-id="88fc1-133">OUTPUTS</span></span>

### <span data-ttu-id="88fc1-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="88fc1-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="88fc1-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88fc1-135">NOTES</span></span>

## <span data-ttu-id="88fc1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88fc1-136">RELATED LINKS</span></span>
