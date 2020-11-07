---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: b41f7ca642d74a33c239f125d7dfe2ccdbad1b68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878057"
---
# <span data-ttu-id="08ac3-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="08ac3-101">Update-AzTag</span></span>

## <span data-ttu-id="08ac3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08ac3-102">SYNOPSIS</span></span>

<span data-ttu-id="08ac3-103">리소스나 구독의 태그 집합을 선택적으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="08ac3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08ac3-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="08ac3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="08ac3-105">DESCRIPTION</span></span>

<span data-ttu-id="08ac3-106">**ResourceId** 가 있는 **업데이트-AzTag** cmdlet은 리소스 또는 구독에 대 한 태그 집합을 선택적으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="08ac3-107">이 작업을 수행 하면 지정 된 리소스나 구독의 태그를 바꾸거나, 병합 하거나, 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="08ac3-108">작업이 끝날 때 지정 된 엔터티는 최대 50 태그를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="08ac3-109">' 바꾸기 ' 옵션은 기존 태그의 전체 집합을 새 집합으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="08ac3-110">' 병합 ' 옵션을 사용 하면 새 이름으로 태그를 추가 하 고 기존 이름을 사용 하 여 태그 값을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="08ac3-111">' 삭제 ' 옵션을 사용 하면 지정 된 이름 또는 이름/값 쌍을 기준으로 태그를 선택적으로 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="08ac3-112">예제의</span><span class="sxs-lookup"><span data-stu-id="08ac3-112">EXAMPLES</span></span>

### <span data-ttu-id="08ac3-113">예제 1: "Merge" 작업을 사용 하 여 선택적으로 구독에 태그 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

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

<span data-ttu-id="08ac3-114">이 명령은 {subId}를 사용 하 여 구독의 태그 집합을 병합 합니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="08ac3-115">예제 2: "바꾸기" 작업을 사용 하 여 선택적으로 구독에 태그 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

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

<span data-ttu-id="08ac3-116">이 명령은 {subId}를 사용 하 여 구독에 대 한 태그 집합을 Repalces.</span><span class="sxs-lookup"><span data-stu-id="08ac3-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="08ac3-117">예제 3: "Delete" 작업을 사용 하 여 구독에서 태그 집합을 선택적으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

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

<span data-ttu-id="08ac3-118">이 명령은 {subId}를 사용 하 여 구독에서 태그 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="08ac3-119">변수</span><span class="sxs-lookup"><span data-stu-id="08ac3-119">PARAMETERS</span></span>

### <span data-ttu-id="08ac3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ac3-120">-DefaultProfile</span></span>
<span data-ttu-id="08ac3-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08ac3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08ac3-122">-ResourceId</span></span>
<span data-ttu-id="08ac3-123">태그가 지정 된 엔터티의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="08ac3-124">리소스, 리소스 그룹 또는 구독에 태그가 지정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ac3-125">태그</span><span class="sxs-lookup"><span data-stu-id="08ac3-125">-Tag</span></span>
<span data-ttu-id="08ac3-126">업데이트에 사용할 태그 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-126">The set of tags to use for update.</span></span>

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

### <span data-ttu-id="08ac3-127">-작업</span><span class="sxs-lookup"><span data-stu-id="08ac3-127">-Operation</span></span>
<span data-ttu-id="08ac3-128">업데이트 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-128">The update operation.</span></span> <span data-ttu-id="08ac3-129">옵션은 병합, 바꾸기 및 삭제입니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08ac3-130">-확인</span><span class="sxs-lookup"><span data-stu-id="08ac3-130">-Confirm</span></span>
<span data-ttu-id="08ac3-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08ac3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08ac3-132">-WhatIf</span></span>
<span data-ttu-id="08ac3-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08ac3-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08ac3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ac3-135">CommonParameters</span></span>
<span data-ttu-id="08ac3-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08ac3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ac3-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="08ac3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ac3-138">입력</span><span class="sxs-lookup"><span data-stu-id="08ac3-138">INPUTS</span></span>

### <span data-ttu-id="08ac3-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="08ac3-139">System.String</span></span>

### <span data-ttu-id="08ac3-140">TagPatchOpeation에 대 한.</span><span class="sxs-lookup"><span data-stu-id="08ac3-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation</span></span>

### <span data-ttu-id="08ac3-141">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="08ac3-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="08ac3-142">출력</span><span class="sxs-lookup"><span data-stu-id="08ac3-142">OUTPUTS</span></span>

### <span data-ttu-id="08ac3-143">PSTagResource에 대 한.</span><span class="sxs-lookup"><span data-stu-id="08ac3-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="08ac3-144">상속자</span><span class="sxs-lookup"><span data-stu-id="08ac3-144">NOTES</span></span>

## <span data-ttu-id="08ac3-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08ac3-145">RELATED LINKS</span></span>

[<span data-ttu-id="08ac3-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="08ac3-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="08ac3-147">새로운 AzTag</span><span class="sxs-lookup"><span data-stu-id="08ac3-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="08ac3-148">제거-AzTag</span><span class="sxs-lookup"><span data-stu-id="08ac3-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
