---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309429"
---
# <span data-ttu-id="89c0a-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="89c0a-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="89c0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="89c0a-103">장치에 대 한 주문 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="89c0a-103">Get the order details for a device</span></span>

## <span data-ttu-id="89c0a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89c0a-104">SYNTAX</span></span>

### <span data-ttu-id="89c0a-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="89c0a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89c0a-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89c0a-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89c0a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89c0a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89c0a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="89c0a-108">DESCRIPTION</span></span>
<span data-ttu-id="89c0a-109">**AzStackEdgeOrder** Cmdlet은 스택 경계 장치에 대 한 주문 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="89c0a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="89c0a-110">EXAMPLES</span></span>

### <span data-ttu-id="89c0a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="89c0a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="89c0a-112">변수</span><span class="sxs-lookup"><span data-stu-id="89c0a-112">PARAMETERS</span></span>

### <span data-ttu-id="89c0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c0a-113">-DefaultProfile</span></span>
<span data-ttu-id="89c0a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89c0a-115">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="89c0a-115">-DeviceName</span></span>
<span data-ttu-id="89c0a-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="89c0a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="89c0a-117">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="89c0a-117">-DeviceObject</span></span>
<span data-ttu-id="89c0a-118">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="89c0a-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="89c0a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89c0a-119">-ResourceGroupName</span></span>
<span data-ttu-id="89c0a-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="89c0a-120">Resource Group Name</span></span>

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

### <span data-ttu-id="89c0a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89c0a-121">-ResourceId</span></span>
<span data-ttu-id="89c0a-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="89c0a-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="89c0a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c0a-123">CommonParameters</span></span>
<span data-ttu-id="89c0a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c0a-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="89c0a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c0a-126">입력</span><span class="sxs-lookup"><span data-stu-id="89c0a-126">INPUTS</span></span>

### <span data-ttu-id="89c0a-127">StackEdge. PSStackEdgeDevice에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="89c0a-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="89c0a-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89c0a-128">System.String</span></span>

## <span data-ttu-id="89c0a-129">출력</span><span class="sxs-lookup"><span data-stu-id="89c0a-129">OUTPUTS</span></span>

### <span data-ttu-id="89c0a-130">StackEdge. PSStackEdgeOrder에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="89c0a-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="89c0a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="89c0a-131">NOTES</span></span>

## <span data-ttu-id="89c0a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89c0a-132">RELATED LINKS</span></span>
