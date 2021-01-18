---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494552"
---
# <span data-ttu-id="045f5-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="045f5-101">Save-AzContext</span></span>

## <span data-ttu-id="045f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="045f5-102">SYNOPSIS</span></span>
<span data-ttu-id="045f5-103">다른 PowerShell 세션에서 사용하기 위해 현재 인증 정보를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="045f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="045f5-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="045f5-105">설명</span><span class="sxs-lookup"><span data-stu-id="045f5-105">DESCRIPTION</span></span>
<span data-ttu-id="045f5-106">이 Save-AzContext cmdlet은 다른 PowerShell 세션에서 사용하기 위해 현재 인증 정보를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="045f5-107">예제</span><span class="sxs-lookup"><span data-stu-id="045f5-107">EXAMPLES</span></span>

### <span data-ttu-id="045f5-108">예제 1: 현재 세션의 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="045f5-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="045f5-109">이 예제에서는 현재 세션의 Azure 컨텍스트를 제공된 JSON 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="045f5-110">예제 2: 주어진 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="045f5-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="045f5-111">이 예제에서는 cmdlet을 통해 제공된 JSON 파일에 전달된 Azure 컨텍스트를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="045f5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="045f5-112">PARAMETERS</span></span>

### <span data-ttu-id="045f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="045f5-113">-DefaultProfile</span></span>
<span data-ttu-id="045f5-114">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="045f5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="045f5-115">-Force</span></span>
<span data-ttu-id="045f5-116">주어진 파일이 있는 경우 덮어 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="045f5-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="045f5-117">-Path</span><span class="sxs-lookup"><span data-stu-id="045f5-117">-Path</span></span>
<span data-ttu-id="045f5-118">인증 정보를 저장할 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-118">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="045f5-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="045f5-119">-Profile</span></span>
<span data-ttu-id="045f5-120">이 cmdlet이 읽는 Azure 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="045f5-121">컨텍스트를 지정하지 않으면 이 cmdlet은 로컬 기본 컨텍스트에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="045f5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="045f5-122">-Confirm</span></span>
<span data-ttu-id="045f5-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="045f5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="045f5-124">-WhatIf</span></span>
<span data-ttu-id="045f5-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="045f5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="045f5-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="045f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="045f5-127">CommonParameters</span></span>
<span data-ttu-id="045f5-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="045f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="045f5-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="045f5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="045f5-130">입력</span><span class="sxs-lookup"><span data-stu-id="045f5-130">INPUTS</span></span>

### <span data-ttu-id="045f5-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="045f5-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="045f5-132">출력</span><span class="sxs-lookup"><span data-stu-id="045f5-132">OUTPUTS</span></span>

### <span data-ttu-id="045f5-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="045f5-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="045f5-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="045f5-134">NOTES</span></span>

## <span data-ttu-id="045f5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="045f5-135">RELATED LINKS</span></span>
