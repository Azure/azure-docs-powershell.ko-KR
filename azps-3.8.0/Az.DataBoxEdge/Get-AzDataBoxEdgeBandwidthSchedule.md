---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e3453e3359bb800180ebdeb3fa5158b890fd237a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042165"
---
# <span data-ttu-id="94a19-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="94a19-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="94a19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94a19-102">SYNOPSIS</span></span>
<span data-ttu-id="94a19-103">대역폭 일정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94a19-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="94a19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94a19-104">SYNTAX</span></span>

### <span data-ttu-id="94a19-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="94a19-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94a19-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94a19-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94a19-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94a19-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94a19-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94a19-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="94a19-109">설명은</span><span class="sxs-lookup"><span data-stu-id="94a19-109">DESCRIPTION</span></span>
<span data-ttu-id="94a19-110">**AzDataBoxEdgeBandwidthSchedule** Cmdlet은 대역폭 일정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94a19-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="94a19-111">리소스 그룹 이름 및 장치 이름과 함께 일정의 이름을 지정 하 여 특정 대역폭 일정에 대 한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94a19-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="94a19-112">예제의</span><span class="sxs-lookup"><span data-stu-id="94a19-112">EXAMPLES</span></span>

### <span data-ttu-id="94a19-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="94a19-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="94a19-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="94a19-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="94a19-115">변수</span><span class="sxs-lookup"><span data-stu-id="94a19-115">PARAMETERS</span></span>

### <span data-ttu-id="94a19-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a19-116">-DefaultProfile</span></span>
<span data-ttu-id="94a19-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94a19-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94a19-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="94a19-118">-DeviceName</span></span>
<span data-ttu-id="94a19-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="94a19-119">Device Name</span></span>

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

### <span data-ttu-id="94a19-120">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="94a19-120">-DeviceObject</span></span>
<span data-ttu-id="94a19-121">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="94a19-121">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="94a19-122">-이름</span><span class="sxs-lookup"><span data-stu-id="94a19-122">-Name</span></span>
<span data-ttu-id="94a19-123">자원 이름</span><span class="sxs-lookup"><span data-stu-id="94a19-123">Resource Name</span></span>

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

### <span data-ttu-id="94a19-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a19-124">-ResourceGroupName</span></span>
<span data-ttu-id="94a19-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="94a19-125">Resource Group Name</span></span>

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

### <span data-ttu-id="94a19-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94a19-126">-ResourceId</span></span>
<span data-ttu-id="94a19-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="94a19-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="94a19-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a19-128">CommonParameters</span></span>
<span data-ttu-id="94a19-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94a19-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a19-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="94a19-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a19-131">입력</span><span class="sxs-lookup"><span data-stu-id="94a19-131">INPUTS</span></span>

### <span data-ttu-id="94a19-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="94a19-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="94a19-133">출력</span><span class="sxs-lookup"><span data-stu-id="94a19-133">OUTPUTS</span></span>

### <span data-ttu-id="94a19-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="94a19-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="94a19-135">상속자</span><span class="sxs-lookup"><span data-stu-id="94a19-135">NOTES</span></span>

## <span data-ttu-id="94a19-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94a19-136">RELATED LINKS</span></span>
