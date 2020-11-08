---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: EFBC8DCD-00CC-4BBF-9383-EA15376535F3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42780f62bc68659874f7aae1e64ad5ce89038fdf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045843"
---
# <span data-ttu-id="b0b58-101">Update-AzureWebsiteRepository</span><span class="sxs-lookup"><span data-stu-id="b0b58-101">Update-AzureWebsiteRepository</span></span>

## <span data-ttu-id="b0b58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b58-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b58-103">모든 슬롯에 대해 로컬 git 리포지토리의 원격 리포지토리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-103">Updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="b0b58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0b58-104">SYNTAX</span></span>

```
Update-AzureWebsiteRepository [-Name <String>] -PublishingUsername <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b58-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0b58-105">DESCRIPTION</span></span>
<span data-ttu-id="b0b58-106">**업데이트 AzureWebsiteRepository** cmdlet은 모든 슬롯에 대 한 로컬 git 리포지토리의 원격 리포지토리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-106">The **Update-AzureWebsiteRepository** cmdlet updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="b0b58-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0b58-107">EXAMPLES</span></span>

### <span data-ttu-id="b0b58-108">예제 1: 웹 사이트 원격 저장소 업데이트</span><span class="sxs-lookup"><span data-stu-id="b0b58-108">Example 1: Update Website Remote Repositories</span></span>
```
PS C:\> Update-AzureWebsiteRepository -Name MyWebsite
```

<span data-ttu-id="b0b58-109">웹 사이트 MyWebsite의 모든 슬롯에 대 한 로컬 git 리포지토리의 원격 리포지토리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-109">Updates the remote repositories of a local git repository for all the slots for website MyWebsite.</span></span>

## <span data-ttu-id="b0b58-110">변수</span><span class="sxs-lookup"><span data-stu-id="b0b58-110">PARAMETERS</span></span>

### <span data-ttu-id="b0b58-111">-이름</span><span class="sxs-lookup"><span data-stu-id="b0b58-111">-Name</span></span>
<span data-ttu-id="b0b58-112">웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-112">The name of the website.</span></span>

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

### <span data-ttu-id="b0b58-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="b0b58-113">-Profile</span></span>
<span data-ttu-id="b0b58-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b0b58-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b0b58-116">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="b0b58-116">-PublishingUsername</span></span>
<span data-ttu-id="b0b58-117">Git 배포에 대해 Microsoft Azure 포털에서 지정한 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-117">The username you have specified in the Microsoft Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="b0b58-118">-확인</span><span class="sxs-lookup"><span data-stu-id="b0b58-118">-Confirm</span></span>
<span data-ttu-id="b0b58-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b58-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b58-120">-WhatIf</span></span>
<span data-ttu-id="b0b58-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0b58-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b58-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b58-123">CommonParameters</span></span>
<span data-ttu-id="b0b58-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b58-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b58-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0b58-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b58-126">입력</span><span class="sxs-lookup"><span data-stu-id="b0b58-126">INPUTS</span></span>

## <span data-ttu-id="b0b58-127">출력</span><span class="sxs-lookup"><span data-stu-id="b0b58-127">OUTPUTS</span></span>

## <span data-ttu-id="b0b58-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b0b58-128">NOTES</span></span>

## <span data-ttu-id="b0b58-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0b58-129">RELATED LINKS</span></span>

[<span data-ttu-id="b0b58-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b0b58-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="b0b58-131">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b0b58-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="b0b58-132">시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b0b58-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="b0b58-133">중지-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b0b58-133">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


