---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: 13b157accea6303363aebca54eb68a5f0ffbd6d9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044458"
---
# <span data-ttu-id="2f0a0-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="2f0a0-101">New-AzADUser</span></span>

## <span data-ttu-id="2f0a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0a0-103">새 active directory 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="2f0a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f0a0-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f0a0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2f0a0-105">DESCRIPTION</span></span>
<span data-ttu-id="2f0a0-106">새 active directory 사용자 (회사/학교 계정 popularly 조직 id 라고도 함)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="2f0a0-107">추가 정보: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="2f0a0-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="2f0a0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2f0a0-108">EXAMPLES</span></span>

### <span data-ttu-id="2f0a0-109">예제 1-새 광고 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="2f0a0-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="2f0a0-110">테 넌 트에 "MyDisplayName" 및 user principal name "" 이라는 이름의 새 광고 사용자를 만듭니다 myemail@domain.com .</span><span class="sxs-lookup"><span data-stu-id="2f0a0-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="2f0a0-111">변수</span><span class="sxs-lookup"><span data-stu-id="2f0a0-111">PARAMETERS</span></span>

### <span data-ttu-id="2f0a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0a0-112">-DefaultProfile</span></span>
<span data-ttu-id="2f0a0-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2f0a0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f0a0-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2f0a0-114">-DisplayName</span></span>
<span data-ttu-id="2f0a0-115">사용자의 주소록에 표시할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="2f0a0-116">' 정 Wu ' 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="2f0a0-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="2f0a0-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="2f0a0-118">사용자가 다음에 성공한 로그인 (true)에서 암호를 변경 해야 하는 경우에는이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="2f0a0-119">기본 동작 (false)은 다음 로그인에 대 한 암호를 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="2f0a0-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="2f0a0-120">-ImmutableId</span></span>
<span data-ttu-id="2f0a0-121">사용자의 upn (사용자 계정 이름) 속성에 페더레이션 도메인을 사용 하는 경우에만 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="2f0a0-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="2f0a0-122">-MailNickname</span></span>
<span data-ttu-id="2f0a0-123">사용자의 메일 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="2f0a0-124">-암호</span><span class="sxs-lookup"><span data-stu-id="2f0a0-124">-Password</span></span>
<span data-ttu-id="2f0a0-125">사용자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-125">Password for the user.</span></span>
<span data-ttu-id="2f0a0-126">테 넌 트의 암호 복잡성 요구 사항을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="2f0a0-127">강력한 암호를 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="2f0a0-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2f0a0-128">-UserPrincipalName</span></span>
<span data-ttu-id="2f0a0-129">사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-129">The user principal name.</span></span>
<span data-ttu-id="2f0a0-130">예-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="2f0a0-131">-확인</span><span class="sxs-lookup"><span data-stu-id="2f0a0-131">-Confirm</span></span>
<span data-ttu-id="2f0a0-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f0a0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f0a0-133">-WhatIf</span></span>
<span data-ttu-id="2f0a0-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f0a0-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f0a0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0a0-136">CommonParameters</span></span>
<span data-ttu-id="2f0a0-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0a0-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2f0a0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0a0-139">입력</span><span class="sxs-lookup"><span data-stu-id="2f0a0-139">INPUTS</span></span>

### <span data-ttu-id="2f0a0-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2f0a0-140">System.String</span></span>

### <span data-ttu-id="2f0a0-141">System.webserver</span><span class="sxs-lookup"><span data-stu-id="2f0a0-141">System.Security.SecureString</span></span>

### <span data-ttu-id="2f0a0-142">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2f0a0-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f0a0-143">출력</span><span class="sxs-lookup"><span data-stu-id="2f0a0-143">OUTPUTS</span></span>

### <span data-ttu-id="2f0a0-144">ActiveDirectory를 사용 하 여 명령을 이동할 때</span><span class="sxs-lookup"><span data-stu-id="2f0a0-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="2f0a0-145">상속자</span><span class="sxs-lookup"><span data-stu-id="2f0a0-145">NOTES</span></span>

## <span data-ttu-id="2f0a0-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f0a0-146">RELATED LINKS</span></span>

[<span data-ttu-id="2f0a0-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="2f0a0-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="2f0a0-148">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="2f0a0-148">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="2f0a0-149">제거-AzADUser</span><span class="sxs-lookup"><span data-stu-id="2f0a0-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
