---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADGroup.md
ms.openlocfilehash: 751b1b7daff59861b3f8e480b27dc4c88d35709d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530080"
---
# <span data-ttu-id="26203-101">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="26203-101">New-AzureRmADGroup</span></span>

## <span data-ttu-id="26203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26203-102">SYNOPSIS</span></span>
<span data-ttu-id="26203-103">새 active directory 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26203-103">Creates a new active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26203-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26203-104">SYNTAX</span></span>

```
New-AzureRmADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26203-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26203-105">DESCRIPTION</span></span>
<span data-ttu-id="26203-106">새 active directory 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26203-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="26203-107">예제의</span><span class="sxs-lookup"><span data-stu-id="26203-107">EXAMPLES</span></span>

### <span data-ttu-id="26203-108">예제 1-새 광고 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="26203-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzureRmADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="26203-109">"MyGroupDisplayName" 이라는 이름과 메일 애칭 ""을 사용 하 여 새 광고 그룹을 만듭니다 myemail@domain.com .</span><span class="sxs-lookup"><span data-stu-id="26203-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="26203-110">변수</span><span class="sxs-lookup"><span data-stu-id="26203-110">PARAMETERS</span></span>

### <span data-ttu-id="26203-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26203-111">-DefaultProfile</span></span>
<span data-ttu-id="26203-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26203-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26203-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="26203-113">-DisplayName</span></span>
<span data-ttu-id="26203-114">그룹에 대 한 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26203-114">The display name for the group.</span></span>

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

### <span data-ttu-id="26203-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="26203-115">-MailNickname</span></span>
<span data-ttu-id="26203-116">그룹의 메일 애칭입니다.</span><span class="sxs-lookup"><span data-stu-id="26203-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="26203-117">-확인</span><span class="sxs-lookup"><span data-stu-id="26203-117">-Confirm</span></span>
<span data-ttu-id="26203-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26203-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26203-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26203-119">-WhatIf</span></span>
<span data-ttu-id="26203-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26203-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26203-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26203-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26203-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26203-122">CommonParameters</span></span>
<span data-ttu-id="26203-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26203-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26203-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26203-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26203-125">입력</span><span class="sxs-lookup"><span data-stu-id="26203-125">INPUTS</span></span>

### <span data-ttu-id="26203-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="26203-126">System.String</span></span>

## <span data-ttu-id="26203-127">출력</span><span class="sxs-lookup"><span data-stu-id="26203-127">OUTPUTS</span></span>

### <span data-ttu-id="26203-128">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="26203-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="26203-129">상속자</span><span class="sxs-lookup"><span data-stu-id="26203-129">NOTES</span></span>

## <span data-ttu-id="26203-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26203-130">RELATED LINKS</span></span>
