---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 14e19068d3634acfd558f976b13661af28495321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007579"
---
# <span data-ttu-id="6f564-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="6f564-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="6f564-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f564-102">SYNOPSIS</span></span>
<span data-ttu-id="6f564-103">디바이스에서 예약된 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f564-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="6f564-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f564-104">SYNTAX</span></span>

### <span data-ttu-id="6f564-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6f564-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f564-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="6f564-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f564-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f564-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="6f564-108">설명</span><span class="sxs-lookup"><span data-stu-id="6f564-108">DESCRIPTION</span></span>
<span data-ttu-id="6f564-109">**Get-AzStackEdgeJob** cmdlet은 Stack Edge 디바이스에서 활성 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f564-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="6f564-110">이름 매개 변수를 언급하여 특정 작업의 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f564-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="6f564-111">예제</span><span class="sxs-lookup"><span data-stu-id="6f564-111">EXAMPLES</span></span>

### <span data-ttu-id="6f564-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f564-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="6f564-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6f564-113">PARAMETERS</span></span>

### <span data-ttu-id="6f564-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f564-114">-DefaultProfile</span></span>
<span data-ttu-id="6f564-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f564-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f564-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6f564-116">-DeviceName</span></span>
<span data-ttu-id="6f564-117">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="6f564-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f564-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6f564-118">-DeviceObject</span></span>
<span data-ttu-id="6f564-119">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="6f564-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f564-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6f564-120">-Name</span></span>
<span data-ttu-id="6f564-121">작업 이름, 일반적으로 GUID</span><span class="sxs-lookup"><span data-stu-id="6f564-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f564-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f564-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f564-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6f564-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f564-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f564-124">-ResourceId</span></span>
<span data-ttu-id="6f564-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f564-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f564-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f564-126">CommonParameters</span></span>
<span data-ttu-id="6f564-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f564-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f564-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f564-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f564-129">입력</span><span class="sxs-lookup"><span data-stu-id="6f564-129">INPUTS</span></span>

### <span data-ttu-id="6f564-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6f564-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="6f564-131">출력</span><span class="sxs-lookup"><span data-stu-id="6f564-131">OUTPUTS</span></span>

### <span data-ttu-id="6f564-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="6f564-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="6f564-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f564-133">NOTES</span></span>

## <span data-ttu-id="6f564-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f564-134">RELATED LINKS</span></span>
