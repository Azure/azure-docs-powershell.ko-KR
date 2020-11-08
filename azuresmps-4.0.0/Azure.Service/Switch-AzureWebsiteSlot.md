---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 496ABC97-A493-4E42-B998-28A907DFBC19
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0641fd7bc8dcfa5048ac3e9d922bade199af2bab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045939"
---
# <span data-ttu-id="6da66-101">Switch-AzureWebsiteSlot</span><span class="sxs-lookup"><span data-stu-id="6da66-101">Switch-AzureWebsiteSlot</span></span>

## <span data-ttu-id="6da66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6da66-102">SYNOPSIS</span></span>
<span data-ttu-id="6da66-103">다른 슬롯을 사용 하 여 웹 사이트의 생산 슬롯을 교체 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-103">Swaps the production slot for a website with another slot.</span></span>

## <span data-ttu-id="6da66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6da66-104">SYNTAX</span></span>

```
Switch-AzureWebsiteSlot [-Name <String>] [-Slot1 <String>] [-Slot2 <String>] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6da66-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6da66-105">DESCRIPTION</span></span>
<span data-ttu-id="6da66-106">**AzureWebsiteSlot** cmdlet은 다른 슬롯을 사용 하 여 웹 사이트의 프로덕션 슬롯을 교체 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-106">The **Switch-AzureWebsiteSlot** cmdlet swaps the production slot for a website with another slot.</span></span>
<span data-ttu-id="6da66-107">이는 슬롯이 두 개인 웹사이트 에서만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-107">This works on websites with two slots only.</span></span>

## <span data-ttu-id="6da66-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6da66-108">EXAMPLES</span></span>

### <span data-ttu-id="6da66-109">예제 1: 웹 사이트 슬롯 전환</span><span class="sxs-lookup"><span data-stu-id="6da66-109">Example 1: Switch Website Slot</span></span>
```
PS C:\> Switch-AzureWebsiteSlot -Name MyWebsite
```

<span data-ttu-id="6da66-110">Azure 웹 사이트 MyWebsite 백업 슬롯을 프로덕션 슬롯으로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-110">Switch the azure website MyWebsite backup slot with production slot.</span></span>

## <span data-ttu-id="6da66-111">변수</span><span class="sxs-lookup"><span data-stu-id="6da66-111">PARAMETERS</span></span>

### <span data-ttu-id="6da66-112">-Force</span><span class="sxs-lookup"><span data-stu-id="6da66-112">-Force</span></span>
<span data-ttu-id="6da66-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6da66-114">-이름</span><span class="sxs-lookup"><span data-stu-id="6da66-114">-Name</span></span>
<span data-ttu-id="6da66-115">웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-115">The name of the website.</span></span>

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

### <span data-ttu-id="6da66-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="6da66-116">-Profile</span></span>
<span data-ttu-id="6da66-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6da66-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6da66-119">-Slot1</span><span class="sxs-lookup"><span data-stu-id="6da66-119">-Slot1</span></span>
<span data-ttu-id="6da66-120">첫 번째 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-120">Specifies the first slot.</span></span>

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

### <span data-ttu-id="6da66-121">-Slot2</span><span class="sxs-lookup"><span data-stu-id="6da66-121">-Slot2</span></span>
<span data-ttu-id="6da66-122">두 번째 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-122">Specifies the second slot.</span></span>

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

### <span data-ttu-id="6da66-123">-확인</span><span class="sxs-lookup"><span data-stu-id="6da66-123">-Confirm</span></span>
<span data-ttu-id="6da66-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6da66-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6da66-125">-WhatIf</span></span>
<span data-ttu-id="6da66-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6da66-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6da66-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da66-128">CommonParameters</span></span>
<span data-ttu-id="6da66-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6da66-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da66-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da66-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da66-131">입력</span><span class="sxs-lookup"><span data-stu-id="6da66-131">INPUTS</span></span>

## <span data-ttu-id="6da66-132">출력</span><span class="sxs-lookup"><span data-stu-id="6da66-132">OUTPUTS</span></span>

## <span data-ttu-id="6da66-133">상속자</span><span class="sxs-lookup"><span data-stu-id="6da66-133">NOTES</span></span>

## <span data-ttu-id="6da66-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6da66-134">RELATED LINKS</span></span>

[<span data-ttu-id="6da66-135">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6da66-135">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="6da66-136">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6da66-136">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="6da66-137">시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6da66-137">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="6da66-138">중지-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6da66-138">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


