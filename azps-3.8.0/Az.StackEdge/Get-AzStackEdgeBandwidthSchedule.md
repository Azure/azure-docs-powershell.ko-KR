---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 5f2dfec045364852d9846fa3bb35bd903c78ca5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034533"
---
# <span data-ttu-id="ccad2-101">Get-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ccad2-101">Get-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="ccad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccad2-102">SYNOPSIS</span></span>
<span data-ttu-id="ccad2-103">대역폭 일정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ccad2-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="ccad2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccad2-104">SYNTAX</span></span>

### <span data-ttu-id="ccad2-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ccad2-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccad2-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccad2-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccad2-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccad2-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccad2-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccad2-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="ccad2-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ccad2-109">DESCRIPTION</span></span>
<span data-ttu-id="ccad2-110">**AzStackEdgeBandwidthSchedule** Cmdlet은 대역폭 일정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ccad2-110">The **Get-AzStackEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="ccad2-111">리소스 그룹 이름 및 장치 이름과 함께 일정의 이름을 지정 하 여 특정 대역폭 일정에 대 한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccad2-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="ccad2-112">예제의</span><span class="sxs-lookup"><span data-stu-id="ccad2-112">EXAMPLES</span></span>

### <span data-ttu-id="ccad2-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ccad2-113">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="ccad2-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ccad2-114">Example 2</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="ccad2-115">변수</span><span class="sxs-lookup"><span data-stu-id="ccad2-115">PARAMETERS</span></span>

### <span data-ttu-id="ccad2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccad2-116">-DefaultProfile</span></span>
<span data-ttu-id="ccad2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccad2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccad2-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="ccad2-118">-DeviceName</span></span>
<span data-ttu-id="ccad2-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="ccad2-119">Device Name</span></span>

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

### <span data-ttu-id="ccad2-120">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ccad2-120">-DeviceObject</span></span>
<span data-ttu-id="ccad2-121">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ccad2-121">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="ccad2-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ccad2-122">-Name</span></span>
<span data-ttu-id="ccad2-123">자원 이름</span><span class="sxs-lookup"><span data-stu-id="ccad2-123">Resource Name</span></span>

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

### <span data-ttu-id="ccad2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccad2-124">-ResourceGroupName</span></span>
<span data-ttu-id="ccad2-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ccad2-125">Resource Group Name</span></span>

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

### <span data-ttu-id="ccad2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccad2-126">-ResourceId</span></span>
<span data-ttu-id="ccad2-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccad2-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="ccad2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccad2-128">CommonParameters</span></span>
<span data-ttu-id="ccad2-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccad2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccad2-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ccad2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccad2-131">입력</span><span class="sxs-lookup"><span data-stu-id="ccad2-131">INPUTS</span></span>

### <span data-ttu-id="ccad2-132">StackEdge. PSStackEdgeDevice에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="ccad2-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="ccad2-133">출력</span><span class="sxs-lookup"><span data-stu-id="ccad2-133">OUTPUTS</span></span>

### <span data-ttu-id="ccad2-134">StackEdge. PSStackEdgeBandWidthSchedule에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="ccad2-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="ccad2-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ccad2-135">NOTES</span></span>

## <span data-ttu-id="ccad2-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccad2-136">RELATED LINKS</span></span>
