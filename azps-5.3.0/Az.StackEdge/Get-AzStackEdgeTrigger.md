---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494708"
---
# <span data-ttu-id="ee54f-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ee54f-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="ee54f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee54f-102">SYNOPSIS</span></span>
<span data-ttu-id="ee54f-103">디바이스에 구성된 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ee54f-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="ee54f-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee54f-104">SYNTAX</span></span>

### <span data-ttu-id="ee54f-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ee54f-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee54f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee54f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee54f-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee54f-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee54f-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee54f-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="ee54f-109">설명</span><span class="sxs-lookup"><span data-stu-id="ee54f-109">DESCRIPTION</span></span>
<span data-ttu-id="ee54f-110">**Get-AzStackEdgeTriger** cmdlet은 디바이스에 대한 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ee54f-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="ee54f-111">cmdlet에서 이름을 매개 변수로 지정하여 특정 특정 트리거의 세부 정보를 페치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee54f-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="ee54f-112">예제</span><span class="sxs-lookup"><span data-stu-id="ee54f-112">EXAMPLES</span></span>

### <span data-ttu-id="ee54f-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee54f-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="ee54f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee54f-114">PARAMETERS</span></span>

### <span data-ttu-id="ee54f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee54f-115">-DefaultProfile</span></span>
<span data-ttu-id="ee54f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee54f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee54f-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ee54f-117">-DeviceName</span></span>
<span data-ttu-id="ee54f-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="ee54f-118">Device Name</span></span>

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

### <span data-ttu-id="ee54f-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ee54f-119">-DeviceObject</span></span>
<span data-ttu-id="ee54f-120">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="ee54f-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="ee54f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ee54f-121">-Name</span></span>
<span data-ttu-id="ee54f-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="ee54f-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee54f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee54f-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee54f-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ee54f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ee54f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee54f-125">-ResourceId</span></span>
<span data-ttu-id="ee54f-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee54f-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="ee54f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee54f-127">CommonParameters</span></span>
<span data-ttu-id="ee54f-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee54f-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee54f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee54f-130">입력</span><span class="sxs-lookup"><span data-stu-id="ee54f-130">INPUTS</span></span>

### <span data-ttu-id="ee54f-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ee54f-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="ee54f-132">출력</span><span class="sxs-lookup"><span data-stu-id="ee54f-132">OUTPUTS</span></span>

### <span data-ttu-id="ee54f-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ee54f-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="ee54f-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee54f-134">NOTES</span></span>

## <span data-ttu-id="ee54f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee54f-135">RELATED LINKS</span></span>
