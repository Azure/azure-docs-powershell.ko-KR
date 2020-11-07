---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879874"
---
# <span data-ttu-id="80149-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="80149-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="80149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80149-102">SYNOPSIS</span></span>
<span data-ttu-id="80149-103">호스트 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80149-103">Removes a host group.</span></span>

## <span data-ttu-id="80149-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80149-104">SYNTAX</span></span>

### <span data-ttu-id="80149-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="80149-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80149-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="80149-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80149-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="80149-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80149-108">설명은</span><span class="sxs-lookup"><span data-stu-id="80149-108">DESCRIPTION</span></span>
<span data-ttu-id="80149-109">이 cmdlet은 호스트 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="80149-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="80149-110">예제의</span><span class="sxs-lookup"><span data-stu-id="80149-110">EXAMPLES</span></span>

### <span data-ttu-id="80149-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="80149-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="80149-112">이 명령은 지정 된 호스트 그룹을 가져와 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80149-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="80149-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="80149-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="80149-114">이 명령은 지정 된 호스트 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80149-114">This command removes the given host group.</span></span>

## <span data-ttu-id="80149-115">변수</span><span class="sxs-lookup"><span data-stu-id="80149-115">PARAMETERS</span></span>

### <span data-ttu-id="80149-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80149-116">-AsJob</span></span>
<span data-ttu-id="80149-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="80149-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80149-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80149-118">-DefaultProfile</span></span>
<span data-ttu-id="80149-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80149-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80149-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80149-120">-InputObject</span></span>
<span data-ttu-id="80149-121">호스트 그룹의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="80149-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80149-122">-이름</span><span class="sxs-lookup"><span data-stu-id="80149-122">-Name</span></span>
<span data-ttu-id="80149-123">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80149-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80149-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80149-124">-ResourceGroupName</span></span>
<span data-ttu-id="80149-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80149-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80149-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80149-126">-ResourceId</span></span>
<span data-ttu-id="80149-127">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="80149-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80149-128">-확인</span><span class="sxs-lookup"><span data-stu-id="80149-128">-Confirm</span></span>
<span data-ttu-id="80149-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80149-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80149-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80149-130">-WhatIf</span></span>
<span data-ttu-id="80149-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80149-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80149-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80149-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80149-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80149-133">CommonParameters</span></span>
<span data-ttu-id="80149-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80149-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80149-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80149-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80149-136">입력</span><span class="sxs-lookup"><span data-stu-id="80149-136">INPUTS</span></span>

### <span data-ttu-id="80149-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="80149-137">System.String</span></span>

### <span data-ttu-id="80149-138">PSHostGroup의. m a.</span><span class="sxs-lookup"><span data-stu-id="80149-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="80149-139">출력</span><span class="sxs-lookup"><span data-stu-id="80149-139">OUTPUTS</span></span>

### <span data-ttu-id="80149-140">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="80149-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="80149-141">상속자</span><span class="sxs-lookup"><span data-stu-id="80149-141">NOTES</span></span>

## <span data-ttu-id="80149-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80149-142">RELATED LINKS</span></span>
