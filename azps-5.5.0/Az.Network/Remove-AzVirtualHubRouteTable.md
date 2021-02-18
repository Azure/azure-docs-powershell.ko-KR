---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206549"
---
# <span data-ttu-id="7a3d0-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7a3d0-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="7a3d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="7a3d0-103">가상 허브와 연결된 가상 허브 경로 테이블 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="7a3d0-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a3d0-104">SYNTAX</span></span>

### <span data-ttu-id="7a3d0-105">ByVirtualHubRouteTableName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a3d0-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a3d0-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="7a3d0-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a3d0-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="7a3d0-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a3d0-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="7a3d0-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a3d0-109">설명</span><span class="sxs-lookup"><span data-stu-id="7a3d0-109">DESCRIPTION</span></span>
<span data-ttu-id="7a3d0-110">지정된 가상 허브와 연결된 지정된 경로 테이블을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="7a3d0-111">예제</span><span class="sxs-lookup"><span data-stu-id="7a3d0-111">EXAMPLES</span></span>

### <span data-ttu-id="7a3d0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a3d0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="7a3d0-113">이 명령은 가상 허브 westushub의 routeTable1을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="7a3d0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a3d0-114">PARAMETERS</span></span>

### <span data-ttu-id="7a3d0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a3d0-115">-AsJob</span></span>
<span data-ttu-id="7a3d0-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7a3d0-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a3d0-117">-DefaultProfile</span></span>
<span data-ttu-id="7a3d0-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7a3d0-119">-Force</span></span>
<span data-ttu-id="7a3d0-120">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="7a3d0-121">-HubName</span></span>
<span data-ttu-id="7a3d0-122">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a3d0-123">-InputObject</span></span>
<span data-ttu-id="7a3d0-124">제거할 virtualhubroutetable 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7a3d0-125">-Name</span></span>
<span data-ttu-id="7a3d0-126">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a3d0-127">-PassThru</span></span>
<span data-ttu-id="7a3d0-128">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a3d0-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a3d0-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a3d0-131">-ResourceId</span></span>
<span data-ttu-id="7a3d0-132">제거할 virtualhubroutetable 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="7a3d0-133">-VirtualHub</span></span>
<span data-ttu-id="7a3d0-134">{{ VirtualHub 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="7a3d0-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a3d0-135">-Confirm</span></span>
<span data-ttu-id="7a3d0-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a3d0-137">-WhatIf</span></span>
<span data-ttu-id="7a3d0-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7a3d0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a3d0-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a3d0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a3d0-140">CommonParameters</span></span>
<span data-ttu-id="7a3d0-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a3d0-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a3d0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a3d0-143">입력</span><span class="sxs-lookup"><span data-stu-id="7a3d0-143">INPUTS</span></span>

### <span data-ttu-id="7a3d0-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7a3d0-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="7a3d0-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7a3d0-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="7a3d0-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7a3d0-146">System.String</span></span>

## <span data-ttu-id="7a3d0-147">출력</span><span class="sxs-lookup"><span data-stu-id="7a3d0-147">OUTPUTS</span></span>

### <span data-ttu-id="7a3d0-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a3d0-148">System.Boolean</span></span>

## <span data-ttu-id="7a3d0-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a3d0-149">NOTES</span></span>

## <span data-ttu-id="7a3d0-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a3d0-150">RELATED LINKS</span></span>
