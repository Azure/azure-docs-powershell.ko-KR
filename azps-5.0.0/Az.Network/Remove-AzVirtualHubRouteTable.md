---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218098"
---
# <span data-ttu-id="b5cc5-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5cc5-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="b5cc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="b5cc5-103">가상 허브에 연결 된 가상 허브 경로 테이블 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="b5cc5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5cc5-104">SYNTAX</span></span>

### <span data-ttu-id="b5cc5-105">ByVirtualHubRouteTableName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b5cc5-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5cc5-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b5cc5-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5cc5-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="b5cc5-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5cc5-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="b5cc5-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5cc5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b5cc5-109">DESCRIPTION</span></span>
<span data-ttu-id="b5cc5-110">지정 된 가상 허브에 연결 된 지정 된 경로 테이블을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="b5cc5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b5cc5-111">EXAMPLES</span></span>

### <span data-ttu-id="b5cc5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5cc5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="b5cc5-113">이 명령은 가상 허브 westushub의 routeTable1를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="b5cc5-114">변수</span><span class="sxs-lookup"><span data-stu-id="b5cc5-114">PARAMETERS</span></span>

### <span data-ttu-id="b5cc5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5cc5-115">-AsJob</span></span>
<span data-ttu-id="b5cc5-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b5cc5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5cc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5cc5-117">-DefaultProfile</span></span>
<span data-ttu-id="b5cc5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5cc5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b5cc5-119">-Force</span></span>
<span data-ttu-id="b5cc5-120">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="b5cc5-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b5cc5-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="b5cc5-121">-HubName</span></span>
<span data-ttu-id="b5cc5-122">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-122">The parent resource name.</span></span>

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

### <span data-ttu-id="b5cc5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5cc5-123">-InputObject</span></span>
<span data-ttu-id="b5cc5-124">제거할 virtualhubroutetable 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-124">The virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="b5cc5-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b5cc5-125">-Name</span></span>
<span data-ttu-id="b5cc5-126">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-126">The resource name.</span></span>

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

### <span data-ttu-id="b5cc5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5cc5-127">-PassThru</span></span>
<span data-ttu-id="b5cc5-128">이 작업이 수행 되는 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="b5cc5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5cc5-129">-ResourceGroupName</span></span>
<span data-ttu-id="b5cc5-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-130">The resource group name.</span></span>

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

### <span data-ttu-id="b5cc5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5cc5-131">-ResourceId</span></span>
<span data-ttu-id="b5cc5-132">제거할 virtualhubroutetable 리소스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="b5cc5-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="b5cc5-133">-VirtualHub</span></span>
<span data-ttu-id="b5cc5-134">{{VirtualHub 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="b5cc5-134">{{ Fill VirtualHub Description }}</span></span>

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

### <span data-ttu-id="b5cc5-135">-확인</span><span class="sxs-lookup"><span data-stu-id="b5cc5-135">-Confirm</span></span>
<span data-ttu-id="b5cc5-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5cc5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5cc5-137">-WhatIf</span></span>
<span data-ttu-id="b5cc5-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5cc5-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5cc5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5cc5-140">CommonParameters</span></span>
<span data-ttu-id="b5cc5-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5cc5-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5cc5-143">입력</span><span class="sxs-lookup"><span data-stu-id="b5cc5-143">INPUTS</span></span>

### <span data-ttu-id="b5cc5-144">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b5cc5-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="b5cc5-145">PSVirtualHubRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b5cc5-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="b5cc5-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b5cc5-146">System.String</span></span>

## <span data-ttu-id="b5cc5-147">출력</span><span class="sxs-lookup"><span data-stu-id="b5cc5-147">OUTPUTS</span></span>

### <span data-ttu-id="b5cc5-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b5cc5-148">System.Boolean</span></span>

## <span data-ttu-id="b5cc5-149">상속자</span><span class="sxs-lookup"><span data-stu-id="b5cc5-149">NOTES</span></span>

## <span data-ttu-id="b5cc5-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5cc5-150">RELATED LINKS</span></span>
