---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213103"
---
# <span data-ttu-id="4fd9b-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="4fd9b-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="4fd9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd9b-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd9b-103">호스트 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-103">Removes a host group.</span></span>

## <span data-ttu-id="4fd9b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fd9b-104">SYNTAX</span></span>

### <span data-ttu-id="4fd9b-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="4fd9b-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd9b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4fd9b-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd9b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4fd9b-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fd9b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4fd9b-108">DESCRIPTION</span></span>
<span data-ttu-id="4fd9b-109">이 cmdlet은 호스트 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="4fd9b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4fd9b-110">EXAMPLES</span></span>

### <span data-ttu-id="4fd9b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4fd9b-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="4fd9b-112">이 명령은 지정 된 호스트 그룹을 가져와 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="4fd9b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4fd9b-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="4fd9b-114">이 명령은 지정 된 호스트 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-114">This command removes the given host group.</span></span>

## <span data-ttu-id="4fd9b-115">변수</span><span class="sxs-lookup"><span data-stu-id="4fd9b-115">PARAMETERS</span></span>

### <span data-ttu-id="4fd9b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fd9b-116">-AsJob</span></span>
<span data-ttu-id="4fd9b-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4fd9b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fd9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd9b-118">-DefaultProfile</span></span>
<span data-ttu-id="4fd9b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd9b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fd9b-120">-InputObject</span></span>
<span data-ttu-id="4fd9b-121">호스트 그룹의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-121">The local object of the host group.</span></span>

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

### <span data-ttu-id="4fd9b-122">-이름</span><span class="sxs-lookup"><span data-stu-id="4fd9b-122">-Name</span></span>
<span data-ttu-id="4fd9b-123">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-123">The name of the host group.</span></span>

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

### <span data-ttu-id="4fd9b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd9b-124">-ResourceGroupName</span></span>
<span data-ttu-id="4fd9b-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="4fd9b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fd9b-126">-ResourceId</span></span>
<span data-ttu-id="4fd9b-127">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="4fd9b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="4fd9b-128">-Confirm</span></span>
<span data-ttu-id="4fd9b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd9b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fd9b-130">-WhatIf</span></span>
<span data-ttu-id="4fd9b-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fd9b-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd9b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd9b-133">CommonParameters</span></span>
<span data-ttu-id="4fd9b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd9b-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd9b-136">입력</span><span class="sxs-lookup"><span data-stu-id="4fd9b-136">INPUTS</span></span>

### <span data-ttu-id="4fd9b-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4fd9b-137">System.String</span></span>

### <span data-ttu-id="4fd9b-138">PSHostGroup의. m a.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="4fd9b-139">출력</span><span class="sxs-lookup"><span data-stu-id="4fd9b-139">OUTPUTS</span></span>

### <span data-ttu-id="4fd9b-140">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="4fd9b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4fd9b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4fd9b-141">NOTES</span></span>

## <span data-ttu-id="4fd9b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fd9b-142">RELATED LINKS</span></span>
