---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308768"
---
# <span data-ttu-id="6d51f-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="6d51f-101">New-AzADGroup</span></span>

## <span data-ttu-id="6d51f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d51f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d51f-103">새 active directory 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="6d51f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d51f-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d51f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6d51f-105">DESCRIPTION</span></span>
<span data-ttu-id="6d51f-106">새 active directory 그룹을 만듭니다. 필요한 사용 권한은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="6d51f-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="6d51f-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="6d51f-108">Directory. a $ $</span><span class="sxs-lookup"><span data-stu-id="6d51f-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="6d51f-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="6d51f-109">Microsoft Graph</span></span>
  - <span data-ttu-id="6d51f-110">Directory. a $ $</span><span class="sxs-lookup"><span data-stu-id="6d51f-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="6d51f-111">PrivilegedAccess AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="6d51f-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="6d51f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="6d51f-112">EXAMPLES</span></span>

### <span data-ttu-id="6d51f-113">예제 1: 새 광고 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="6d51f-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="6d51f-114">"MyGroupDisplayName" 이라는 이름과 메일 애칭 "MyGroupNick"을 사용 하 여 새 광고 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="6d51f-115">변수</span><span class="sxs-lookup"><span data-stu-id="6d51f-115">PARAMETERS</span></span>

### <span data-ttu-id="6d51f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d51f-116">-DefaultProfile</span></span>
<span data-ttu-id="6d51f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d51f-118">-설명</span><span class="sxs-lookup"><span data-stu-id="6d51f-118">-Description</span></span>
<span data-ttu-id="6d51f-119">그룹에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-119">The description for the group.</span></span>

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

### <span data-ttu-id="6d51f-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6d51f-120">-DisplayName</span></span>
<span data-ttu-id="6d51f-121">그룹에 대 한 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-121">The display name for the group.</span></span>

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

### <span data-ttu-id="6d51f-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="6d51f-122">-MailNickname</span></span>
<span data-ttu-id="6d51f-123">그룹의 메일 애칭입니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-123">The mail nickname for the group.</span></span> <span data-ttu-id="6d51f-124">@ 기호를 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="6d51f-125">-확인</span><span class="sxs-lookup"><span data-stu-id="6d51f-125">-Confirm</span></span>
<span data-ttu-id="6d51f-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d51f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d51f-127">-WhatIf</span></span>
<span data-ttu-id="6d51f-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d51f-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d51f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d51f-130">CommonParameters</span></span>
<span data-ttu-id="6d51f-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d51f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d51f-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6d51f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d51f-133">입력</span><span class="sxs-lookup"><span data-stu-id="6d51f-133">INPUTS</span></span>

### <span data-ttu-id="6d51f-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d51f-134">System.String</span></span>

## <span data-ttu-id="6d51f-135">출력</span><span class="sxs-lookup"><span data-stu-id="6d51f-135">OUTPUTS</span></span>

### <span data-ttu-id="6d51f-136">ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="6d51f-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="6d51f-137">상속자</span><span class="sxs-lookup"><span data-stu-id="6d51f-137">NOTES</span></span>

## <span data-ttu-id="6d51f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d51f-138">RELATED LINKS</span></span>
