---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056066"
---
# <span data-ttu-id="41f88-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="41f88-101">New-AzADGroup</span></span>

## <span data-ttu-id="41f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41f88-102">SYNOPSIS</span></span>
<span data-ttu-id="41f88-103">새 active directory 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="41f88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41f88-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41f88-105">설명은</span><span class="sxs-lookup"><span data-stu-id="41f88-105">DESCRIPTION</span></span>
<span data-ttu-id="41f88-106">새 active directory 그룹을 만듭니다. 필요한 사용 권한은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="41f88-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="41f88-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="41f88-108">Directory. a $ $</span><span class="sxs-lookup"><span data-stu-id="41f88-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="41f88-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="41f88-109">Microsoft Graph</span></span>
  - <span data-ttu-id="41f88-110">Directory. a $ $</span><span class="sxs-lookup"><span data-stu-id="41f88-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="41f88-111">PrivilegedAccess AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="41f88-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="41f88-112">예제의</span><span class="sxs-lookup"><span data-stu-id="41f88-112">EXAMPLES</span></span>

### <span data-ttu-id="41f88-113">예제 1: 새 광고 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="41f88-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="41f88-114">"MyGroupDisplayName" 이라는 이름과 메일 애칭 "MyGroupNick"을 사용 하 여 새 광고 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="41f88-115">변수</span><span class="sxs-lookup"><span data-stu-id="41f88-115">PARAMETERS</span></span>

### <span data-ttu-id="41f88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f88-116">-DefaultProfile</span></span>
<span data-ttu-id="41f88-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41f88-118">-설명</span><span class="sxs-lookup"><span data-stu-id="41f88-118">-Description</span></span>
<span data-ttu-id="41f88-119">그룹에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-119">The description for the group.</span></span>

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

### <span data-ttu-id="41f88-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="41f88-120">-DisplayName</span></span>
<span data-ttu-id="41f88-121">그룹에 대 한 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-121">The display name for the group.</span></span>

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

### <span data-ttu-id="41f88-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="41f88-122">-MailNickname</span></span>
<span data-ttu-id="41f88-123">그룹의 메일 애칭입니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-123">The mail nickname for the group.</span></span> <span data-ttu-id="41f88-124">@ 기호를 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="41f88-125">-확인</span><span class="sxs-lookup"><span data-stu-id="41f88-125">-Confirm</span></span>
<span data-ttu-id="41f88-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41f88-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f88-127">-WhatIf</span></span>
<span data-ttu-id="41f88-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41f88-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41f88-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f88-130">CommonParameters</span></span>
<span data-ttu-id="41f88-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41f88-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f88-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="41f88-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f88-133">입력</span><span class="sxs-lookup"><span data-stu-id="41f88-133">INPUTS</span></span>

### <span data-ttu-id="41f88-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41f88-134">System.String</span></span>

## <span data-ttu-id="41f88-135">출력</span><span class="sxs-lookup"><span data-stu-id="41f88-135">OUTPUTS</span></span>

### <span data-ttu-id="41f88-136">ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="41f88-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="41f88-137">상속자</span><span class="sxs-lookup"><span data-stu-id="41f88-137">NOTES</span></span>

## <span data-ttu-id="41f88-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41f88-138">RELATED LINKS</span></span>
