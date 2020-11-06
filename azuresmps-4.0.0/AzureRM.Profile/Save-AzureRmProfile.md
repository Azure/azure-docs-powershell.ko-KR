---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523552"
---
# <span data-ttu-id="3b5bd-101">Save-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="3b5bd-101">Save-AzureRmProfile</span></span>

## <span data-ttu-id="3b5bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b5bd-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5bd-103">다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="3b5bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b5bd-104">SYNTAX</span></span>

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b5bd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3b5bd-105">DESCRIPTION</span></span>
<span data-ttu-id="3b5bd-106">Save-AzureRmProfile cmdlet은 다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-106">The Save-AzureRmProfile cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="3b5bd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3b5bd-107">EXAMPLES</span></span>

### <span data-ttu-id="3b5bd-108">예제 1: 현재 세션의 프로필 저장</span><span class="sxs-lookup"><span data-stu-id="3b5bd-108">Example 1: Saving the current session's profile</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

<span data-ttu-id="3b5bd-109">이 예제에서는 현재 세션의 Azure 프로필을 제공 된 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-109">This example saves the current session's Azure profile to the JSON file provided.</span></span>

### <span data-ttu-id="3b5bd-110">예제 2: 지정 된 프로필 저장</span><span class="sxs-lookup"><span data-stu-id="3b5bd-110">Example 2: Saving a given profile</span></span>
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="3b5bd-111">이 예제에서는 cmdlet에 전달 된 Azure 프로필을 제공 된 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-111">This example saves the Azure profile that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="3b5bd-112">변수</span><span class="sxs-lookup"><span data-stu-id="3b5bd-112">PARAMETERS</span></span>

### <span data-ttu-id="3b5bd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3b5bd-113">-Force</span></span>
<span data-ttu-id="3b5bd-114">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-114">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="3b5bd-115">-Path</span><span class="sxs-lookup"><span data-stu-id="3b5bd-115">-Path</span></span>
<span data-ttu-id="3b5bd-116">인증 정보를 저장할 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b5bd-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="3b5bd-117">-Profile</span></span>
<span data-ttu-id="3b5bd-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b5bd-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5bd-120">-확인</span><span class="sxs-lookup"><span data-stu-id="3b5bd-120">-Confirm</span></span>
<span data-ttu-id="3b5bd-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b5bd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b5bd-122">-WhatIf</span></span>
<span data-ttu-id="3b5bd-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b5bd-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b5bd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5bd-125">CommonParameters</span></span>
<span data-ttu-id="3b5bd-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b5bd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5bd-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b5bd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5bd-128">입력</span><span class="sxs-lookup"><span data-stu-id="3b5bd-128">INPUTS</span></span>

## <span data-ttu-id="3b5bd-129">출력</span><span class="sxs-lookup"><span data-stu-id="3b5bd-129">OUTPUTS</span></span>

### <span data-ttu-id="3b5bd-130">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="3b5bd-130">PSAzureProfile</span></span>

## <span data-ttu-id="3b5bd-131">상속자</span><span class="sxs-lookup"><span data-stu-id="3b5bd-131">NOTES</span></span>

## <span data-ttu-id="3b5bd-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b5bd-132">RELATED LINKS</span></span>

[<span data-ttu-id="3b5bd-133">선택-AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="3b5bd-133">Select-AzureRMProfile</span></span>]()

