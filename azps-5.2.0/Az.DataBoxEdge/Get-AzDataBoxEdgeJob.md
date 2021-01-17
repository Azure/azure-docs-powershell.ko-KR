---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c2d97f4a7d713482a5e442e1fcb712ccb18797c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330350"
---
# <span data-ttu-id="6a474-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="6a474-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="6a474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a474-102">SYNOPSIS</span></span>
<span data-ttu-id="6a474-103">디바이스에서 예약된 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a474-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="6a474-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a474-104">SYNTAX</span></span>

### <span data-ttu-id="6a474-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6a474-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a474-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="6a474-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a474-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a474-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="6a474-108">설명</span><span class="sxs-lookup"><span data-stu-id="6a474-108">DESCRIPTION</span></span>
<span data-ttu-id="6a474-109">**Get-AzDataBoxEdgeJob** cmdlet은 Data Box Edge 디바이스에서 활성 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a474-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="6a474-110">Name 매개 변수를 언급하여 특정 작업의 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a474-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="6a474-111">예제</span><span class="sxs-lookup"><span data-stu-id="6a474-111">EXAMPLES</span></span>

### <span data-ttu-id="6a474-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a474-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="6a474-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a474-113">PARAMETERS</span></span>

### <span data-ttu-id="6a474-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a474-114">-DefaultProfile</span></span>
<span data-ttu-id="6a474-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a474-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a474-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6a474-116">-DeviceName</span></span>
<span data-ttu-id="6a474-117">디바이스의 이름</span><span class="sxs-lookup"><span data-stu-id="6a474-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a474-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6a474-118">-DeviceObject</span></span>
<span data-ttu-id="6a474-119">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="6a474-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="6a474-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6a474-120">-Name</span></span>
<span data-ttu-id="6a474-121">작업의 이름, 일반적으로 GUID</span><span class="sxs-lookup"><span data-stu-id="6a474-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a474-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a474-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a474-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6a474-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a474-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a474-124">-ResourceId</span></span>
<span data-ttu-id="6a474-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a474-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a474-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a474-126">CommonParameters</span></span>
<span data-ttu-id="6a474-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a474-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a474-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a474-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a474-129">입력</span><span class="sxs-lookup"><span data-stu-id="6a474-129">INPUTS</span></span>

### <span data-ttu-id="6a474-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6a474-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="6a474-131">출력</span><span class="sxs-lookup"><span data-stu-id="6a474-131">OUTPUTS</span></span>

### <span data-ttu-id="6a474-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="6a474-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="6a474-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a474-133">NOTES</span></span>

## <span data-ttu-id="6a474-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a474-134">RELATED LINKS</span></span>
