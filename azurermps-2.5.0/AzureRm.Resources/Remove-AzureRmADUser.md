---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 51758c5b51c358a60be310405a89666cc56bac2e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880617"
---
# <span data-ttu-id="aae14-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="aae14-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="aae14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aae14-102">SYNOPSIS</span></span>
<span data-ttu-id="aae14-103">Active directory 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aae14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aae14-104">SYNTAX</span></span>

### <span data-ttu-id="aae14-105">UPNOrObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aae14-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aae14-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="aae14-106">UPNParameterSet</span></span>
```
Remove-AzureRmADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aae14-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aae14-107">ObjectIdParameterSet</span></span>
```
Remove-AzureRmADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aae14-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aae14-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aae14-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aae14-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aae14-110">설명은</span><span class="sxs-lookup"><span data-stu-id="aae14-110">DESCRIPTION</span></span>
<span data-ttu-id="aae14-111">Active directory 사용자 (회사/학교 계정 popularly 조직 id 라고도 함)를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="aae14-112">예제의</span><span class="sxs-lookup"><span data-stu-id="aae14-112">EXAMPLES</span></span>

### <span data-ttu-id="aae14-113">예제 1-upn (사용자 이름)으로 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="aae14-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="aae14-114">테 넌 트에서 사용자 이름 ""이 (가) 있는 사용자를 제거 합니다 foo@domain.com .</span><span class="sxs-lookup"><span data-stu-id="aae14-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="aae14-115">예제 2-개체 id로 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="aae14-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="aae14-116">테 넌 트에서 개체 id가 ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' 인 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="aae14-117">예제 3-파이핑을 사용 하 여 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="aae14-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzureRmADUser
```

<span data-ttu-id="aae14-118">개체 id가 ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' 인 사용자를 가져오고, 테 넌 트에서 사용자를 제거 하기 위해 Remove-AzureRmADUser cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzureRmADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="aae14-119">변수</span><span class="sxs-lookup"><span data-stu-id="aae14-119">PARAMETERS</span></span>

### <span data-ttu-id="aae14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae14-120">-DefaultProfile</span></span>
<span data-ttu-id="aae14-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aae14-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aae14-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="aae14-122">-DisplayName</span></span>
<span data-ttu-id="aae14-123">삭제할 사용자의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="aae14-124">-Force</span><span class="sxs-lookup"><span data-stu-id="aae14-124">-Force</span></span>
<span data-ttu-id="aae14-125">지정 된 경우 사용자 삭제 확인을 요청 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="aae14-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aae14-126">-InputObject</span></span>
<span data-ttu-id="aae14-127">삭제할 사용자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aae14-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="aae14-128">-ObjectId</span></span>
<span data-ttu-id="aae14-129">삭제할 사용자의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="aae14-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aae14-130">-PassThru</span></span>
<span data-ttu-id="aae14-131">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="aae14-132">-Up. Objectid</span><span class="sxs-lookup"><span data-stu-id="aae14-132">-UPNOrObjectId</span></span>
<span data-ttu-id="aae14-133">삭제할 사용자의 사용자 계정 이름 또는 objectId입니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="aae14-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="aae14-134">-UserPrincipalName</span></span>
<span data-ttu-id="aae14-135">삭제할 사용자의 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="aae14-136">-확인</span><span class="sxs-lookup"><span data-stu-id="aae14-136">-Confirm</span></span>
<span data-ttu-id="aae14-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aae14-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aae14-138">-WhatIf</span></span>
<span data-ttu-id="aae14-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aae14-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aae14-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae14-141">CommonParameters</span></span>
<span data-ttu-id="aae14-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aae14-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae14-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae14-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae14-144">입력</span><span class="sxs-lookup"><span data-stu-id="aae14-144">INPUTS</span></span>

### <span data-ttu-id="aae14-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aae14-145">System.String</span></span>

### <span data-ttu-id="aae14-146">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="aae14-146">System.Guid</span></span>

### <span data-ttu-id="aae14-147">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Aduser</span><span class="sxs-lookup"><span data-stu-id="aae14-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="aae14-148">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aae14-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="aae14-149">출력</span><span class="sxs-lookup"><span data-stu-id="aae14-149">OUTPUTS</span></span>

### <span data-ttu-id="aae14-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="aae14-150">System.Boolean</span></span>

## <span data-ttu-id="aae14-151">상속자</span><span class="sxs-lookup"><span data-stu-id="aae14-151">NOTES</span></span>

## <span data-ttu-id="aae14-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aae14-152">RELATED LINKS</span></span>

[<span data-ttu-id="aae14-153">새로운 AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="aae14-153">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="aae14-154">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="aae14-154">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)



