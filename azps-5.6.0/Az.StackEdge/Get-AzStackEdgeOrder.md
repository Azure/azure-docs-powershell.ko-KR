---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: d15a8dd5aecaa57c54707b026ad05763563b2070
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997103"
---
# <span data-ttu-id="5f704-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="5f704-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="5f704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f704-102">SYNOPSIS</span></span>
<span data-ttu-id="5f704-103">디바이스에 대한 주문 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="5f704-103">Get the order details for a device</span></span>

## <span data-ttu-id="5f704-104">구문</span><span class="sxs-lookup"><span data-stu-id="5f704-104">SYNTAX</span></span>

### <span data-ttu-id="5f704-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5f704-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f704-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f704-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f704-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f704-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f704-108">설명</span><span class="sxs-lookup"><span data-stu-id="5f704-108">DESCRIPTION</span></span>
<span data-ttu-id="5f704-109">**Get-AzStackEdgeOrder** cmdlet은 Stack Edge 디바이스에 대한 주문 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f704-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="5f704-110">예제</span><span class="sxs-lookup"><span data-stu-id="5f704-110">EXAMPLES</span></span>

### <span data-ttu-id="5f704-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5f704-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="5f704-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5f704-112">PARAMETERS</span></span>

### <span data-ttu-id="5f704-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f704-113">-DefaultProfile</span></span>
<span data-ttu-id="5f704-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f704-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f704-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5f704-115">-DeviceName</span></span>
<span data-ttu-id="5f704-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5f704-116">Resource Group Name</span></span>

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

### <span data-ttu-id="5f704-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5f704-117">-DeviceObject</span></span>
<span data-ttu-id="5f704-118">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="5f704-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: GetByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f704-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f704-119">-ResourceGroupName</span></span>
<span data-ttu-id="5f704-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5f704-120">Resource Group Name</span></span>

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

### <span data-ttu-id="5f704-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f704-121">-ResourceId</span></span>
<span data-ttu-id="5f704-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f704-122">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f704-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f704-123">CommonParameters</span></span>
<span data-ttu-id="5f704-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f704-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f704-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f704-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f704-126">입력</span><span class="sxs-lookup"><span data-stu-id="5f704-126">INPUTS</span></span>

### <span data-ttu-id="5f704-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5f704-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="5f704-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5f704-128">System.String</span></span>

## <span data-ttu-id="5f704-129">출력</span><span class="sxs-lookup"><span data-stu-id="5f704-129">OUTPUTS</span></span>

### <span data-ttu-id="5f704-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="5f704-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="5f704-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5f704-131">NOTES</span></span>

## <span data-ttu-id="5f704-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f704-132">RELATED LINKS</span></span>
