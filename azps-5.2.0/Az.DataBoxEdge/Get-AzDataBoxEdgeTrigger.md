---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 390646984cbe18c6fed0e6552e8034ae7afe311c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362776"
---
# <span data-ttu-id="600b6-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="600b6-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="600b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="600b6-102">SYNOPSIS</span></span>
<span data-ttu-id="600b6-103">디바이스에 구성된 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="600b6-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="600b6-104">구문</span><span class="sxs-lookup"><span data-stu-id="600b6-104">SYNTAX</span></span>

### <span data-ttu-id="600b6-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="600b6-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="600b6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="600b6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="600b6-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="600b6-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="600b6-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="600b6-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="600b6-109">설명</span><span class="sxs-lookup"><span data-stu-id="600b6-109">DESCRIPTION</span></span>
<span data-ttu-id="600b6-110">**Get-AzDataBoxEdgeTriger** cmdlet은 디바이스에 대한 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="600b6-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="600b6-111">cmdlet에서 이름을 매개 변수로 지정하여 특정 특정 트리거의 세부 정보를 페치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="600b6-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="600b6-112">예제</span><span class="sxs-lookup"><span data-stu-id="600b6-112">EXAMPLES</span></span>

### <span data-ttu-id="600b6-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="600b6-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="600b6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="600b6-114">PARAMETERS</span></span>

### <span data-ttu-id="600b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600b6-115">-DefaultProfile</span></span>
<span data-ttu-id="600b6-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="600b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="600b6-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="600b6-117">-DeviceName</span></span>
<span data-ttu-id="600b6-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="600b6-118">Device Name</span></span>

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

### <span data-ttu-id="600b6-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="600b6-119">-DeviceObject</span></span>
<span data-ttu-id="600b6-120">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="600b6-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="600b6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="600b6-121">-Name</span></span>
<span data-ttu-id="600b6-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="600b6-122">Resource Name</span></span>

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

### <span data-ttu-id="600b6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600b6-123">-ResourceGroupName</span></span>
<span data-ttu-id="600b6-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="600b6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="600b6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="600b6-125">-ResourceId</span></span>
<span data-ttu-id="600b6-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="600b6-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="600b6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600b6-127">CommonParameters</span></span>
<span data-ttu-id="600b6-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="600b6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600b6-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="600b6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600b6-130">입력</span><span class="sxs-lookup"><span data-stu-id="600b6-130">INPUTS</span></span>

### <span data-ttu-id="600b6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="600b6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="600b6-132">출력</span><span class="sxs-lookup"><span data-stu-id="600b6-132">OUTPUTS</span></span>

### <span data-ttu-id="600b6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="600b6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="600b6-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="600b6-134">NOTES</span></span>

## <span data-ttu-id="600b6-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="600b6-135">RELATED LINKS</span></span>
