---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046147"
---
# <span data-ttu-id="5f6f1-101">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="5f6f1-101">Remove-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="5f6f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f6f1-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6f1-103">Azure RemoteApp 컬렉션에서 사용자의 사용자 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f6f1-103">Removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="5f6f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f6f1-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f6f1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5f6f1-105">DESCRIPTION</span></span>
<span data-ttu-id="5f6f1-106">**AzureRemoteAppUserDisk** Cmdlet은 Azure RemoteApp 컬렉션에서 사용자의 사용자 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f6f1-106">The **Remove-AzureRemoteAppUserDisk** cmdlet removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="5f6f1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5f6f1-107">EXAMPLES</span></span>

### <span data-ttu-id="5f6f1-108">예제 1: 사용자 디스크 제거</span><span class="sxs-lookup"><span data-stu-id="5f6f1-108">Example 1: Remove a user disk</span></span>
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="5f6f1-109">이 명령은 컬렉션 Contoso01에서 UPN을 사용 하는 Azure Active Directory 사용자의 사용자 디스크를 제거 합니다 PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="5f6f1-109">This command removes the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01.</span></span>

## <span data-ttu-id="5f6f1-110">변수</span><span class="sxs-lookup"><span data-stu-id="5f6f1-110">PARAMETERS</span></span>

### <span data-ttu-id="5f6f1-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="5f6f1-111">-CollectionName</span></span>
<span data-ttu-id="5f6f1-112">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f6f1-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f1-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="5f6f1-113">-Profile</span></span>
<span data-ttu-id="5f6f1-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f6f1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f6f1-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5f6f1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5f6f1-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="5f6f1-116">-UserUpn</span></span>
<span data-ttu-id="5f6f1-117">이 cmdlet이 디스크를 제거 하는 사용자의 UPN (사용자 계정 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f6f1-117">Specifies the user principal name (UPN) of the user for whom this cmdlet removes the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f1-118">-확인</span><span class="sxs-lookup"><span data-stu-id="5f6f1-118">-Confirm</span></span>
<span data-ttu-id="5f6f1-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f6f1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f6f1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f6f1-120">-WhatIf</span></span>
<span data-ttu-id="5f6f1-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5f6f1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f6f1-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f6f1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f6f1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6f1-123">CommonParameters</span></span>
<span data-ttu-id="5f6f1-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f6f1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6f1-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f6f1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6f1-126">입력</span><span class="sxs-lookup"><span data-stu-id="5f6f1-126">INPUTS</span></span>

## <span data-ttu-id="5f6f1-127">출력</span><span class="sxs-lookup"><span data-stu-id="5f6f1-127">OUTPUTS</span></span>

## <span data-ttu-id="5f6f1-128">상속자</span><span class="sxs-lookup"><span data-stu-id="5f6f1-128">NOTES</span></span>

## <span data-ttu-id="5f6f1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f6f1-129">RELATED LINKS</span></span>

[<span data-ttu-id="5f6f1-130">복사-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="5f6f1-130">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)


