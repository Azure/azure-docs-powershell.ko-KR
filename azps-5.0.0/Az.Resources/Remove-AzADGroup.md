---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 895974f12c7472cb93679cb27ca895ca40757f53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215889"
---
# <span data-ttu-id="75618-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="75618-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="75618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75618-102">SYNOPSIS</span></span>
<span data-ttu-id="75618-103">Active directory 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="75618-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="75618-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75618-104">SYNTAX</span></span>

### <span data-ttu-id="75618-105">ObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="75618-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75618-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75618-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75618-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75618-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75618-108">설명은</span><span class="sxs-lookup"><span data-stu-id="75618-108">DESCRIPTION</span></span>
<span data-ttu-id="75618-109">Active directory 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="75618-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="75618-110">예제의</span><span class="sxs-lookup"><span data-stu-id="75618-110">EXAMPLES</span></span>

### <span data-ttu-id="75618-111">예제 1: 개체 id를 기준으로 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="75618-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="75618-112">테 넌 트에서 개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75618-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="75618-113">예제 2: 파이핑을 기준으로 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="75618-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="75618-114">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹을 가져오고, 테 넌 트에서 그룹을 제거 하도록 Remove-AzADGroup 하는 데 사용 하는 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75618-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="75618-115">변수</span><span class="sxs-lookup"><span data-stu-id="75618-115">PARAMETERS</span></span>

### <span data-ttu-id="75618-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75618-116">-DefaultProfile</span></span>
<span data-ttu-id="75618-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75618-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75618-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="75618-118">-DisplayName</span></span>
<span data-ttu-id="75618-119">제거할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75618-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="75618-120">-Force</span><span class="sxs-lookup"><span data-stu-id="75618-120">-Force</span></span>
<span data-ttu-id="75618-121">지정 된 경우 그룹 삭제에 대 한 확인을 요청 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75618-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="75618-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75618-122">-InputObject</span></span>
<span data-ttu-id="75618-123">제거할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="75618-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75618-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="75618-124">-ObjectId</span></span>
<span data-ttu-id="75618-125">제거할 그룹의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="75618-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75618-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75618-126">-PassThru</span></span>
<span data-ttu-id="75618-127">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75618-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="75618-128">-확인</span><span class="sxs-lookup"><span data-stu-id="75618-128">-Confirm</span></span>
<span data-ttu-id="75618-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="75618-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75618-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75618-130">-WhatIf</span></span>
<span data-ttu-id="75618-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="75618-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75618-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75618-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75618-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75618-133">CommonParameters</span></span>
<span data-ttu-id="75618-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75618-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75618-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="75618-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75618-136">입력</span><span class="sxs-lookup"><span data-stu-id="75618-136">INPUTS</span></span>

### <span data-ttu-id="75618-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75618-137">System.String</span></span>

### <span data-ttu-id="75618-138">ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="75618-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="75618-139">출력</span><span class="sxs-lookup"><span data-stu-id="75618-139">OUTPUTS</span></span>

### <span data-ttu-id="75618-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="75618-140">System.Boolean</span></span>

## <span data-ttu-id="75618-141">상속자</span><span class="sxs-lookup"><span data-stu-id="75618-141">NOTES</span></span>

## <span data-ttu-id="75618-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75618-142">RELATED LINKS</span></span>