---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045483"
---
# <span data-ttu-id="51363-101">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="51363-101">Remove-AzureWebsite</span></span>

## <span data-ttu-id="51363-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51363-102">SYNOPSIS</span></span>
<span data-ttu-id="51363-103">Azure에서 지정 된 웹 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-103">Removes the specified website from Azure.</span></span>

## <span data-ttu-id="51363-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51363-104">SYNTAX</span></span>

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51363-105">설명은</span><span class="sxs-lookup"><span data-stu-id="51363-105">DESCRIPTION</span></span>
<span data-ttu-id="51363-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="51363-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="51363-108">**AzureWebsite** cmdlet은 확인 메시지 표시 여부에 관계 없이 Azure에서 지정 된 웹 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-108">The **Remove-AzureWebsite** cmdlet removes the specified website from Azure, either with or without a prompt for confirmation.</span></span>

## <span data-ttu-id="51363-109">예제의</span><span class="sxs-lookup"><span data-stu-id="51363-109">EXAMPLES</span></span>

### <span data-ttu-id="51363-110">예제 1: 현재 웹 사이트 제거</span><span class="sxs-lookup"><span data-stu-id="51363-110">Example 1: Remove the current website</span></span>
```
PS C:\> Remove-AzureWebsite
```

<span data-ttu-id="51363-111">이 예제에서는 Azure에서 현재 디렉터리와 연결 된 웹 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-111">This example removes the website in Azure associated with the current directory.</span></span>

### <span data-ttu-id="51363-112">예제 2: 확인 하지 않고 웹 사이트 제거</span><span class="sxs-lookup"><span data-stu-id="51363-112">Example 2: Remove a website without confirmation</span></span>
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

<span data-ttu-id="51363-113">이 예제에서는 확인 메시지 없이 내 사이트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-113">This example deletes the website named mySite without prompting for confirmation.</span></span>

## <span data-ttu-id="51363-114">변수</span><span class="sxs-lookup"><span data-stu-id="51363-114">PARAMETERS</span></span>

### <span data-ttu-id="51363-115">-Force</span><span class="sxs-lookup"><span data-stu-id="51363-115">-Force</span></span>
<span data-ttu-id="51363-116">지정 하는 경우 확인 메시지를 표시 하지 않고 지정 된 웹 사이트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-116">If specified, deletes the specified website without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51363-117">-이름</span><span class="sxs-lookup"><span data-stu-id="51363-117">-Name</span></span>
<span data-ttu-id="51363-118">삭제할 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-118">Specifies the name of the website to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51363-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="51363-119">-Profile</span></span>
<span data-ttu-id="51363-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51363-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="51363-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51363-122">-슬롯</span><span class="sxs-lookup"><span data-stu-id="51363-122">-Slot</span></span>
<span data-ttu-id="51363-123">웹 사이트의 슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-123">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51363-124">-확인</span><span class="sxs-lookup"><span data-stu-id="51363-124">-Confirm</span></span>
<span data-ttu-id="51363-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51363-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51363-126">-WhatIf</span></span>
<span data-ttu-id="51363-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51363-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51363-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51363-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51363-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51363-129">CommonParameters</span></span>
<span data-ttu-id="51363-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51363-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51363-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51363-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51363-132">입력</span><span class="sxs-lookup"><span data-stu-id="51363-132">INPUTS</span></span>

## <span data-ttu-id="51363-133">출력</span><span class="sxs-lookup"><span data-stu-id="51363-133">OUTPUTS</span></span>

## <span data-ttu-id="51363-134">상속자</span><span class="sxs-lookup"><span data-stu-id="51363-134">NOTES</span></span>

## <span data-ttu-id="51363-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51363-135">RELATED LINKS</span></span>

[<span data-ttu-id="51363-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="51363-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


