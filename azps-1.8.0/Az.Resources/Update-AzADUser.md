---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: 27d97a89aed930dad33cca0ba0382267a3f6d3fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699287"
---
# <span data-ttu-id="d37e0-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d37e0-101">Update-AzADUser</span></span>

## <span data-ttu-id="d37e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d37e0-103">기존 active directory 사용자를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="d37e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d37e0-104">SYNTAX</span></span>

### <span data-ttu-id="d37e0-105">UPNOrObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d37e0-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d37e0-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d37e0-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d37e0-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d37e0-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d37e0-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d37e0-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37e0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d37e0-109">DESCRIPTION</span></span>
<span data-ttu-id="d37e0-110">기존 active directory 사용자를 업데이트 합니다 (회사/학교 계정에도 popularly 알려진 조직 id).</span><span class="sxs-lookup"><span data-stu-id="d37e0-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="d37e0-111">추가 정보: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="d37e0-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="d37e0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d37e0-112">EXAMPLES</span></span>

### <span data-ttu-id="d37e0-113">예제 1-개체 id를 사용 하 여 사용자의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="d37e0-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="d37e0-114">개체 id가 ' 155a5c10-93a9-4941-a0df-96d83ab5ab24 ' 인 사용자의 표시 이름을 ' MyNewDisplayName '로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="d37e0-115">예제 2-사용자 계정 이름을 사용 하 여 사용자의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="d37e0-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="d37e0-116">사용자 계정 이름이 ' ' 인 사용자의 표시 이름을 foo@domain.com ' MyNewDisplayName '로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="d37e0-117">예제 3-파이핑을 사용 하 여 사용자의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="d37e0-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="d37e0-118">개체 id가 ' 155a5c10-93a9-4941-a0df-96d83ab5ab24 ' 인 사용자를 가져오고 해당 사용자의 표시 이름을 ' MyNewDisplayName '로 업데이트 하도록 Update-AzADUser cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="d37e0-119">변수</span><span class="sxs-lookup"><span data-stu-id="d37e0-119">PARAMETERS</span></span>

### <span data-ttu-id="d37e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37e0-120">-DefaultProfile</span></span>
<span data-ttu-id="d37e0-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37e0-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d37e0-122">-DisplayName</span></span>
<span data-ttu-id="d37e0-123">사용자의 새 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-123">New display name for the user.</span></span>

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

### <span data-ttu-id="d37e0-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="d37e0-124">-EnableAccount</span></span>
<span data-ttu-id="d37e0-125">계정을 사용 하도록 설정 하려면 true이 고, 그렇지 않으면 false입니다. 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="d37e0-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="d37e0-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="d37e0-127">사용자가 다음에 로그인 할 때 암호를 변경 해야 하는 경우이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="d37e0-128">암호를 업데이트 한 경우에만 유효 하며, 그렇지 않은 경우 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="d37e0-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d37e0-129">-InputObject</span></span>
<span data-ttu-id="d37e0-130">업데이트할 사용자를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="d37e0-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d37e0-131">-ObjectId</span></span>
<span data-ttu-id="d37e0-132">업데이트할 사용자의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="d37e0-133">-암호</span><span class="sxs-lookup"><span data-stu-id="d37e0-133">-Password</span></span>
<span data-ttu-id="d37e0-134">사용자의 새 비밀 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-134">New password for the user.</span></span>

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

### <span data-ttu-id="d37e0-135">-Up. Objectid</span><span class="sxs-lookup"><span data-stu-id="d37e0-135">-UPNOrObjectId</span></span>
<span data-ttu-id="d37e0-136">업데이트할 사용자의 사용자 주체 이름 또는 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="d37e0-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d37e0-137">-UserPrincipalName</span></span>
<span data-ttu-id="d37e0-138">업데이트할 사용자의 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="d37e0-139">-확인</span><span class="sxs-lookup"><span data-stu-id="d37e0-139">-Confirm</span></span>
<span data-ttu-id="d37e0-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37e0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37e0-141">-WhatIf</span></span>
<span data-ttu-id="d37e0-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d37e0-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37e0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37e0-144">CommonParameters</span></span>
<span data-ttu-id="d37e0-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37e0-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d37e0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37e0-147">입력</span><span class="sxs-lookup"><span data-stu-id="d37e0-147">INPUTS</span></span>

### <span data-ttu-id="d37e0-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d37e0-148">System.String</span></span>

### <span data-ttu-id="d37e0-149">ActiveDirectory를 사용 하 여 명령을 이동할 때</span><span class="sxs-lookup"><span data-stu-id="d37e0-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="d37e0-150">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d37e0-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d37e0-151">System.webserver</span><span class="sxs-lookup"><span data-stu-id="d37e0-151">System.Security.SecureString</span></span>

## <span data-ttu-id="d37e0-152">출력</span><span class="sxs-lookup"><span data-stu-id="d37e0-152">OUTPUTS</span></span>

### <span data-ttu-id="d37e0-153">ActiveDirectory를 사용 하 여 명령을 이동할 때</span><span class="sxs-lookup"><span data-stu-id="d37e0-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="d37e0-154">상속자</span><span class="sxs-lookup"><span data-stu-id="d37e0-154">NOTES</span></span>

## <span data-ttu-id="d37e0-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d37e0-155">RELATED LINKS</span></span>
