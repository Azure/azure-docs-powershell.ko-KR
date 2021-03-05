---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 71540063e9eb4323d94a579df8f6489719f7c3fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011440"
---
# <span data-ttu-id="e503f-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e503f-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="e503f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e503f-102">SYNOPSIS</span></span>
<span data-ttu-id="e503f-103">디바이스에서 Edge Storage 계정에 대한 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e503f-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="e503f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e503f-104">SYNTAX</span></span>

### <span data-ttu-id="e503f-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e503f-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e503f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e503f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e503f-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e503f-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e503f-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e503f-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="e503f-109">설명</span><span class="sxs-lookup"><span data-stu-id="e503f-109">DESCRIPTION</span></span>
<span data-ttu-id="e503f-110">**Get-AzStackEdgeStorageContainer** cmdlet은 Stack Edge 디바이스의 Edge Storage 계정에 대한 저장소 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e503f-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="e503f-111">이름을 cmdlet에서 매개 변수로 지정하여 특정 저장소 컨테이너의 세부 정보를 인용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e503f-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="e503f-112">예제</span><span class="sxs-lookup"><span data-stu-id="e503f-112">EXAMPLES</span></span>

### <span data-ttu-id="e503f-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="e503f-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="e503f-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="e503f-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="e503f-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e503f-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="e503f-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e503f-116">PARAMETERS</span></span>

### <span data-ttu-id="e503f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e503f-117">-DefaultProfile</span></span>
<span data-ttu-id="e503f-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e503f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e503f-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e503f-119">-DeviceName</span></span>
<span data-ttu-id="e503f-120">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="e503f-120">Device Name</span></span>

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

### <span data-ttu-id="e503f-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e503f-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="e503f-122">기존 EdgeStorageAccount의 이름 제공</span><span class="sxs-lookup"><span data-stu-id="e503f-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e503f-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="e503f-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="e503f-124">기존 EdgeStorageAccount 개체 제공</span><span class="sxs-lookup"><span data-stu-id="e503f-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e503f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e503f-125">-Name</span></span>
<span data-ttu-id="e503f-126">EdgeStorageContainer의 이름</span><span class="sxs-lookup"><span data-stu-id="e503f-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e503f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e503f-127">-ResourceGroupName</span></span>
<span data-ttu-id="e503f-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e503f-128">Resource Group Name</span></span>

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

### <span data-ttu-id="e503f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e503f-129">-ResourceId</span></span>
<span data-ttu-id="e503f-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e503f-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e503f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e503f-131">CommonParameters</span></span>
<span data-ttu-id="e503f-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e503f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e503f-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e503f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e503f-134">입력</span><span class="sxs-lookup"><span data-stu-id="e503f-134">INPUTS</span></span>

### <span data-ttu-id="e503f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e503f-135">System.String</span></span>

### <span data-ttu-id="e503f-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e503f-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="e503f-137">출력</span><span class="sxs-lookup"><span data-stu-id="e503f-137">OUTPUTS</span></span>

### <span data-ttu-id="e503f-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e503f-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="e503f-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e503f-139">NOTES</span></span>

## <span data-ttu-id="e503f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e503f-140">RELATED LINKS</span></span>
