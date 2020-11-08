---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6E369BDF-AE3C-416B-81B7-097C20147CBE
online version: ''
schema: 2.0.0
ms.openlocfilehash: bb48f7412c957ceefb7df03d79e57ce8e75447d5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046130"
---
# <span data-ttu-id="a8978-101">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="a8978-101">Remove-AzureSBNamespace</span></span>

## <span data-ttu-id="a8978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8978-102">SYNOPSIS</span></span>
<span data-ttu-id="a8978-103">네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-103">Removes a namespace.</span></span>

## <span data-ttu-id="a8978-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8978-104">SYNTAX</span></span>

```
Remove-AzureSBNamespace -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8978-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a8978-105">DESCRIPTION</span></span>
<span data-ttu-id="a8978-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a8978-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a8978-108">**AzureSBNamespace** Cmdlet은 service Bus에 대 한 서비스 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-108">The **Remove-AzureSBNamespace** cmdlet removes a service namespace for Service Bus.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="a8978-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a8978-109">EXAMPLES</span></span>

## <span data-ttu-id="a8978-110">변수</span><span class="sxs-lookup"><span data-stu-id="a8978-110">PARAMETERS</span></span>

### <span data-ttu-id="a8978-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a8978-111">-Force</span></span>
<span data-ttu-id="a8978-112">이 설정을 사용 하면 확인 메시지를 표시 하지 않고 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-112">If enabled, removes the namespace without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a8978-113">-이름</span><span class="sxs-lookup"><span data-stu-id="a8978-113">-Name</span></span>
<span data-ttu-id="a8978-114">제거할 네임 스페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-114">Specifies the name of the namespace to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8978-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8978-115">-PassThru</span></span>
<span data-ttu-id="a8978-116">성공 하는 경우 작업이 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-116">Causes the operation to return true if it succeeds.</span></span>

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

### <span data-ttu-id="a8978-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="a8978-117">-Profile</span></span>
<span data-ttu-id="a8978-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8978-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8978-120">-확인</span><span class="sxs-lookup"><span data-stu-id="a8978-120">-Confirm</span></span>
<span data-ttu-id="a8978-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8978-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8978-122">-WhatIf</span></span>
<span data-ttu-id="a8978-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8978-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8978-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8978-125">CommonParameters</span></span>
<span data-ttu-id="a8978-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8978-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8978-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8978-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8978-128">입력</span><span class="sxs-lookup"><span data-stu-id="a8978-128">INPUTS</span></span>

## <span data-ttu-id="a8978-129">출력</span><span class="sxs-lookup"><span data-stu-id="a8978-129">OUTPUTS</span></span>

## <span data-ttu-id="a8978-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a8978-130">NOTES</span></span>

## <span data-ttu-id="a8978-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8978-131">RELATED LINKS</span></span>

[<span data-ttu-id="a8978-132">새로운 AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="a8978-132">New-AzureSBNamespace</span></span>](./New-AzureSBNamespace.md)


