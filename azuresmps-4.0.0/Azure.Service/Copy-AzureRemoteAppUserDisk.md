---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045698"
---
# <span data-ttu-id="d57ec-101">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="d57ec-101">Copy-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="d57ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d57ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d57ec-103">사용자의 사용자 디스크를 한 Azure RemoteApp 컬렉션에서 다른 항목으로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-103">Copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="d57ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d57ec-104">SYNTAX</span></span>

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d57ec-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d57ec-105">DESCRIPTION</span></span>
<span data-ttu-id="d57ec-106">**AzureRemoteAppUserDisk** cmdlet은 사용자의 사용자 디스크를 한 Azure RemoteApp 컬렉션 간에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-106">The **Copy-AzureRemoteAppUserDisk** cmdlet copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="d57ec-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d57ec-107">EXAMPLES</span></span>

### <span data-ttu-id="d57ec-108">예제 1: 사용자 디스크 복사</span><span class="sxs-lookup"><span data-stu-id="d57ec-108">Example 1: Copy a user disk</span></span>
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

<span data-ttu-id="d57ec-109">이 명령은 컬렉션의 UPN을 보유 한 Azure Active Directory 사용자의 사용자 디스크를 컬렉션 PattiFuller@contoso.com Contoso02 Contoso01 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-109">This command copies the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01 to the collection Contoso02.</span></span>
<span data-ttu-id="d57ec-110">Contoso02에 이미 사용자 디스크가 있는 경우 PattiFuller@contoso.com 이 명령은이를 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-110">If a user disk for PattiFuller@contoso.com already exists on Contoso02, this command overwrites it.</span></span>

## <span data-ttu-id="d57ec-111">변수</span><span class="sxs-lookup"><span data-stu-id="d57ec-111">PARAMETERS</span></span>

### <span data-ttu-id="d57ec-112">-DestinationCollectionName</span><span class="sxs-lookup"><span data-stu-id="d57ec-112">-DestinationCollectionName</span></span>
<span data-ttu-id="d57ec-113">대상 Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-113">Specifies the name of the destination Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="d57ec-114">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="d57ec-114">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="d57ec-115">이 cmdlet이 기존 사용자 디스크를 덮어쓴다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-115">Indicates that this cmdlet overwrites an existing user disk.</span></span>

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

### <span data-ttu-id="d57ec-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="d57ec-116">-Profile</span></span>
<span data-ttu-id="d57ec-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d57ec-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d57ec-119">-SourceCollectionName</span><span class="sxs-lookup"><span data-stu-id="d57ec-119">-SourceCollectionName</span></span>
<span data-ttu-id="d57ec-120">원본 Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-120">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="d57ec-121">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="d57ec-121">-UserUpn</span></span>
<span data-ttu-id="d57ec-122">이 cmdlet이 디스크를 복사 하는 사용자의 UPN (사용자 계정 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-122">Specifies the user principal name (UPN) of the user for whom this cmdlet copies the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d57ec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57ec-123">CommonParameters</span></span>
<span data-ttu-id="d57ec-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d57ec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57ec-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d57ec-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57ec-126">입력</span><span class="sxs-lookup"><span data-stu-id="d57ec-126">INPUTS</span></span>

## <span data-ttu-id="d57ec-127">출력</span><span class="sxs-lookup"><span data-stu-id="d57ec-127">OUTPUTS</span></span>

## <span data-ttu-id="d57ec-128">상속자</span><span class="sxs-lookup"><span data-stu-id="d57ec-128">NOTES</span></span>

## <span data-ttu-id="d57ec-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d57ec-129">RELATED LINKS</span></span>

[<span data-ttu-id="d57ec-130">제거-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="d57ec-130">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


