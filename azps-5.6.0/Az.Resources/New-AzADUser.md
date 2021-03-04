---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: 275f43d184e6b34aeeba83a9563a812649a6044c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967755"
---
# <span data-ttu-id="beff9-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="beff9-101">New-AzADUser</span></span>

## <span data-ttu-id="beff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beff9-102">SYNOPSIS</span></span>
<span data-ttu-id="beff9-103">새 활성 디렉터리 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="beff9-104">구문</span><span class="sxs-lookup"><span data-stu-id="beff9-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beff9-105">설명</span><span class="sxs-lookup"><span data-stu-id="beff9-105">DESCRIPTION</span></span>
<span data-ttu-id="beff9-106">새 활성 디렉터리 사용자(직장/학교 계정도 org-id라고도 합니다)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="beff9-107">자세한 내용은 https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="beff9-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="beff9-108">예제</span><span class="sxs-lookup"><span data-stu-id="beff9-108">EXAMPLES</span></span>

### <span data-ttu-id="beff9-109">예제 1: 새 AD 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="beff9-109">Example 1: Create a new AD user</span></span>
```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="beff9-110">테넌트에서 "MyDisplayName" 및 사용자 주체 이름 "으로 새 AD 사용자를 myemail@domain.com 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="beff9-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="beff9-111">PARAMETERS</span></span>

### <span data-ttu-id="beff9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beff9-112">-DefaultProfile</span></span>
<span data-ttu-id="beff9-113">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="beff9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="beff9-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="beff9-114">-DisplayName</span></span>
<span data-ttu-id="beff9-115">사용자의 주소 책에 표시할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="beff9-116">예제 'Alex Wu'.</span><span class="sxs-lookup"><span data-stu-id="beff9-116">example 'Alex Wu'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beff9-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="beff9-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="beff9-118">사용자가 성공한 다음 로그인(true)에서 암호를 변경해야 하는 경우 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="beff9-119">기본 동작은 성공한 다음 로그인에서 암호를 변경하지 않는(false)입니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beff9-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="beff9-120">-ImmutableId</span></span>
<span data-ttu-id="beff9-121">사용자의 사용자 주체 이름(upn) 속성에 페더리드 도메인을 사용하는 경우만 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beff9-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="beff9-122">-MailNickname</span></span>
<span data-ttu-id="beff9-123">사용자에 대한 메일 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-123">The mail alias for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beff9-124">-Password</span><span class="sxs-lookup"><span data-stu-id="beff9-124">-Password</span></span>
<span data-ttu-id="beff9-125">사용자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-125">Password for the user.</span></span>
<span data-ttu-id="beff9-126">테넌트의 암호 복잡성 요구 사항을 충족해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="beff9-127">강력한 암호를 설정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beff9-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="beff9-128">-UserPrincipalName</span></span>
<span data-ttu-id="beff9-129">사용자 주체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-129">The user principal name.</span></span>
<span data-ttu-id="beff9-130">예제-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="beff9-130">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beff9-131">-확인</span><span class="sxs-lookup"><span data-stu-id="beff9-131">-Confirm</span></span>
<span data-ttu-id="beff9-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beff9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beff9-133">-WhatIf</span></span>
<span data-ttu-id="beff9-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beff9-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beff9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beff9-136">CommonParameters</span></span>
<span data-ttu-id="beff9-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="beff9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beff9-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="beff9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beff9-139">입력</span><span class="sxs-lookup"><span data-stu-id="beff9-139">INPUTS</span></span>

### <span data-ttu-id="beff9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="beff9-140">System.String</span></span>

### <span data-ttu-id="beff9-141">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="beff9-141">System.Security.SecureString</span></span>

### <span data-ttu-id="beff9-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="beff9-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="beff9-143">출력</span><span class="sxs-lookup"><span data-stu-id="beff9-143">OUTPUTS</span></span>

### <span data-ttu-id="beff9-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="beff9-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="beff9-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="beff9-145">NOTES</span></span>

## <span data-ttu-id="beff9-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="beff9-146">RELATED LINKS</span></span>

[<span data-ttu-id="beff9-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="beff9-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="beff9-148">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="beff9-148">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="beff9-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="beff9-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
