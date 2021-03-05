---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: acf97f282e50d9c6f468e400cb2a5c598fe06659
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997131"
---
# <span data-ttu-id="16aff-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="16aff-101">Update-AzTag</span></span>

## <span data-ttu-id="16aff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16aff-102">SYNOPSIS</span></span>

<span data-ttu-id="16aff-103">리소스 또는 구독에서 태그 집합을 선택적으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="16aff-104">구문</span><span class="sxs-lookup"><span data-stu-id="16aff-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOperation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="16aff-105">설명</span><span class="sxs-lookup"><span data-stu-id="16aff-105">DESCRIPTION</span></span>

<span data-ttu-id="16aff-106">**ResourceId가** **있는 Update-AzTag** cmdlet은 리소스 또는 구독의 태그 집합을 선택적으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="16aff-107">이 작업을 사용하면 지정된 리소스 또는 구독에서 태그를 바꾸거나, 을(를) 또는 선택적으로 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="16aff-108">지정된 엔터티는 작업 끝에 최대 50개 태그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="16aff-109">'바꾸기' 옵션은 기존 태그의 전체 집합을 새 집합으로 바 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="16aff-110">'병합' 옵션을 사용하면 새 이름이 있는 태그를 추가하고 기존 이름으로 태그 값을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="16aff-111">'delete' 옵션을 사용하면 지정한 이름 또는 이름/값 쌍에 따라 태그를 선택적으로 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="16aff-112">예제</span><span class="sxs-lookup"><span data-stu-id="16aff-112">EXAMPLES</span></span>

### <span data-ttu-id="16aff-113">예제 1: "병합" 작업을 사용하여 구독의 태그 집합을 선택적으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

<span data-ttu-id="16aff-114">이 명령은 구독의 태그 집합을 {subId}로 병합합니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="16aff-115">예제 2: "바꾸기" 작업으로 구독의 태그 집합을 선택적으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

<span data-ttu-id="16aff-116">이 명령은 {subId}를 사용하여 구독의 태그 집합을 다시palces합니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="16aff-117">예제 3: "삭제" 작업을 사용하여 구독의 태그 집합을 선택적으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

<span data-ttu-id="16aff-118">이 명령은 {subId}를 사용하여 구독의 태그 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="16aff-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="16aff-119">PARAMETERS</span></span>

### <span data-ttu-id="16aff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16aff-120">-DefaultProfile</span></span>
<span data-ttu-id="16aff-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16aff-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16aff-122">-ResourceId</span></span>
<span data-ttu-id="16aff-123">태그가 지정된 엔터티의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="16aff-124">리소스, 리소스 그룹 또는 구독에 태그가 지정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16aff-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="16aff-125">-Tag</span></span>
<span data-ttu-id="16aff-126">업데이트에 사용할 태그 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-126">The set of tags to use for update.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16aff-127">-Operation</span><span class="sxs-lookup"><span data-stu-id="16aff-127">-Operation</span></span>
<span data-ttu-id="16aff-128">업데이트 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-128">The update operation.</span></span> <span data-ttu-id="16aff-129">옵션은 병합, 바꾸기 및 삭제입니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOperation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16aff-130">-확인</span><span class="sxs-lookup"><span data-stu-id="16aff-130">-Confirm</span></span>
<span data-ttu-id="16aff-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16aff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16aff-132">-WhatIf</span></span>
<span data-ttu-id="16aff-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16aff-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16aff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16aff-135">CommonParameters</span></span>
<span data-ttu-id="16aff-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16aff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16aff-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16aff-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16aff-138">입력</span><span class="sxs-lookup"><span data-stu-id="16aff-138">INPUTS</span></span>

### <span data-ttu-id="16aff-139">System.String</span><span class="sxs-lookup"><span data-stu-id="16aff-139">System.String</span></span>

### <span data-ttu-id="16aff-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span><span class="sxs-lookup"><span data-stu-id="16aff-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span></span>

### <span data-ttu-id="16aff-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="16aff-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="16aff-142">출력</span><span class="sxs-lookup"><span data-stu-id="16aff-142">OUTPUTS</span></span>

### <span data-ttu-id="16aff-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="16aff-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="16aff-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16aff-144">NOTES</span></span>

## <span data-ttu-id="16aff-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16aff-145">RELATED LINKS</span></span>

[<span data-ttu-id="16aff-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="16aff-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="16aff-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="16aff-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="16aff-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="16aff-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
