---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: 3875b697b801760b2db78ecfa55f3cbfc734b250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970315"
---
# <span data-ttu-id="7a3ab-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7a3ab-101">Update-AzADUser</span></span>

## <span data-ttu-id="7a3ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="7a3ab-103">기존 활성 디렉터리 사용자를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="7a3ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a3ab-104">SYNTAX</span></span>

### <span data-ttu-id="7a3ab-105">UPNOrObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a3ab-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a3ab-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a3ab-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a3ab-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a3ab-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a3ab-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a3ab-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a3ab-109">설명</span><span class="sxs-lookup"><span data-stu-id="7a3ab-109">DESCRIPTION</span></span>
<span data-ttu-id="7a3ab-110">기존 활성 디렉터리 사용자(직장/학교 계정도 org-id라고도 합니다)를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="7a3ab-111">자세한 내용은 https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="7a3ab-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="7a3ab-112">예제</span><span class="sxs-lookup"><span data-stu-id="7a3ab-112">EXAMPLES</span></span>

### <span data-ttu-id="7a3ab-113">예제 1: 개체 ID를 사용하여 사용자의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="7a3ab-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="7a3ab-114">개체 ID '155a5c10-93a9-4941-a0df-96d83ab5ab24'로 사용자의 표시 이름을 'MyNewDisplayName'로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="7a3ab-115">예제 2: 사용자 주체 이름을 사용하여 사용자의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="7a3ab-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="7a3ab-116">사용자 주체 이름으로 사용자의 표시 이름을 foo@domain.com 'myNewDisplayName'로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="7a3ab-117">예제 3: 배관을 사용하여 사용자의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="7a3ab-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="7a3ab-118">개체 ID '155a5c10-93a9-4941-a0df-96d83ab5ab24' 및 해당 사용자의 표시 이름을 'myNewDisplayName'으로 업데이트하기 위해 Update-AzADUser cmdlet에 파이프를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="7a3ab-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7a3ab-119">PARAMETERS</span></span>

### <span data-ttu-id="7a3ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a3ab-120">-DefaultProfile</span></span>
<span data-ttu-id="7a3ab-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a3ab-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7a3ab-122">-DisplayName</span></span>
<span data-ttu-id="7a3ab-123">사용자의 새 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-123">New display name for the user.</span></span>

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

### <span data-ttu-id="7a3ab-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="7a3ab-124">-EnableAccount</span></span>
<span data-ttu-id="7a3ab-125">계정을 사용하도록 설정하기 위한 true; 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="7a3ab-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="7a3ab-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="7a3ab-127">사용자가 성공한 다음 로그인에서 암호를 변경해야 하는지 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="7a3ab-128">암호가 업데이트된 경우만 유효합니다. 그렇지 않으면 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="7a3ab-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a3ab-129">-InputObject</span></span>
<span data-ttu-id="7a3ab-130">업데이트할 사용자를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="7a3ab-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7a3ab-131">-ObjectId</span></span>
<span data-ttu-id="7a3ab-132">업데이트할 사용자의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="7a3ab-133">-Password</span><span class="sxs-lookup"><span data-stu-id="7a3ab-133">-Password</span></span>
<span data-ttu-id="7a3ab-134">사용자의 새 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-134">New password for the user.</span></span>

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

### <span data-ttu-id="7a3ab-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="7a3ab-135">-UPNOrObjectId</span></span>
<span data-ttu-id="7a3ab-136">업데이트할 사용자의 사용자 주체 이름 또는 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="7a3ab-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7a3ab-137">-UserPrincipalName</span></span>
<span data-ttu-id="7a3ab-138">업데이트할 사용자의 사용자 주체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="7a3ab-139">-확인</span><span class="sxs-lookup"><span data-stu-id="7a3ab-139">-Confirm</span></span>
<span data-ttu-id="7a3ab-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a3ab-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a3ab-141">-WhatIf</span></span>
<span data-ttu-id="7a3ab-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a3ab-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a3ab-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a3ab-144">CommonParameters</span></span>
<span data-ttu-id="7a3ab-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a3ab-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a3ab-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a3ab-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a3ab-147">입력</span><span class="sxs-lookup"><span data-stu-id="7a3ab-147">INPUTS</span></span>

### <span data-ttu-id="7a3ab-148">System.String</span><span class="sxs-lookup"><span data-stu-id="7a3ab-148">System.String</span></span>

### <span data-ttu-id="7a3ab-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="7a3ab-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="7a3ab-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7a3ab-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7a3ab-151">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="7a3ab-151">System.Security.SecureString</span></span>

## <span data-ttu-id="7a3ab-152">출력</span><span class="sxs-lookup"><span data-stu-id="7a3ab-152">OUTPUTS</span></span>

### <span data-ttu-id="7a3ab-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="7a3ab-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="7a3ab-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a3ab-154">NOTES</span></span>

## <span data-ttu-id="7a3ab-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a3ab-155">RELATED LINKS</span></span>
