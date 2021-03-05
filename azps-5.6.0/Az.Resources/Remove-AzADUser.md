---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 98d5433ca2a8d557c7ca1924b9edb6e4fdca2b2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970331"
---
# <span data-ttu-id="66343-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="66343-101">Remove-AzADUser</span></span>

## <span data-ttu-id="66343-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66343-102">SYNOPSIS</span></span>
<span data-ttu-id="66343-103">활성 디렉터리 사용자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="66343-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="66343-104">구문</span><span class="sxs-lookup"><span data-stu-id="66343-104">SYNTAX</span></span>

### <span data-ttu-id="66343-105">UPNOrObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="66343-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66343-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="66343-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66343-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66343-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66343-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66343-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66343-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66343-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66343-110">설명</span><span class="sxs-lookup"><span data-stu-id="66343-110">DESCRIPTION</span></span>
<span data-ttu-id="66343-111">활성 디렉터리 사용자(직장/학교 계정도 org-id라고도 합니다)를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="66343-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="66343-112">예제</span><span class="sxs-lookup"><span data-stu-id="66343-112">EXAMPLES</span></span>

### <span data-ttu-id="66343-113">예제 1: 사용자 주체 이름으로 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="66343-113">Example 1: Remove a user by user principal name</span></span>

```powershell
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="66343-114">테넌트에서 사용자 주체 이름 foo@domain.com ""을 사용하여 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="66343-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="66343-115">예제 2: 개체 ID로 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="66343-115">Example 2: Remove a user by object id</span></span>

```powershell
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="66343-116">테넌트에서 개체 ID '7a9582cf-88c4-4319-842b-7a5d60967a69'를 사용하여 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="66343-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="66343-117">예제 3: 배관을 사용하여 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="66343-117">Example 3: Remove a user by piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="66343-118">개체 ID '7a9582cf-88c4-4319-842b-7a5d60967a69'를 사용하여 사용자를 테넌트에서 사용자를 Remove-AzADUser cmdlet에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="66343-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="66343-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="66343-119">PARAMETERS</span></span>

### <span data-ttu-id="66343-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66343-120">-DefaultProfile</span></span>
<span data-ttu-id="66343-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="66343-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66343-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="66343-122">-DisplayName</span></span>
<span data-ttu-id="66343-123">삭제할 사용자의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66343-123">The display name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66343-124">-Force</span><span class="sxs-lookup"><span data-stu-id="66343-124">-Force</span></span>
<span data-ttu-id="66343-125">지정한 경우 사용자를 삭제하기 위한 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66343-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="66343-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66343-126">-InputObject</span></span>
<span data-ttu-id="66343-127">삭제할 사용자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="66343-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66343-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="66343-128">-ObjectId</span></span>
<span data-ttu-id="66343-129">삭제할 사용자의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="66343-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="66343-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66343-130">-PassThru</span></span>
<span data-ttu-id="66343-131">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="66343-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="66343-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="66343-132">-UPNOrObjectId</span></span>
<span data-ttu-id="66343-133">삭제할 사용자의 사용자 주체 이름 또는 objectId입니다.</span><span class="sxs-lookup"><span data-stu-id="66343-133">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66343-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="66343-134">-UserPrincipalName</span></span>
<span data-ttu-id="66343-135">삭제할 사용자의 사용자 주체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66343-135">The user principal name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66343-136">-확인</span><span class="sxs-lookup"><span data-stu-id="66343-136">-Confirm</span></span>
<span data-ttu-id="66343-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="66343-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66343-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66343-138">-WhatIf</span></span>
<span data-ttu-id="66343-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="66343-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66343-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66343-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66343-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66343-141">CommonParameters</span></span>
<span data-ttu-id="66343-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66343-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66343-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66343-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66343-144">입력</span><span class="sxs-lookup"><span data-stu-id="66343-144">INPUTS</span></span>

### <span data-ttu-id="66343-145">System.String</span><span class="sxs-lookup"><span data-stu-id="66343-145">System.String</span></span>

### <span data-ttu-id="66343-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="66343-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="66343-147">출력</span><span class="sxs-lookup"><span data-stu-id="66343-147">OUTPUTS</span></span>

### <span data-ttu-id="66343-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66343-148">System.Boolean</span></span>

## <span data-ttu-id="66343-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66343-149">NOTES</span></span>

## <span data-ttu-id="66343-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66343-150">RELATED LINKS</span></span>

[<span data-ttu-id="66343-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="66343-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="66343-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="66343-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="66343-153">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="66343-153">Update-AzADUser</span></span>](./Update-AzADUser.md)

