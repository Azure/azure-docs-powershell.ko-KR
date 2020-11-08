---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8E67D1A4-4247-4603-8D26-42D6D48FE686
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90c654432760061d5c2ba36675c958135329b225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045868"
---
# <span data-ttu-id="f38ba-101">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="f38ba-101">Remove-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="f38ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f38ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f38ba-103">Azure RemoteApp 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ba-103">Removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="f38ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f38ba-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppCollection [-CollectionName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f38ba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f38ba-105">DESCRIPTION</span></span>
<span data-ttu-id="f38ba-106">**AzureRemoteAppCollection** Cmdlet은 Azure RemoteApp 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ba-106">The **Remove-AzureRemoteAppCollection** cmdlet removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="f38ba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f38ba-107">EXAMPLES</span></span>

## <span data-ttu-id="f38ba-108">변수</span><span class="sxs-lookup"><span data-stu-id="f38ba-108">PARAMETERS</span></span>

### <span data-ttu-id="f38ba-109">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="f38ba-109">-CollectionName</span></span>
<span data-ttu-id="f38ba-110">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ba-110">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f38ba-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="f38ba-111">-Profile</span></span>
<span data-ttu-id="f38ba-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ba-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f38ba-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f38ba-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f38ba-114">-확인</span><span class="sxs-lookup"><span data-stu-id="f38ba-114">-Confirm</span></span>
<span data-ttu-id="f38ba-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ba-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f38ba-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f38ba-116">-WhatIf</span></span>
<span data-ttu-id="f38ba-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f38ba-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f38ba-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f38ba-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f38ba-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f38ba-119">CommonParameters</span></span>
<span data-ttu-id="f38ba-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ba-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f38ba-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f38ba-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f38ba-122">입력</span><span class="sxs-lookup"><span data-stu-id="f38ba-122">INPUTS</span></span>

## <span data-ttu-id="f38ba-123">출력</span><span class="sxs-lookup"><span data-stu-id="f38ba-123">OUTPUTS</span></span>

## <span data-ttu-id="f38ba-124">상속자</span><span class="sxs-lookup"><span data-stu-id="f38ba-124">NOTES</span></span>

## <span data-ttu-id="f38ba-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f38ba-125">RELATED LINKS</span></span>

[<span data-ttu-id="f38ba-126">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="f38ba-126">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="f38ba-127">새로운 AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="f38ba-127">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="f38ba-128">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="f38ba-128">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="f38ba-129">업데이트-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="f38ba-129">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


