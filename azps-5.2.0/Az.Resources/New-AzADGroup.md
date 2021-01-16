---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358086"
---
# <span data-ttu-id="2895b-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="2895b-101">New-AzADGroup</span></span>

## <span data-ttu-id="2895b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2895b-102">SYNOPSIS</span></span>
<span data-ttu-id="2895b-103">새 Active Directory 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="2895b-104">구문</span><span class="sxs-lookup"><span data-stu-id="2895b-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2895b-105">설명</span><span class="sxs-lookup"><span data-stu-id="2895b-105">DESCRIPTION</span></span>
<span data-ttu-id="2895b-106">새 Active Directory 그룹을 만듭니다. 필요한 권한은 아래와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="2895b-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="2895b-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="2895b-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2895b-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="2895b-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="2895b-109">Microsoft Graph</span></span>
  - <span data-ttu-id="2895b-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2895b-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="2895b-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="2895b-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="2895b-112">예제</span><span class="sxs-lookup"><span data-stu-id="2895b-112">EXAMPLES</span></span>

### <span data-ttu-id="2895b-113">예제 1: 새 AD 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="2895b-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="2895b-114">이름이 "MyGroupDisplayName"이고 메일 애칭이 "MyGroupNick"인 새 AD 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="2895b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2895b-115">PARAMETERS</span></span>

### <span data-ttu-id="2895b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2895b-116">-DefaultProfile</span></span>
<span data-ttu-id="2895b-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2895b-118">-Description</span><span class="sxs-lookup"><span data-stu-id="2895b-118">-Description</span></span>
<span data-ttu-id="2895b-119">그룹에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-119">The description for the group.</span></span>

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

### <span data-ttu-id="2895b-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2895b-120">-DisplayName</span></span>
<span data-ttu-id="2895b-121">그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-121">The display name for the group.</span></span>

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

### <span data-ttu-id="2895b-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="2895b-122">-MailNickname</span></span>
<span data-ttu-id="2895b-123">그룹의 메일 별명입니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-123">The mail nickname for the group.</span></span> <span data-ttu-id="2895b-124">@ 기호를 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="2895b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2895b-125">-Confirm</span></span>
<span data-ttu-id="2895b-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2895b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2895b-127">-WhatIf</span></span>
<span data-ttu-id="2895b-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2895b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2895b-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2895b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2895b-130">CommonParameters</span></span>
<span data-ttu-id="2895b-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2895b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2895b-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2895b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2895b-133">입력</span><span class="sxs-lookup"><span data-stu-id="2895b-133">INPUTS</span></span>

### <span data-ttu-id="2895b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2895b-134">System.String</span></span>

## <span data-ttu-id="2895b-135">출력</span><span class="sxs-lookup"><span data-stu-id="2895b-135">OUTPUTS</span></span>

### <span data-ttu-id="2895b-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="2895b-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="2895b-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2895b-137">NOTES</span></span>

## <span data-ttu-id="2895b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2895b-138">RELATED LINKS</span></span>
