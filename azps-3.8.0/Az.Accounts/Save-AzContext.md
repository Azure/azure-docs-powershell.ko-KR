---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042005"
---
# <span data-ttu-id="f150a-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="f150a-101">Save-AzContext</span></span>

## <span data-ttu-id="f150a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f150a-102">SYNOPSIS</span></span>
<span data-ttu-id="f150a-103">다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="f150a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f150a-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f150a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f150a-105">DESCRIPTION</span></span>
<span data-ttu-id="f150a-106">Save-AzContext cmdlet은 다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="f150a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f150a-107">EXAMPLES</span></span>

### <span data-ttu-id="f150a-108">예제 1: 현재 세션의 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="f150a-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="f150a-109">이 예제에서는 현재 세션의 Azure 컨텍스트를 제공 된 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="f150a-110">예제 2: 지정 된 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="f150a-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="f150a-111">이 예제에서는 cmdlet에 전달 된 Azure 컨텍스트를 제공 된 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="f150a-112">변수</span><span class="sxs-lookup"><span data-stu-id="f150a-112">PARAMETERS</span></span>

### <span data-ttu-id="f150a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f150a-113">-DefaultProfile</span></span>
<span data-ttu-id="f150a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f150a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f150a-115">-Force</span></span>
<span data-ttu-id="f150a-116">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="f150a-117">-Path</span><span class="sxs-lookup"><span data-stu-id="f150a-117">-Path</span></span>
<span data-ttu-id="f150a-118">인증 정보를 저장할 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="f150a-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="f150a-119">-Profile</span></span>
<span data-ttu-id="f150a-120">이 cmdlet이 읽는 Azure 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="f150a-121">컨텍스트를 지정 하지 않으면이 cmdlet은 로컬 기본 컨텍스트를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="f150a-122">-확인</span><span class="sxs-lookup"><span data-stu-id="f150a-122">-Confirm</span></span>
<span data-ttu-id="f150a-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f150a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f150a-124">-WhatIf</span></span>
<span data-ttu-id="f150a-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f150a-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f150a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f150a-127">CommonParameters</span></span>
<span data-ttu-id="f150a-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f150a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f150a-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f150a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f150a-130">입력</span><span class="sxs-lookup"><span data-stu-id="f150a-130">INPUTS</span></span>

### <span data-ttu-id="f150a-131">AzureRmProfile (일반. 인증. 모델)</span><span class="sxs-lookup"><span data-stu-id="f150a-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="f150a-132">출력</span><span class="sxs-lookup"><span data-stu-id="f150a-132">OUTPUTS</span></span>

### <span data-ttu-id="f150a-133">Microsoft. Azure. a PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f150a-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="f150a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f150a-134">NOTES</span></span>

## <span data-ttu-id="f150a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f150a-135">RELATED LINKS</span></span>
