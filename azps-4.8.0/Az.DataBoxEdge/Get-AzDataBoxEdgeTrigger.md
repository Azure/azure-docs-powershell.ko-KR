---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 390646984cbe18c6fed0e6552e8034ae7afe311c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056435"
---
# <span data-ttu-id="4ce8c-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="4ce8c-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="4ce8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ce8c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce8c-103">장치에 구성 된 트리거 가져오기</span><span class="sxs-lookup"><span data-stu-id="4ce8c-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="4ce8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ce8c-104">SYNTAX</span></span>

### <span data-ttu-id="4ce8c-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4ce8c-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ce8c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ce8c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ce8c-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ce8c-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ce8c-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ce8c-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="4ce8c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="4ce8c-109">DESCRIPTION</span></span>
<span data-ttu-id="4ce8c-110">**AzDataBoxEdgeTriger** cmdlet은 장치에 대 한 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ce8c-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="4ce8c-111">Cmdlet에서 이름을 매개 변수로 지정 하 여 특정 특정 트리거의 세부 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ce8c-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="4ce8c-112">예제의</span><span class="sxs-lookup"><span data-stu-id="4ce8c-112">EXAMPLES</span></span>

### <span data-ttu-id="4ce8c-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="4ce8c-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="4ce8c-114">변수</span><span class="sxs-lookup"><span data-stu-id="4ce8c-114">PARAMETERS</span></span>

### <span data-ttu-id="4ce8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce8c-115">-DefaultProfile</span></span>
<span data-ttu-id="4ce8c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ce8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce8c-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="4ce8c-117">-DeviceName</span></span>
<span data-ttu-id="4ce8c-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="4ce8c-118">Device Name</span></span>

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

### <span data-ttu-id="4ce8c-119">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="4ce8c-119">-DeviceObject</span></span>
<span data-ttu-id="4ce8c-120">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4ce8c-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="4ce8c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="4ce8c-121">-Name</span></span>
<span data-ttu-id="4ce8c-122">자원 이름</span><span class="sxs-lookup"><span data-stu-id="4ce8c-122">Resource Name</span></span>

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

### <span data-ttu-id="4ce8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="4ce8c-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4ce8c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4ce8c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce8c-125">-ResourceId</span></span>
<span data-ttu-id="4ce8c-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce8c-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="4ce8c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce8c-127">CommonParameters</span></span>
<span data-ttu-id="4ce8c-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce8c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce8c-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4ce8c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce8c-130">입력</span><span class="sxs-lookup"><span data-stu-id="4ce8c-130">INPUTS</span></span>

### <span data-ttu-id="4ce8c-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4ce8c-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="4ce8c-132">출력</span><span class="sxs-lookup"><span data-stu-id="4ce8c-132">OUTPUTS</span></span>

### <span data-ttu-id="4ce8c-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="4ce8c-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="4ce8c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4ce8c-134">NOTES</span></span>

## <span data-ttu-id="4ce8c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ce8c-135">RELATED LINKS</span></span>
