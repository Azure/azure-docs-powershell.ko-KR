---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 50cb6a806522e8e8b0f3a792ad74e2543633f668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699406"
---
# <span data-ttu-id="c7f2d-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="c7f2d-101">New-AzADGroup</span></span>

## <span data-ttu-id="c7f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f2d-103">새 active directory 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="c7f2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7f2d-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7f2d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c7f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="c7f2d-106">새 active directory 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="c7f2d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c7f2d-107">EXAMPLES</span></span>

### <span data-ttu-id="c7f2d-108">예제 1-새 광고 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="c7f2d-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="c7f2d-109">"MyGroupDisplayName" 이라는 이름과 메일 애칭 "MyGroupNick"을 사용 하 여 새 광고 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="c7f2d-110">변수</span><span class="sxs-lookup"><span data-stu-id="c7f2d-110">PARAMETERS</span></span>

### <span data-ttu-id="c7f2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f2d-111">-DefaultProfile</span></span>
<span data-ttu-id="c7f2d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7f2d-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7f2d-113">-DisplayName</span></span>
<span data-ttu-id="c7f2d-114">그룹에 대 한 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-114">The display name for the group.</span></span>

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

### <span data-ttu-id="c7f2d-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="c7f2d-115">-MailNickname</span></span>
<span data-ttu-id="c7f2d-116">그룹의 메일 애칭입니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-116">The mail nickname for the group.</span></span> <span data-ttu-id="c7f2d-117">@ 기호를 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-117">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="c7f2d-118">-확인</span><span class="sxs-lookup"><span data-stu-id="c7f2d-118">-Confirm</span></span>
<span data-ttu-id="c7f2d-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7f2d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7f2d-120">-WhatIf</span></span>
<span data-ttu-id="c7f2d-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7f2d-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7f2d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f2d-123">CommonParameters</span></span>
<span data-ttu-id="c7f2d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7f2d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f2d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f2d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f2d-126">입력</span><span class="sxs-lookup"><span data-stu-id="c7f2d-126">INPUTS</span></span>

### <span data-ttu-id="c7f2d-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7f2d-127">System.String</span></span>

## <span data-ttu-id="c7f2d-128">출력</span><span class="sxs-lookup"><span data-stu-id="c7f2d-128">OUTPUTS</span></span>

### <span data-ttu-id="c7f2d-129">ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="c7f2d-129">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="c7f2d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="c7f2d-130">NOTES</span></span>

## <span data-ttu-id="c7f2d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7f2d-131">RELATED LINKS</span></span>