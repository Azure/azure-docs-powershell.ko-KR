---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056940"
---
# <span data-ttu-id="cd017-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="cd017-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="cd017-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd017-102">SYNOPSIS</span></span>
<span data-ttu-id="cd017-103">장치에 구성 된 트리거 가져오기</span><span class="sxs-lookup"><span data-stu-id="cd017-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="cd017-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd017-104">SYNTAX</span></span>

### <span data-ttu-id="cd017-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd017-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd017-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd017-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd017-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd017-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd017-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd017-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="cd017-109">설명은</span><span class="sxs-lookup"><span data-stu-id="cd017-109">DESCRIPTION</span></span>
<span data-ttu-id="cd017-110">**AzStackEdgeTriger** cmdlet은 장치에 대 한 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd017-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="cd017-111">Cmdlet에서 이름을 매개 변수로 지정 하 여 특정 특정 트리거의 세부 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd017-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="cd017-112">예제의</span><span class="sxs-lookup"><span data-stu-id="cd017-112">EXAMPLES</span></span>

### <span data-ttu-id="cd017-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd017-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="cd017-114">변수</span><span class="sxs-lookup"><span data-stu-id="cd017-114">PARAMETERS</span></span>

### <span data-ttu-id="cd017-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd017-115">-DefaultProfile</span></span>
<span data-ttu-id="cd017-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd017-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd017-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="cd017-117">-DeviceName</span></span>
<span data-ttu-id="cd017-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="cd017-118">Device Name</span></span>

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

### <span data-ttu-id="cd017-119">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="cd017-119">-DeviceObject</span></span>
<span data-ttu-id="cd017-120">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd017-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="cd017-121">-이름</span><span class="sxs-lookup"><span data-stu-id="cd017-121">-Name</span></span>
<span data-ttu-id="cd017-122">자원 이름</span><span class="sxs-lookup"><span data-stu-id="cd017-122">Resource Name</span></span>

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

### <span data-ttu-id="cd017-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd017-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd017-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="cd017-124">Resource Group Name</span></span>

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

### <span data-ttu-id="cd017-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd017-125">-ResourceId</span></span>
<span data-ttu-id="cd017-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd017-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="cd017-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd017-127">CommonParameters</span></span>
<span data-ttu-id="cd017-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd017-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd017-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd017-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd017-130">입력</span><span class="sxs-lookup"><span data-stu-id="cd017-130">INPUTS</span></span>

### <span data-ttu-id="cd017-131">StackEdge. PSStackEdgeDevice에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="cd017-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="cd017-132">출력</span><span class="sxs-lookup"><span data-stu-id="cd017-132">OUTPUTS</span></span>

### <span data-ttu-id="cd017-133">StackEdge. PSStackEdgeTrigger에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="cd017-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="cd017-134">상속자</span><span class="sxs-lookup"><span data-stu-id="cd017-134">NOTES</span></span>

## <span data-ttu-id="cd017-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd017-135">RELATED LINKS</span></span>
