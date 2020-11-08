---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045866"
---
# <span data-ttu-id="86b97-101">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="86b97-101">Remove-AzureRemoteAppUser</span></span>

## <span data-ttu-id="86b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86b97-102">SYNOPSIS</span></span>
<span data-ttu-id="86b97-103">Azure RemoteApp 컬렉션에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86b97-103">Removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="86b97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86b97-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86b97-105">설명은</span><span class="sxs-lookup"><span data-stu-id="86b97-105">DESCRIPTION</span></span>
<span data-ttu-id="86b97-106">**AzureRemoteAppUser** Cmdlet은 Azure RemoteApp 컬렉션에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86b97-106">The **Remove-AzureRemoteAppUser** cmdlet removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="86b97-107">예제의</span><span class="sxs-lookup"><span data-stu-id="86b97-107">EXAMPLES</span></span>

### <span data-ttu-id="86b97-108">Example1: 컬렉션에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="86b97-108">Example1: Remove a user from a collection</span></span>
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="86b97-109">이 명령은 Contoso 컬렉션에서 Azure ActiveDirectory 사용자를 제거 합니다 PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="86b97-109">This command removes the Azure ActiveDirectory user PattiFuller@contoso.com from the Contoso collection.</span></span>

## <span data-ttu-id="86b97-110">변수</span><span class="sxs-lookup"><span data-stu-id="86b97-110">PARAMETERS</span></span>

### <span data-ttu-id="86b97-111">-별칭</span><span class="sxs-lookup"><span data-stu-id="86b97-111">-Alias</span></span>
<span data-ttu-id="86b97-112">게시 된 프로그램 별칭을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86b97-112">Specifies a published program alias.</span></span>
<span data-ttu-id="86b97-113">이 매개 변수는 앱 당 게시 모드 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86b97-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="86b97-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="86b97-114">-CollectionName</span></span>
<span data-ttu-id="86b97-115">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86b97-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="86b97-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="86b97-116">-Profile</span></span>
<span data-ttu-id="86b97-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86b97-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86b97-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="86b97-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86b97-119">-Type</span><span class="sxs-lookup"><span data-stu-id="86b97-119">-Type</span></span>
<span data-ttu-id="86b97-120">사용자 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86b97-120">Specifies a user type.</span></span>
<span data-ttu-id="86b97-121">이 매개 변수에 허용 되는 값은 OrgId 또는 MicrosoftAccount입니다.</span><span class="sxs-lookup"><span data-stu-id="86b97-121">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

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

### <span data-ttu-id="86b97-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="86b97-122">-UserUpn</span></span>
<span data-ttu-id="86b97-123">예를 들어 사용자의 UPN (사용자 계정 이름)을 지정 합니다 user@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="86b97-123">Specifies the User Principal Name (UPN) of a user, for example, user@contoso.com.</span></span>

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

### <span data-ttu-id="86b97-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b97-124">CommonParameters</span></span>
<span data-ttu-id="86b97-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86b97-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b97-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86b97-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b97-127">입력</span><span class="sxs-lookup"><span data-stu-id="86b97-127">INPUTS</span></span>

## <span data-ttu-id="86b97-128">출력</span><span class="sxs-lookup"><span data-stu-id="86b97-128">OUTPUTS</span></span>

## <span data-ttu-id="86b97-129">상속자</span><span class="sxs-lookup"><span data-stu-id="86b97-129">NOTES</span></span>

## <span data-ttu-id="86b97-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86b97-130">RELATED LINKS</span></span>

[<span data-ttu-id="86b97-131">추가-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="86b97-131">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="86b97-132">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="86b97-132">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


