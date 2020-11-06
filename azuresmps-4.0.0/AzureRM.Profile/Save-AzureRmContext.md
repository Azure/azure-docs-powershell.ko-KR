---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522684"
---
# <span data-ttu-id="ce6d9-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ce6d9-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="ce6d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ce6d9-103">다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="ce6d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce6d9-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ce6d9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce6d9-105">DESCRIPTION</span></span>
<span data-ttu-id="ce6d9-106">Save-AzureRmContext cmdlet은 다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="ce6d9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ce6d9-107">EXAMPLES</span></span>

### <span data-ttu-id="ce6d9-108">예제 1: 현재 세션의 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="ce6d9-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="ce6d9-109">이 예제에서는 현재 세션의 Azure 컨텍스트를 제공 된 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="ce6d9-110">예제 2: 지정 된 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="ce6d9-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="ce6d9-111">이 예제에서는 cmdlet에 전달 된 Azure 컨텍스트를 제공 된 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="ce6d9-112">변수</span><span class="sxs-lookup"><span data-stu-id="ce6d9-112">PARAMETERS</span></span>

### <span data-ttu-id="ce6d9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ce6d9-113">-Force</span></span>
<span data-ttu-id="ce6d9-114">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6d9-115">-Path</span><span class="sxs-lookup"><span data-stu-id="ce6d9-115">-Path</span></span>
<span data-ttu-id="ce6d9-116">인증 정보를 저장할 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6d9-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="ce6d9-117">-Profile</span></span>
<span data-ttu-id="ce6d9-118">이 cmdlet이 읽는 Azure 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="ce6d9-119">컨텍스트를 지정 하지 않으면이 cmdlet은 로컬 기본 컨텍스트를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce6d9-120">-확인</span><span class="sxs-lookup"><span data-stu-id="ce6d9-120">-Confirm</span></span>
<span data-ttu-id="ce6d9-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6d9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce6d9-122">-WhatIf</span></span>
<span data-ttu-id="ce6d9-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce6d9-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce6d9-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="ce6d9-125">입력</span><span class="sxs-lookup"><span data-stu-id="ce6d9-125">INPUTS</span></span>

### <span data-ttu-id="ce6d9-126">AzureRMProfile (일반. 인증. 모델)</span><span class="sxs-lookup"><span data-stu-id="ce6d9-126">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="ce6d9-127">출력</span><span class="sxs-lookup"><span data-stu-id="ce6d9-127">OUTPUTS</span></span>

### <span data-ttu-id="ce6d9-128">Microsoft. Azure. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ce6d9-128">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="ce6d9-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ce6d9-129">NOTES</span></span>

## <span data-ttu-id="ce6d9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce6d9-130">RELATED LINKS</span></span>

