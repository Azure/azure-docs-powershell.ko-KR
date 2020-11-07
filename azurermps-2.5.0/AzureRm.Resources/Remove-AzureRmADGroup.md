---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: 511d028c8307e53884cfa16472021fc59760b929
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880318"
---
# <span data-ttu-id="c59d3-101">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="c59d3-101">Remove-AzureRmADGroup</span></span>

## <span data-ttu-id="c59d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c59d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c59d3-103">Active directory 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-103">Deletes an active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c59d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c59d3-104">SYNTAX</span></span>

### <span data-ttu-id="c59d3-105">ObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c59d3-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59d3-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c59d3-106">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59d3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c59d3-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c59d3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c59d3-108">DESCRIPTION</span></span>
<span data-ttu-id="c59d3-109">Active directory 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="c59d3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c59d3-110">EXAMPLES</span></span>

### <span data-ttu-id="c59d3-111">예제 1-개체 id를 기준으로 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="c59d3-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c59d3-112">테 넌 트에서 개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="c59d3-113">예제 2-파이핑을 기준으로 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="c59d3-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroup
```

<span data-ttu-id="c59d3-114">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹을 가져오고, 테 넌 트에서 그룹을 제거 하도록 Remove-AzureRmADGroup 하는 데 사용 하는 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzureRmADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="c59d3-115">변수</span><span class="sxs-lookup"><span data-stu-id="c59d3-115">PARAMETERS</span></span>

### <span data-ttu-id="c59d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59d3-116">-DefaultProfile</span></span>
<span data-ttu-id="c59d3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59d3-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c59d3-118">-DisplayName</span></span>
<span data-ttu-id="c59d3-119">제거할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59d3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c59d3-120">-Force</span></span>
<span data-ttu-id="c59d3-121">지정 된 경우 그룹 삭제에 대 한 확인을 요청 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59d3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c59d3-122">-InputObject</span></span>
<span data-ttu-id="c59d3-123">제거할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c59d3-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c59d3-124">-ObjectId</span></span>
<span data-ttu-id="c59d3-125">제거할 그룹의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59d3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c59d3-126">-PassThru</span></span>
<span data-ttu-id="c59d3-127">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59d3-128">-확인</span><span class="sxs-lookup"><span data-stu-id="c59d3-128">-Confirm</span></span>
<span data-ttu-id="c59d3-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c59d3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c59d3-130">-WhatIf</span></span>
<span data-ttu-id="c59d3-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c59d3-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c59d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59d3-133">CommonParameters</span></span>
<span data-ttu-id="c59d3-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59d3-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c59d3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59d3-136">입력</span><span class="sxs-lookup"><span data-stu-id="c59d3-136">INPUTS</span></span>

### <span data-ttu-id="c59d3-137">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="c59d3-137">System.Guid</span></span>

### <span data-ttu-id="c59d3-138">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="c59d3-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="c59d3-139">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c59d3-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c59d3-140">출력</span><span class="sxs-lookup"><span data-stu-id="c59d3-140">OUTPUTS</span></span>

### <span data-ttu-id="c59d3-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c59d3-141">System.Boolean</span></span>

## <span data-ttu-id="c59d3-142">상속자</span><span class="sxs-lookup"><span data-stu-id="c59d3-142">NOTES</span></span>

## <span data-ttu-id="c59d3-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c59d3-143">RELATED LINKS</span></span>
