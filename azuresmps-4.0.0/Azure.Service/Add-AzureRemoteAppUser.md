---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046381"
---
# <span data-ttu-id="24bab-101">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="24bab-101">Add-AzureRemoteAppUser</span></span>

## <span data-ttu-id="24bab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24bab-102">SYNOPSIS</span></span>
<span data-ttu-id="24bab-103">Azure RemoteApp 컬렉션에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-103">Adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="24bab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24bab-104">SYNTAX</span></span>

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="24bab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24bab-105">DESCRIPTION</span></span>
<span data-ttu-id="24bab-106">**Add-AzureRemoteAppUser** cmdlet은 사용자를 Azure RemoteApp 컬렉션에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-106">The **Add-AzureRemoteAppUser** cmdlet adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="24bab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="24bab-107">EXAMPLES</span></span>

### <span data-ttu-id="24bab-108">예제 1: Microsoft 계정을 사용 하 여 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="24bab-108">Example 1: Add a user using a Microsoft Account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="24bab-109">이 명령은 PattiFuller@contoso.com Contoso 라는 컬렉션에 Microsoft 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-109">This command adds the Microsoft Account PattiFuller@contoso.com to the collection named Contoso.</span></span>

### <span data-ttu-id="24bab-110">예제 2: Azure Active Directory 계정을 사용 하 여 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="24bab-110">Example 2: Add a user using an Azure Active Directory account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="24bab-111">이 명령은 PattiFuller@contoso.com Contoso 라는 컬렉션에 Azure Active Directory 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-111">This command adds the Azure Active Directory account PattiFuller@contoso.com to the collection named Contoso.</span></span>

## <span data-ttu-id="24bab-112">변수</span><span class="sxs-lookup"><span data-stu-id="24bab-112">PARAMETERS</span></span>

### <span data-ttu-id="24bab-113">-별칭</span><span class="sxs-lookup"><span data-stu-id="24bab-113">-Alias</span></span>
<span data-ttu-id="24bab-114">게시 된 프로그램 별칭을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-114">Specifies a published program alias.</span></span>
<span data-ttu-id="24bab-115">이 매개 변수는 앱 당 게시 모드 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-115">You can use this parameter only in per-app publishing mode.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bab-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="24bab-116">-CollectionName</span></span>
<span data-ttu-id="24bab-117">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="24bab-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="24bab-118">-Profile</span></span>
<span data-ttu-id="24bab-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="24bab-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="24bab-121">-Type</span><span class="sxs-lookup"><span data-stu-id="24bab-121">-Type</span></span>
<span data-ttu-id="24bab-122">사용자 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-122">Specifies a user type.</span></span>
<span data-ttu-id="24bab-123">이 매개 변수에 허용 되는 값은 OrgId 또는 MicrosoftAccount입니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-123">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bab-124">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="24bab-124">-UserUpn</span></span>
<span data-ttu-id="24bab-125">예를 들어 사용자의 UPN (사용자 계정 이름)을 지정 합니다 PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="24bab-125">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24bab-126">CommonParameters</span></span>
<span data-ttu-id="24bab-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24bab-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24bab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24bab-129">입력</span><span class="sxs-lookup"><span data-stu-id="24bab-129">INPUTS</span></span>

## <span data-ttu-id="24bab-130">출력</span><span class="sxs-lookup"><span data-stu-id="24bab-130">OUTPUTS</span></span>

## <span data-ttu-id="24bab-131">상속자</span><span class="sxs-lookup"><span data-stu-id="24bab-131">NOTES</span></span>

## <span data-ttu-id="24bab-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24bab-132">RELATED LINKS</span></span>

[<span data-ttu-id="24bab-133">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="24bab-133">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)

[<span data-ttu-id="24bab-134">제거-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="24bab-134">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


