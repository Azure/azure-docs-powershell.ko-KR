---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215170"
---
# <span data-ttu-id="27ba7-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ba7-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="27ba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="27ba7-103">장치에서 Edge 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27ba7-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="27ba7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27ba7-104">SYNTAX</span></span>

### <span data-ttu-id="27ba7-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="27ba7-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27ba7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27ba7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27ba7-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27ba7-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27ba7-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27ba7-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="27ba7-109">설명은</span><span class="sxs-lookup"><span data-stu-id="27ba7-109">DESCRIPTION</span></span>
<span data-ttu-id="27ba7-110">**AzStackEdgeStorageAccount** Cmdlet은 스택 경계 장치에서 사용할 수 있는 Edge 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27ba7-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="27ba7-111">Cmdlet에서 이름을 매개 변수로 지정 하 여 특정 Edge 저장소 계정의 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27ba7-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="27ba7-112">예제의</span><span class="sxs-lookup"><span data-stu-id="27ba7-112">EXAMPLES</span></span>

### <span data-ttu-id="27ba7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="27ba7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="27ba7-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="27ba7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="27ba7-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="27ba7-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="27ba7-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="27ba7-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="27ba7-117">변수</span><span class="sxs-lookup"><span data-stu-id="27ba7-117">PARAMETERS</span></span>

### <span data-ttu-id="27ba7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ba7-118">-DefaultProfile</span></span>
<span data-ttu-id="27ba7-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27ba7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27ba7-120">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="27ba7-120">-DeviceName</span></span>
<span data-ttu-id="27ba7-121">장치 이름</span><span class="sxs-lookup"><span data-stu-id="27ba7-121">Device Name</span></span>

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

### <span data-ttu-id="27ba7-122">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="27ba7-122">-DeviceObject</span></span>
<span data-ttu-id="27ba7-123">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="27ba7-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="27ba7-124">-이름</span><span class="sxs-lookup"><span data-stu-id="27ba7-124">-Name</span></span>
<span data-ttu-id="27ba7-125">자원 이름</span><span class="sxs-lookup"><span data-stu-id="27ba7-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ba7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ba7-126">-ResourceGroupName</span></span>
<span data-ttu-id="27ba7-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="27ba7-127">Resource Group Name</span></span>

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

### <span data-ttu-id="27ba7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ba7-128">-ResourceId</span></span>
<span data-ttu-id="27ba7-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ba7-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="27ba7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ba7-130">CommonParameters</span></span>
<span data-ttu-id="27ba7-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27ba7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ba7-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="27ba7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ba7-133">입력</span><span class="sxs-lookup"><span data-stu-id="27ba7-133">INPUTS</span></span>

### <span data-ttu-id="27ba7-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="27ba7-134">System.String</span></span>

### <span data-ttu-id="27ba7-135">StackEdge. PSStackEdgeDevice에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="27ba7-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="27ba7-136">출력</span><span class="sxs-lookup"><span data-stu-id="27ba7-136">OUTPUTS</span></span>

### <span data-ttu-id="27ba7-137">StackEdge. PSStackEdgeStorageAccount에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="27ba7-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="27ba7-138">상속자</span><span class="sxs-lookup"><span data-stu-id="27ba7-138">NOTES</span></span>

## <span data-ttu-id="27ba7-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27ba7-139">RELATED LINKS</span></span>
