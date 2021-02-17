---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: b765e33479c6178d69fb670a2f18ef0169eadf35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205952"
---
# <span data-ttu-id="bc1d6-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="bc1d6-101">Update-AzADUser</span></span>

## <span data-ttu-id="bc1d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="bc1d6-103">기존 Active Directory 사용자를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="bc1d6-104">구문</span><span class="sxs-lookup"><span data-stu-id="bc1d6-104">SYNTAX</span></span>

### <span data-ttu-id="bc1d6-105">UPNOrObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bc1d6-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc1d6-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc1d6-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc1d6-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc1d6-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc1d6-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc1d6-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc1d6-109">설명</span><span class="sxs-lookup"><span data-stu-id="bc1d6-109">DESCRIPTION</span></span>
<span data-ttu-id="bc1d6-110">기존 Active Directory 사용자(org-id라고도 하는 직장/학교 계정)를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="bc1d6-111">자세한 내용은 https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="bc1d6-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="bc1d6-112">예제</span><span class="sxs-lookup"><span data-stu-id="bc1d6-112">EXAMPLES</span></span>

### <span data-ttu-id="bc1d6-113">예제 1: 개체 ID를 사용하여 사용자의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="bc1d6-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="bc1d6-114">개체 ID '155a5c10-93a9-4941-a0df-96d83ab5ab24'로 사용자의 표시 이름을 'MyNewDisplayName'으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="bc1d6-115">예제 2: 사용자 계정 이름을 사용하여 사용자의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="bc1d6-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="bc1d6-116">사용자의 표시 이름을 foo@domain.com 'MyNewDisplayName'으로 사용자 계정 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="bc1d6-117">예제 3: 파이핑을 사용하여 사용자의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="bc1d6-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="bc1d6-118">개체 ID가 '155a5c10-93a9-4941-a0df-96d83ab5ab24'인 사용자를 다운로드하고 해당 사용자의 표시 이름을 'MyNewDisplayName'으로 업데이트하기 위해 Update-AzADUser cmdlet에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="bc1d6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc1d6-119">PARAMETERS</span></span>

### <span data-ttu-id="bc1d6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc1d6-120">-DefaultProfile</span></span>
<span data-ttu-id="bc1d6-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc1d6-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc1d6-122">-DisplayName</span></span>
<span data-ttu-id="bc1d6-123">사용자의 새 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-123">New display name for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc1d6-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="bc1d6-124">-EnableAccount</span></span>
<span data-ttu-id="bc1d6-125">계정을 사용하도록 설정하는 경우 true입니다. 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-125">true for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc1d6-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="bc1d6-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="bc1d6-127">사용자가 다음에 성공한 로그인에서 암호를 변경해야 하는 경우 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="bc1d6-128">암호가 업데이트된 경우만 유효합니다. 그렇지 않으면 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="bc1d6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc1d6-129">-InputObject</span></span>
<span data-ttu-id="bc1d6-130">업데이트할 사용자를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="bc1d6-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bc1d6-131">-ObjectId</span></span>
<span data-ttu-id="bc1d6-132">업데이트할 사용자의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="bc1d6-133">-Password</span><span class="sxs-lookup"><span data-stu-id="bc1d6-133">-Password</span></span>
<span data-ttu-id="bc1d6-134">사용자의 새 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-134">New password for the user.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc1d6-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="bc1d6-135">-UPNOrObjectId</span></span>
<span data-ttu-id="bc1d6-136">업데이트할 사용자의 사용자 계정 이름 또는 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="bc1d6-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bc1d6-137">-UserPrincipalName</span></span>
<span data-ttu-id="bc1d6-138">업데이트할 사용자의 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="bc1d6-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc1d6-139">-Confirm</span></span>
<span data-ttu-id="bc1d6-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc1d6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc1d6-141">-WhatIf</span></span>
<span data-ttu-id="bc1d6-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bc1d6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc1d6-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc1d6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc1d6-144">CommonParameters</span></span>
<span data-ttu-id="bc1d6-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc1d6-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc1d6-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc1d6-147">입력</span><span class="sxs-lookup"><span data-stu-id="bc1d6-147">INPUTS</span></span>

### <span data-ttu-id="bc1d6-148">System.String</span><span class="sxs-lookup"><span data-stu-id="bc1d6-148">System.String</span></span>

### <span data-ttu-id="bc1d6-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="bc1d6-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="bc1d6-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc1d6-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bc1d6-151">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="bc1d6-151">System.Security.SecureString</span></span>

## <span data-ttu-id="bc1d6-152">출력</span><span class="sxs-lookup"><span data-stu-id="bc1d6-152">OUTPUTS</span></span>

### <span data-ttu-id="bc1d6-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="bc1d6-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="bc1d6-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bc1d6-154">NOTES</span></span>

## <span data-ttu-id="bc1d6-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc1d6-155">RELATED LINKS</span></span>
