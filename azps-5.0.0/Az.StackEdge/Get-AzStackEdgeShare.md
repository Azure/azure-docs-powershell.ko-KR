---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216944"
---
# <span data-ttu-id="80582-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="80582-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="80582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80582-102">SYNOPSIS</span></span>
<span data-ttu-id="80582-103">장치에 사용할 수 있는 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="80582-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="80582-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80582-104">SYNTAX</span></span>

### <span data-ttu-id="80582-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="80582-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80582-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80582-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80582-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="80582-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80582-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80582-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="80582-109">설명은</span><span class="sxs-lookup"><span data-stu-id="80582-109">DESCRIPTION</span></span>
<span data-ttu-id="80582-110">**AzStackEdgeShare** Cmdlet은 스택 경계 장치에 사용할 수 있는 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="80582-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="80582-111">Name이 제공 되 면 이름에 따라 공유를 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80582-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="80582-112">예제의</span><span class="sxs-lookup"><span data-stu-id="80582-112">EXAMPLES</span></span>

### <span data-ttu-id="80582-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="80582-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="80582-114">변수</span><span class="sxs-lookup"><span data-stu-id="80582-114">PARAMETERS</span></span>

### <span data-ttu-id="80582-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80582-115">-DefaultProfile</span></span>
<span data-ttu-id="80582-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80582-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80582-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="80582-117">-DeviceName</span></span>
<span data-ttu-id="80582-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="80582-118">Device Name</span></span>

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

### <span data-ttu-id="80582-119">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="80582-119">-DeviceObject</span></span>
<span data-ttu-id="80582-120">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="80582-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="80582-121">-이름</span><span class="sxs-lookup"><span data-stu-id="80582-121">-Name</span></span>
<span data-ttu-id="80582-122">자원 이름</span><span class="sxs-lookup"><span data-stu-id="80582-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80582-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80582-123">-ResourceGroupName</span></span>
<span data-ttu-id="80582-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="80582-124">Resource Group Name</span></span>

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

### <span data-ttu-id="80582-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80582-125">-ResourceId</span></span>
<span data-ttu-id="80582-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="80582-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="80582-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80582-127">CommonParameters</span></span>
<span data-ttu-id="80582-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80582-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80582-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80582-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80582-130">입력</span><span class="sxs-lookup"><span data-stu-id="80582-130">INPUTS</span></span>

### <span data-ttu-id="80582-131">StackEdge. PSStackEdgeDevice에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="80582-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="80582-132">출력</span><span class="sxs-lookup"><span data-stu-id="80582-132">OUTPUTS</span></span>

### <span data-ttu-id="80582-133">StackEdge. PSStackEdgeShare에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="80582-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="80582-134">상속자</span><span class="sxs-lookup"><span data-stu-id="80582-134">NOTES</span></span>

## <span data-ttu-id="80582-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80582-135">RELATED LINKS</span></span>
