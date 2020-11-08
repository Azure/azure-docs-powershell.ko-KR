---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218102"
---
# <span data-ttu-id="0a808-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a808-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="0a808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a808-102">SYNOPSIS</span></span>
<span data-ttu-id="0a808-103">VirtualHub와 연결 된 허브 경로 테이블 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="0a808-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a808-104">SYNTAX</span></span>

### <span data-ttu-id="0a808-105">ByVHubRouteTableName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0a808-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a808-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="0a808-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a808-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="0a808-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a808-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="0a808-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a808-109">설명은</span><span class="sxs-lookup"><span data-stu-id="0a808-109">DESCRIPTION</span></span>
<span data-ttu-id="0a808-110">지정 된 가상 허브에 연결 된 지정 된 허브 경로 테이블을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="0a808-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0a808-111">EXAMPLES</span></span>

### <span data-ttu-id="0a808-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a808-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="0a808-113">이 명령은 가상 허브의 허브 경로 테이블을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="0a808-114">변수</span><span class="sxs-lookup"><span data-stu-id="0a808-114">PARAMETERS</span></span>

### <span data-ttu-id="0a808-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a808-115">-AsJob</span></span>
<span data-ttu-id="0a808-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0a808-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a808-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a808-117">-DefaultProfile</span></span>
<span data-ttu-id="0a808-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a808-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0a808-119">-Force</span></span>
<span data-ttu-id="0a808-120">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="0a808-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0a808-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a808-121">-InputObject</span></span>
<span data-ttu-id="0a808-122">제거할 vhubroutetable 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a808-123">-이름</span><span class="sxs-lookup"><span data-stu-id="0a808-123">-Name</span></span>
<span data-ttu-id="0a808-124">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a808-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0a808-125">-ParentObject</span></span>
<span data-ttu-id="0a808-126">이 리소스의 부모 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a808-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="0a808-127">-ParentResourceName</span></span>
<span data-ttu-id="0a808-128">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a808-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a808-129">-PassThru</span></span>
<span data-ttu-id="0a808-130">이 작업이 수행 되는 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="0a808-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a808-131">-ResourceGroupName</span></span>
<span data-ttu-id="0a808-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a808-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a808-133">-ResourceId</span></span>
<span data-ttu-id="0a808-134">제거할 vhubroutetable 리소스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a808-135">-확인</span><span class="sxs-lookup"><span data-stu-id="0a808-135">-Confirm</span></span>
<span data-ttu-id="0a808-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a808-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a808-137">-WhatIf</span></span>
<span data-ttu-id="0a808-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a808-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a808-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a808-140">CommonParameters</span></span>
<span data-ttu-id="0a808-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a808-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a808-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0a808-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a808-143">입력</span><span class="sxs-lookup"><span data-stu-id="0a808-143">INPUTS</span></span>

### <span data-ttu-id="0a808-144">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a808-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="0a808-145">PSVHubRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0a808-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="0a808-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0a808-146">System.String</span></span>

## <span data-ttu-id="0a808-147">출력</span><span class="sxs-lookup"><span data-stu-id="0a808-147">OUTPUTS</span></span>

### <span data-ttu-id="0a808-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0a808-148">System.Boolean</span></span>

## <span data-ttu-id="0a808-149">상속자</span><span class="sxs-lookup"><span data-stu-id="0a808-149">NOTES</span></span>

## <span data-ttu-id="0a808-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a808-150">RELATED LINKS</span></span>

[<span data-ttu-id="0a808-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a808-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="0a808-152">새로운 AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="0a808-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="0a808-153">새로운 AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a808-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="0a808-154">업데이트-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a808-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)