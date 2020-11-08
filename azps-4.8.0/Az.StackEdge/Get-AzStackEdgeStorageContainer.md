---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056942"
---
# <span data-ttu-id="0d151-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0d151-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="0d151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d151-102">SYNOPSIS</span></span>
<span data-ttu-id="0d151-103">디바이스의 Edge 저장소 계정에 대 한 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d151-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="0d151-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d151-104">SYNTAX</span></span>

### <span data-ttu-id="0d151-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0d151-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d151-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d151-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d151-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d151-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d151-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d151-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="0d151-109">설명은</span><span class="sxs-lookup"><span data-stu-id="0d151-109">DESCRIPTION</span></span>
<span data-ttu-id="0d151-110">**AzStackEdgeStorageContainer** Cmdlet은 스택 경계 디바이스의 edge 저장소 계정에 대 한 저장소 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d151-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="0d151-111">Cmdlet에서 이름을 매개 변수로 지정 하 여 특정 저장소 컨테이너의 세부 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d151-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="0d151-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0d151-112">EXAMPLES</span></span>

### <span data-ttu-id="0d151-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d151-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="0d151-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="0d151-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="0d151-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="0d151-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="0d151-116">변수</span><span class="sxs-lookup"><span data-stu-id="0d151-116">PARAMETERS</span></span>

### <span data-ttu-id="0d151-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d151-117">-DefaultProfile</span></span>
<span data-ttu-id="0d151-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d151-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d151-119">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="0d151-119">-DeviceName</span></span>
<span data-ttu-id="0d151-120">장치 이름</span><span class="sxs-lookup"><span data-stu-id="0d151-120">Device Name</span></span>

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

### <span data-ttu-id="0d151-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0d151-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="0d151-122">기존 EdgeStorageAccount의 이름 제공</span><span class="sxs-lookup"><span data-stu-id="0d151-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="0d151-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="0d151-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="0d151-124">기존 EdgeStorageAccount 개체 제공</span><span class="sxs-lookup"><span data-stu-id="0d151-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="0d151-125">-이름</span><span class="sxs-lookup"><span data-stu-id="0d151-125">-Name</span></span>
<span data-ttu-id="0d151-126">EdgeStorageContainer의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d151-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="0d151-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d151-127">-ResourceGroupName</span></span>
<span data-ttu-id="0d151-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0d151-128">Resource Group Name</span></span>

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

### <span data-ttu-id="0d151-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d151-129">-ResourceId</span></span>
<span data-ttu-id="0d151-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d151-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="0d151-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d151-131">CommonParameters</span></span>
<span data-ttu-id="0d151-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d151-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d151-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d151-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d151-134">입력</span><span class="sxs-lookup"><span data-stu-id="0d151-134">INPUTS</span></span>

### <span data-ttu-id="0d151-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0d151-135">System.String</span></span>

### <span data-ttu-id="0d151-136">StackEdge. PSStackEdgeStorageAccount에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="0d151-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="0d151-137">출력</span><span class="sxs-lookup"><span data-stu-id="0d151-137">OUTPUTS</span></span>

### <span data-ttu-id="0d151-138">StackEdge. PSStackEdgeStorageContainer에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="0d151-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="0d151-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0d151-139">NOTES</span></span>

## <span data-ttu-id="0d151-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d151-140">RELATED LINKS</span></span>
