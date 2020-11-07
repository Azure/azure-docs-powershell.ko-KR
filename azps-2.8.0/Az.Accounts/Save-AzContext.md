---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 337fbe8fbfd11fdedad3fa13279dac60bac08455
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698234"
---
# <span data-ttu-id="ca8cf-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="ca8cf-101">Save-AzContext</span></span>

## <span data-ttu-id="ca8cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8cf-103">다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="ca8cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca8cf-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca8cf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ca8cf-105">DESCRIPTION</span></span>
<span data-ttu-id="ca8cf-106">Save-AzContext cmdlet은 다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="ca8cf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ca8cf-107">EXAMPLES</span></span>

### <span data-ttu-id="ca8cf-108">예제 1: 현재 세션의 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="ca8cf-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="ca8cf-109">이 예제에서는 현재 세션의 Azure 컨텍스트를 제공 된 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="ca8cf-110">예제 2: 지정 된 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="ca8cf-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="ca8cf-111">이 예제에서는 cmdlet에 전달 된 Azure 컨텍스트를 제공 된 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="ca8cf-112">변수</span><span class="sxs-lookup"><span data-stu-id="ca8cf-112">PARAMETERS</span></span>

### <span data-ttu-id="ca8cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8cf-113">-DefaultProfile</span></span>
<span data-ttu-id="ca8cf-114">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca8cf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ca8cf-115">-Force</span></span>
<span data-ttu-id="ca8cf-116">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="ca8cf-117">-Path</span><span class="sxs-lookup"><span data-stu-id="ca8cf-117">-Path</span></span>
<span data-ttu-id="ca8cf-118">인증 정보를 저장할 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="ca8cf-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="ca8cf-119">-Profile</span></span>
<span data-ttu-id="ca8cf-120">이 cmdlet이 읽는 Azure 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="ca8cf-121">컨텍스트를 지정 하지 않으면이 cmdlet은 로컬 기본 컨텍스트를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="ca8cf-122">-확인</span><span class="sxs-lookup"><span data-stu-id="ca8cf-122">-Confirm</span></span>
<span data-ttu-id="ca8cf-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca8cf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8cf-124">-WhatIf</span></span>
<span data-ttu-id="ca8cf-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca8cf-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca8cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8cf-127">CommonParameters</span></span>
<span data-ttu-id="ca8cf-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca8cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8cf-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca8cf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8cf-130">입력</span><span class="sxs-lookup"><span data-stu-id="ca8cf-130">INPUTS</span></span>

### <span data-ttu-id="ca8cf-131">AzureRmProfile (일반. 인증. 모델)</span><span class="sxs-lookup"><span data-stu-id="ca8cf-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="ca8cf-132">출력</span><span class="sxs-lookup"><span data-stu-id="ca8cf-132">OUTPUTS</span></span>

### <span data-ttu-id="ca8cf-133">Microsoft. Azure. a PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ca8cf-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="ca8cf-134">상속자</span><span class="sxs-lookup"><span data-stu-id="ca8cf-134">NOTES</span></span>

## <span data-ttu-id="ca8cf-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca8cf-135">RELATED LINKS</span></span>
