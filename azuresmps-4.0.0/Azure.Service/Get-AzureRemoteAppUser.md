---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046316"
---
# <span data-ttu-id="8540a-101">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="8540a-101">Get-AzureRemoteAppUser</span></span>

## <span data-ttu-id="8540a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8540a-102">SYNOPSIS</span></span>
<span data-ttu-id="8540a-103">Azure RemoteApp 컬렉션의 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8540a-103">Lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8540a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8540a-104">SYNTAX</span></span>

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8540a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8540a-105">DESCRIPTION</span></span>
<span data-ttu-id="8540a-106">**AzureRemoteAppUser** Cmdlet은 Azure RemoteApp 컬렉션의 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8540a-106">The **Get-AzureRemoteAppUser** cmdlet lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8540a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8540a-107">EXAMPLES</span></span>

### <span data-ttu-id="8540a-108">예제 1: 컬렉션의 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="8540a-108">Example 1: List the users of a collection</span></span>
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

<span data-ttu-id="8540a-109">이 명령은 Contoso 라는 Azure RemoteApp 컬렉션에 대 한 액세스 권한이 있는 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8540a-109">This command lists the users who have access to the Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="8540a-110">변수</span><span class="sxs-lookup"><span data-stu-id="8540a-110">PARAMETERS</span></span>

### <span data-ttu-id="8540a-111">-별칭</span><span class="sxs-lookup"><span data-stu-id="8540a-111">-Alias</span></span>
<span data-ttu-id="8540a-112">게시 된 프로그램 별칭을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8540a-112">Specifies a published program alias.</span></span>
<span data-ttu-id="8540a-113">이 매개 변수는 앱 당 게시 모드 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8540a-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="8540a-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="8540a-114">-CollectionName</span></span>
<span data-ttu-id="8540a-115">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8540a-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="8540a-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="8540a-116">-Profile</span></span>
<span data-ttu-id="8540a-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8540a-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8540a-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8540a-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8540a-119">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="8540a-119">-UserUpn</span></span>
<span data-ttu-id="8540a-120">정보를 나열할 사용자의 UPN (사용자 계정 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8540a-120">Specifies the User Principal Name (UPN) of a user for which to list information.</span></span>
<span data-ttu-id="8540a-121">예를 들어 PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="8540a-121">For example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8540a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8540a-122">CommonParameters</span></span>
<span data-ttu-id="8540a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8540a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8540a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8540a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8540a-125">입력</span><span class="sxs-lookup"><span data-stu-id="8540a-125">INPUTS</span></span>

## <span data-ttu-id="8540a-126">출력</span><span class="sxs-lookup"><span data-stu-id="8540a-126">OUTPUTS</span></span>

## <span data-ttu-id="8540a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="8540a-127">NOTES</span></span>

## <span data-ttu-id="8540a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8540a-128">RELATED LINKS</span></span>

[<span data-ttu-id="8540a-129">추가-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="8540a-129">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="8540a-130">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="8540a-130">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="8540a-131">제거-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="8540a-131">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


